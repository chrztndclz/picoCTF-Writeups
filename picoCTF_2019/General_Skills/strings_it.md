# strings it

**Platform:** picoCTF  
**Author:** SANJAY C / DANNY TUNITIS  
**Category:** General Skills  
**Difficulty:** Easy  

---

## Description
Can you find the flag in the 'file' without running it?

---

## Hints
- `strings`

---

## Analysis
Based on the hint, the challenge requires the use of the `strings` command.

---

## Methodology
**Step 1:** Download the provided file.  

**Step 2:** Navigate to the file’s directory using the terminal.  

**Step 3:** Run the `strings` command to read all printable text from the file:


<img width="666" height="729" alt="image" src="https://github.com/user-attachments/assets/0528b16c-1675-4a38-86c4-36887f16e8ec" />


You’ll see a large number of random strings printed on the screen. Searching manually would take too long, so we can use another command to filter the output.

**Step 4:** Use the grep command to search specifically for lines containing “picoCTF”:


<img width="666" height="44" alt="image" src="https://github.com/user-attachments/assets/f739dc4b-c130-43f9-9a4d-c92dc117288d" />

---

## Flag
picoCTF{5tRIng5_'REDACTED'_aee91}

---

## Reflection
This challenge demonstrates how simple command-line tools like strings and grep can be powerful for extracting hidden information from binary files. It reinforces the importance of understanding basic Linux utilities and their use in cybersecurity investigations. By combining strings with grep, we can efficiently filter large outputs and locate specific patterns such as flags or keywords—an essential skill in CTFs and real-world analysis tasks.

---

## Tools

strings command – Extracts readable text from binary files.

grep command – Searches and filters text for specific patterns.

---

## References

[GNU Coreutils Manual – strings](https://man7.org/linux/man-pages/man1/strings.1.html)

[GNU Grep Manual – grep](https://man7.org/linux/man-pages/man1/grep.1.html)

[picoCTF Official Website](https://picoctf.org)


