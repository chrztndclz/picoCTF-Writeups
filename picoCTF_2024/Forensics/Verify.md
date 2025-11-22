
## Verify

**Platform:** picoCTF 2024

**Author:**  JEFFERY JOHN

**Category:** Forensics

**Difficulty:** Easy

Tags:
#picoCTF_2024
#Forensics 
#Easy 

---

## Description

People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.

Additional details will be available after launching your challenge instance.

ssh -p 55048 ctf-player@rhea.picoctf.net Using the password 1ad5be0d. Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden!

    Checksum: 5848768e56185707f76c1d74f34f4e03fb0573ecc1ca7b11238007226654bcda
    To decrypt the file once you've verified the hash, run ./decrypt.sh files/<file>.

---

## Hints

- Checksums let you tell if a file is complete and from the original distributor. If the hash doesn't match, it's a different file.
- You can create a SHA checksum of a file with sha256sum file or all files in a directory with sha256sum directory/*.
- Remember you can pipe the output of one command to another with |. Try practicing with the 'First Grep' challenge if you're stuck!

---

## Analysis

This challenge is about verifying file integrity using a SHA-256 checksum. Inside the remote machine, you’re given many files but only one is genuine. By running sha256sum on all files and comparing the results with the provided checksum, you can quickly identify the correct file. Once the matching file is found, you use the decrypt.sh script to reveal the real flag. The challenge mainly tests your ability to use basic command-line tools to confirm authenticity before processing a file.

---

## Methodology
**Step 1:** SSH into the challenge instance

ssh -p 55048 ctf-player@rhea.picoctf.net
password: 1ad5be0d

**Step 2:** Use ls command to view the files in the directory 

ls 


<img width="255" height="47" alt="image" src="https://github.com/user-attachments/assets/71828a56-1b7e-4423-9092-b2b67815fa94" />


**Step 3:** Use cat command to view the checksum.txt 


<img width="519" height="43" alt="image" src="https://github.com/user-attachments/assets/afdb1c17-0ef9-4c42-b35f-16745529fea2" />

We'll use this verify the flag

Step 4: Run SHA-256 on every file


<img width="1761" height="331" alt="image" src="https://github.com/user-attachments/assets/23ecbbb5-ab96-48b4-ab09-590f03abd6f2" />

sha256sum * → computes the hash of every file
grep <checksum> → filters and shows only the file with the matching hash

Step 5: Decrypt the matching file


<img width="408" height="81" alt="image" src="https://github.com/user-attachments/assets/9b29513d-f141-4e25-bdf4-52dbe5ba2df6" />


---

## Flag

picoCTF{tru---------195}

---

## Reflection

This task shows why verifying checksums is important in cybersecurity. Hashes help confirm that a file hasn’t been altered or replaced, which is essential for maintaining integrity and trust. It also reinforces the usefulness of simple Linux commands for analyzing data. Overall, the challenge demonstrates how integrity checks protect against tampered or fake files.

---

## Tools

ssh – Used to remotely access the challenge machine.

ls – Lists files and directories.

sha256sum – Computes SHA-256 hashes of files.

grep – Filters output to find matching text.

decrypt.sh – Provided script that decrypts the verified file.

----

## References
[SHA-256](https://linux.die.net/man/1/sha256sum)

[grep](https://linux.die.net/man/1/grep)
