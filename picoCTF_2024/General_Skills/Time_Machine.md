
## Time Machine

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

What was I last working on? I remember writing a note to help me remember... You can download the challenge files here:

    challenge.zip

---

## Hints
- The cat command will let you read a file, but that won't help you here!
- Read the chapter on Git from the picoPrimer here
- When committing a file with git, a message can (and should) be included.

---

## Analysis

The challenge revolves around discovering previous work saved in a Git repository. The dropped-in folder contains a .git directory, which stores commit history. Since the hint mentions that commit messages can contain useful notes, the flag is likely included in one of these messages. Inspecting the Git logs reveals the necessary information.

---

## Methodology
**Step 1:** Download the file

**Step 2:** Unzip the file 


<img width="668" height="389" alt="image" src="https://github.com/user-attachments/assets/1748e32e-62ae-4cf5-81d0-af9370ed9e96" />

<img width="668" height="73" alt="image" src="https://github.com/user-attachments/assets/0bb3c8b8-4e3b-4361-ad8a-e535c6180780" />


**Step 3:** go to the drop-in directory

<img width="661" height="72" alt="image" src="https://github.com/user-attachments/assets/3512ac56-713d-458a-861f-75f597ab5631" />

**Step 4:** go to the drop-in directory and cat the messsage.txt file 


<img width="706" height="202" alt="image" src="https://github.com/user-attachments/assets/77dce3b8-3894-4f3b-ad67-05ee5ee034f3" />

**Step 4:** go to the Git directory 


<img width="754" height="132" alt="image" src="https://github.com/user-attachments/assets/ddbe1b30-39b2-45c1-ba57-c5e433811b98" />

Step 5: Check the Git commit logs

The file .git/logs/HEAD is a log that tracks movements of the HEAD pointer—this includes every commit you check out or create.


<img width="1226" height="274" alt="image" src="https://github.com/user-attachments/assets/c6d80468-3201-4327-914a-ff0bf0590f6f" />


Step 6: Retrieve the Flag 

---

## Flag

picoCTF{t1m--------c0f}

---

## Reflection

This challenge demonstrates how Git preserves detailed history, including commit messages. Even if files appear unchanged or unhelpful, the repository logs may contain important information. It reinforces the importance of understanding Git’s internal structure and how to navigate .git directories for forensics and CTF tasks.

---

## Tools

cat – Displays file contents; used to read Git log files.

git – Version control system; its internal logs store commit messages where the flag was hidden.

----

## References

[picoCTF Git Primer](https://primer.picoctf.com/#_git)

[cat command: https](//man7.org/linux/man-pages/man1/cat.1.html)
