
## Blame Game

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

Someone's commits seems to be preventing the program from working. Who is it? You can download the challenge files here:

    challenge.zip

---

## Hints
- In collaborative projects, many users can make many changes. How can you see the changes within one file?
- Read the chapter on Git from the picoPrimer here.
- You can use python3 (file).py to try running the code, though you won't need to for this challenge.

---

## Analysis

The provided Python file (message.py) fails immediately due to a syntax error: a missing closing parenthesis. Since the challenge is about tracking who caused the error, the correct approach is to use Git’s built-in line-tracking features.

The most relevant tool is git blame, which shows the commit and author responsible for each line in the file. By blaming message.py, we can see exactly which person last modified the incorrect line—and therefore determine the culprit.

---

## Methodology

**Step 1:** Download file 

**Step 2:** Unzip File 


<img width="647" height="406" alt="image" src="https://github.com/user-attachments/assets/afe88166-b81c-4bda-8c80-589f9becee2b" />


**Step 3:** Inspect the Python file


<img width="841" height="127" alt="image" src="https://github.com/user-attachments/assets/06d16c69-494a-40cb-9b21-c795f63eb78f" />


The file is broken, confirming the challenge objective.


**Step 4: ** Use git blame on the file

`git blame message.py`
2466febd (picoCTF{@sk--------2} 2024-03-12 00:07:06 +0000 1) print("Hello, World!"

To find out who changed the broken line

**Step 5: ** Inspect the commit

`git show 2466febd` 

commit 2466febd40004b9ca644ce924181d07e23dcfaeb
Author: picoCTF{@sk---------b2} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:06 2024 +0000

    optimize file size of prod code

diff --git a/message.py b/message.py
index 7df869a..326544a 100644
--- a/message.py
+++ b/message.py
@@ -1 +1 @@
-print("Hello, World!")
+print("Hello, World!"

---

## Flag

picoCTF{@sk---------5b2}

---

## Reflection

This challenge reinforces the importance of version control—specifically Git’s ability to track who changed what and when. In real development, git blame is essential for debugging regressions, understanding code history, and identifying when bugs were introduced. The exercise demonstrates how readable Git metadata is and why commit messages and proper code reviews matter.

---

## Tools

git blame	- Identified which commit/author last modified each line.

git show - Examined the commit that introduced the error.

Git Repository - Stored commit history and metadata needed to trace the bug.

Python3 Interpreter	- Confirmed the file was broken but not needed to solve challenge.

----

## References

[Git Blame Documentation](https://git-scm.com/docs/git-blame)

[Viewing Commit Details (git show)](https://git-scm.com/docs/git-show)
