## Python Wrangling

**Platform:** picoCTF 2021

**Author:** SYRAEL

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2021 
#General_Skills 
#Easy 

---

## Description
Python scripts are invoked kind of like programs in the Terminal... Can you run `this Python script` using `this password` to get `the flag`?


---

## Hints
- Get the Python script accessible in your shell by entering the following command in the Terminal prompt: $ wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py
- $ man python

---

## Analysis
`ende.py` is a small command-line Python utility that supports encryption (`-e`) and decryption (`-d`) of a file. The encrypted flag is provided as `flag.txt.en` and the password is in `pw.txt`. The simplest approach: download all files, read `pw.txt` to obtain the password, then run `ende.py` in decrypt mode on `flag.txt.en`, supplying the password when prompted.

---

## Methodology

**Step 1:** Download the files 

wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py
wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en
wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt


**Step 2:** First let's try to run ende.py using python command 


<img width="693" height="143" alt="image" src="https://github.com/user-attachments/assets/acef89db-71fd-4c86-bc80-83adc2b3a13e" />


-e stands for encrypt
-d stands for decrypt

Basically we'll use the ende.py to decrypt the flag.txt.en file to see the flag. 

**Step 3:** Let's first get the password in the .txt file using cat command 


<img width="692" height="70" alt="image" src="https://github.com/user-attachments/assets/dd6bc3c2-10e6-402b-8301-ddc246bdb0e8" />


Step 4: Decrypt the flag

<img width="693" height="66" alt="image" src="https://github.com/user-attachments/assets/0f1d02e6-cf50-4a87-8724-b9a0a13fa86c" />


---

## Flag

picoCTF{4p0---------0ff}

---

## Reflection
This exercise reinforces basic Python script usage and file I/O on the command line: downloading assets, reading plaintext files for secrets, and running scripts with command-line options. When a script accepts `-e`/`-d`, try both modes only with files you control; avoid decrypting unknown files unless you understand the script.

---

## Tools
python - programming language
cat - view plaintext files.



----

## References

[python 3](https://docs.python.org/3/)

[cat](https://man7.org/linux/man-pages/man1/cat.1.html)
