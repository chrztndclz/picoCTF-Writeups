
## Commitment Issues

**Platform:** picoCTF 2024

**Author:** JEFFERY JOHN

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2024 
#General_Skills 
#Easy 

---

## Description

I accidentally wrote the flag down. Good thing I deleted it! You download the challenge files here:

    challenge.zip

---

## Hints
- Version control can help you recover files if you change or lose them!
- Read the chapter on Git from the picoPrimer here
- You can 'checkout' commits to see the files inside them

---

## Analysis

This challenge tests understanding of how Git stores history. Even if a file is deleted in the latest commit, its contents remain stored in previous commits inside .git/objects/. By inspecting commit objects, tree objects, and blob objects, you can recover deleted content—in this case, the flag.

---

## Methodology
**Step 1: ** Download the file

**Step 2: ** Unzip the file 


<img width="1048" height="641" alt="image" src="https://github.com/user-attachments/assets/c9bcf8ba-2f7b-474c-9d55-4f050e0b07a7" />


**Step 3:** Navigate the unzip file and go to drop-in/.git/objects/ef/

<img width="1050" height="168" alt="image" src="https://github.com/user-attachments/assets/6e3b77dc-ee9a-4666-bbcb-b6e39cec6549" />


**Step 4:** Recover Git Object Contents 

Use git cat-file

This prints the original message, which is likely the deleted flag.

git cat-file -p ef0b7cc6b98367fa168573c931e0f7098ef59182


<img width="739" height="215" alt="image" src="https://github.com/user-attachments/assets/9fb9f439-ce47-4bae-a95f-a1dfb8f030a0" />

The commit message says "remove sensitive info", meaning this commit deleted the flag. It also shows a parent commit hash, which still holds the original file.

**Step 5:** View Parent Commit

git cat-file -p ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0


<img width="732" height="187" alt="image" src="https://github.com/user-attachments/assets/47913702-4c7f-4694-a8ea-55492dd9daae" />

**Step 6:** Inspect that tree

git cat-file -p 61db7d05a8b7657aedc1e13320ca53623a364fe7


<img width="819" height="102" alt="image" src="https://github.com/user-attachments/assets/6697ed31-018c-44bd-a54a-e4195326107c" />

**Step 7:** Print the blob and retrieve the flag

git cat-file -p fca28bbf8dde2f49246166ae6512a1046fc4cbc3

<img width="726" height="60" alt="image" src="https://github.com/user-attachments/assets/91ae22eb-e1ff-40c7-b55c-1b3972844364" />


---

## Flag

picoCTF{s@n--------85}

---

## Reflection

This challenge reinforced how Git internally tracks data and why deleted files are never immediately lost. Understanding commits, trees, and blobs makes it possible to reconstruct past states and recover sensitive information from version control history. The exercise demonstrates why secure development requires careful cleaning of commit history—not simply deleting files.

---

## Tools

Git – Used to inspect commit, tree, and blob objects (git cat-file -p) to recover deleted file contents.

unzip – Extracted the challenge archive to reveal the Git repository.

----

## References

[Git Documentation](https://git-scm.com/doc)
