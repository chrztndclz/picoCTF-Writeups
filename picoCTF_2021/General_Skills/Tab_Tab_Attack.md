## Tab, Tab, Attack

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
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip

---

## Hints
- After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...

---

## Analysis
This challenge focuses on **Linux navigation efficiency** — particularly using the **Tab key for auto-completion**.  
The zip file contains a deeply nested folder structure, and the flag is hidden inside one of the files.  
The trick is to use the **Tab key** to quickly move through directories without typing long names manually.

---

## Methodology

**Step 1:** Download the provided zip file (`Addadshashanammu.zip`).

**Step 2:** Unzip the archive:
unzip Addadshashanammu.zip


<img width="1105" height="216" alt="image" src="https://github.com/user-attachments/assets/5f988ec9-c55e-44af-8030-1fcaf1c0bd99" />


You’ll now see a large nested folder structure.

**Step 3:** Navigate through the directories using the `cd` command and the **Tab key** for auto-completion.

Pressing `Tab` fills in the full directory name automatically. Keep doing this until you reach the last directory.

**Step 4:** Once inside the final folder, list its contents:

You’ll find a file named `fang-of-haynekhtnamet`.


<img width="776" height="532" alt="image" src="https://github.com/user-attachments/assets/7eda3722-f604-4a7d-928d-629cbb45f2b0" />


**Step 5:** Read the file’s contents using the `strings` command to extract readable text:

strings fang-of-haynekhtnamet


<img width="735" height="511" alt="image" src="https://github.com/user-attachments/assets/9e688bb4-e57f-4605-b6fc-92aadc4c0a3b" />



**Step 6:** Look for the flag in the output — it follows the format: picoCTF{...}


---

## Flag
picoCTF{l3v----------e70}

---

## Reflection

This challenge highlights the power of **command-line efficiency**.  
Instead of typing long or confusing directory names, **tab completion** allows you to navigate quickly and accurately — a vital skill in Linux-based environments, cybersecurity tasks, and CTF competitions.  
It’s also a reminder to explore files systematically and make use of tools like `strings` for inspecting binary files.

---

## Tools
unzip command - Extracts compressed `.zip` archives into directories and files.
strings command - Displays readable (ASCII) text found inside binary files.
tab key - Quickly completes file or directory names in the terminal.

----

## References
- [unzip Command](https://linuxize.com/post/how-to-unzip-files-in-linux/)
    
- [strings Command)](https://man7.org/linux/man-pages/man1/strings.1.html)
    
- [Tab Completion in Bash](https://www.gnu.org/software/bash/manual/html_node/Commands-For-Completion.html)
    
- [Linux Command Line Basics](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview)
