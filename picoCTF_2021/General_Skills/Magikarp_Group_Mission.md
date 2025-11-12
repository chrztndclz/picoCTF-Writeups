## Magikarp Ground Mission

**Platform:** picoCTF 2021

**Author:** SYREAL

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2021
#General_Skills 
#Easy 

---

## Description
Do you know how to move between directories and read files in the shell? Start the container, ssh to it, and then ls once connected to begin.

Additional details will be available after launching your challenge instance.

Launch Instance: 

Do you know how to move between directories and read files in the shell? Start the container, ssh to it, and then ls once connected to begin. Login via ssh as ctf-player with the password, 8c606eb1 on the host wily-courier.picoctf.net and port 56086.

---

## Hints
Finding a cheatsheet for bash would be really helpful!

---

## Analysis
This challenge is a beginner-level task focused on basic Linux commands and SSH access. You connect to a remote server, explore directories, and use simple commands like `ls`, `cd`, and `cat` to locate and read text files containing pieces of the flag. It’s a straightforward exercise to build comfort with terminal navigation and file reading.


---

## Methodology
Step 1: Launch the Instance
Start the challenge instance on the picoCTF website to get the SSH login details.

Step 2: 
Connect via SSH

<img width="837" height="494" alt="image" src="https://github.com/user-attachments/assets/767ae593-6dc0-47a5-bb7e-f35821586001" />


Step 3: Explore the Directory
List the current directory using `ls command`

You’ll find: 1of3.flag.txt

Step 4: Read the first flag using `cat command`
cat 1of3.flag.txt

Output: picoCTF{xxsh_

Step 5: Read the instruction using `cat command`
cat instructions-to-2of3.txt

Output: "Next, go to the root of all things, more succinctly `/`."


<img width="469" height="145" alt="image" src="https://github.com/user-attachments/assets/60aec2ca-fd46-4266-954f-a1ae883f119c" />


Step 6: Go to root directory using `cd /`  command and list the files inside using `ls` command

Step 7: Read the second flag using `cat command`
cat 2of3.flag.txt

Output: 0ut_0f_//4t3r_

Step 8: Read the instruction using `cat command`
"Lastly, ctf-player, go home... more succinctly `~`."


<img width="1241" height="153" alt="image" src="https://github.com/user-attachments/assets/2dec9e1c-b557-44f1-bd72-2f58a637a185" />


Step 9: Go to home directory using `cd ~` command and list the files inside using `ls` command

Step 10: Read the third flag using `cat command`
cat 3of3.flag.txt

Output: 0b24fc4f}


<img width="333" height="102" alt="image" src="https://github.com/user-attachments/assets/aea788c8-a274-4d0b-99e2-28969510f661" />


---

## Flag

picoCTF{xxs---------c4f}

---

## Reflection
This challenge is an excellent introduction to using the Linux terminal. It shows how simple commands can help you explore a system and find hidden information. By completing this task, you learn how to connect to a remote server securely with SSH and how to navigate using commands like `cd`, `ls`, and `cat`.

It reinforces that understanding the basics of the command line is essential in cybersecurity, as it’s often used to access, analyze, and retrieve data from systems in real-world scenarios. This foundational knowledge prepares you for more advanced challenges that involve automation, scripting, and file system analysis.

---

## Tools


**SSH** - Connects securely to a remote system through the terminal.
**cd** - Moves between directories.
**ls** - Lists files and folders in the current location.
**cat** - Displays file contents directly in the terminal.


----

## References

[OpenSSH Manual](https://man.openbsd.org/ssh)

[GNU Coreutils Manual](https://www.gnu.org/software/coreutils/manual/coreutils.html)

[cd command](https://man7.org/linux/man-pages/man1/bash.1.html)
