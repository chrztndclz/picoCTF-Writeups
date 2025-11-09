# Title

**Platform:** picoCTF 2019

**Author:** JEDAVIS/DANNY

**Category:**  Forensics

**Difficulty:** Easy

---

## Description
This 'garden' contains more than it seems.


---

## Hints
What is a hex editor?

---

## Analysis

When you download the file and open it, you’ll see it’s a **JPEG image** (`garden.jpg`). At first glance, it appears to be an ordinary picture.  

However, the challenge description suggests that there might be **hidden information** within the file — not visible through normal viewing.

The hint, “What is a hex editor?”, indicates that the data we’re looking for might be embedded directly in the **binary (hexadecimal)** structure of the file.  
Therefore, we can inspect the image at the byte level using a **hex editor**.

---

## Methodology

**Step 1:** Download the File
Save the provided `garden.jpg` file to your working directory.

**Step 2:** Install a Hex Editor
If you’re using **Kali Linux**, install **hexedit** using the command:

<img width="236" height="47" alt="image" src="https://github.com/user-attachments/assets/4bcb5fca-a670-4257-a6dd-9589d057381e" />

Hex editors allow you to view and edit the **raw data** (in hexadecimal) of any file. Each byte is represented by two hex digits, and an ASCII translation appears beside it.


**Step 3:** Open the File in Hexedit
`hexedit garden.jpg`

You’ll see a large grid of hexadecimal values on the left and corresponding ASCII text on the right.

**Step 4:** Search for the Flag
Instead of manually scanning the data, use hexedit’s built-in search feature:

1. Press `/` to start a search.
2. Type:
    `picoCTF`
    and press **Enter**.

This searches for the ASCII text that matches the flag format (`picoCTF{...}`).


<img width="1890" height="759" alt="image" src="https://github.com/user-attachments/assets/a4d0a03e-cdb8-4392-bd2c-58cfde948702" />


**Step 5:** Adjust or Navigate the Offset (if needed)
If the flag is partially visible or located deeper in the file:

- Press **Ctrl + G** to go to a specific offset (memory address).
- You can move through the data to explore nearby bytes until the entire flag is visible.




---

## Flag

picoCTF{more_than_m33ts_the_'REDACTED'}


---

## Reflection

This challenge demonstrates the importance of understanding how data can be embedded within files.  

Even though an image may appear normal, its binary contents can hide **text strings, metadata, or even encoded data**.  

Learning to use tools like **hex editors** and commands like `strings` is essential for forensic analysis and reverse engineering in cybersecurity.

---

## Tools

hexedit – A command-line hex editor used to view and modify binary data.

----

## References

[hexedit](https://linux.die.net/man/1/hexedit)

