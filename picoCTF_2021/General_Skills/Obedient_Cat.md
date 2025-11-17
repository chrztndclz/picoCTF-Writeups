
## Obedient Cat

**Platform:** picoCTF 2021

**Author:** SYRAEL

**Category:** General Skills 

**Difficulty:**  Easy

Tags:
#picoCTF_2021 
#General_Skills 
#Easy 

---

## Description

This file has a flag in plain sight (aka "in-the-clear"). Download flag.

---

## Hints
- Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
- To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
- $ man cat
---

## Analysis
The challenge itself states that the flag is “in plain sight,” meaning you don’t have to decode, extract, or crack anything. Simply viewing the file’s contents will reveal the flag.

---

## Methodology
**Step 1:** Download the file 
**Step 2:** **View the file using `cat`**

`cat flag`

**Step 3:** **Copy the flag**

The flag will be printed directly onto the terminal.

---

## Flag

picoCTF{s4n--------01}

---

## Reflection

This challenge reinforces basic command-line usage and file manipulation. It highlights how simple tools like `wget` and `cat` are often enough to retrieve information during CTF tasks. No decoding or exploitation was needed—just understanding how to read a downloaded file.


---

## Tools
**wget** — to download the file
**cat** — to display file contents
**Terminal** — basic Linux command-line environment

----

## References

[cat manual page](https://man7.org/linux/man-pages/man1/cat.1.html)
