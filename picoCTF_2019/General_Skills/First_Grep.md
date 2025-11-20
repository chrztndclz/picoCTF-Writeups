
## First Grep

**Platform:** First Grep

**Author:** ALEX FULTON/DANNY TUNITIS

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2019 
#General_Skills 
#Easy 

---

## Description

Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way. The flag is in this `file`.

---

## Hints
- grep tutorial

---

## Analysis

This challenge involves scanning a long text file. Instead of reading everything manually, using `grep` is the most efficient way to search for the flag pattern (e.g., text containing `picoCTF`).

---

## Methodology

**Step 1:** Download the file

**Step 2:** View the file briefly to confirm its contents:

`cat file`

**Step 3:** use grep to find the flag 

`grep "picoCTF" file`


<img width="1891" height="470" alt="image" src="https://github.com/user-attachments/assets/0311c51c-730f-4b3a-8e4f-3b75c50bb51d" />


**Step 4:** The command will return the exact line containing the flag.

---

## Flag

picoCTF{gre--------591}

---

## Reflection

This challenge demonstrates the importance of efficient text searching in CTFs and real-world tasks. Instead of manually scanning through large files, tools like `grep` allow you to locate important information instantly. Becoming comfortable with command-line search tools speeds up your workflow significantly and is essential for future challenges involving logs, dumps, and encoded data

---

## Tools

`cat` — for quickly viewing file contents

`grep` — for searching patterns inside files


----

## References

[cat ](https://www.gnu.org/software/coreutils/manual/html_node/cat-invocation.html)

[grep](https://www.gnu.org/software/grep/manual/grep.html)

