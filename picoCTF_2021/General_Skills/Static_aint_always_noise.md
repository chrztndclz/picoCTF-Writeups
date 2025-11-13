## Static ain't always noise

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
Can you look at the data in this binary: `static?` This `BASH script` might help!

---

## Hints
(none)

---

## Analysis
This challenge introduces the idea of **static analysis** — examining a binary file without executing it directly to understand its contents.  
The helper script `ltdis.sh` (short for “little disassembler”) automates **disassembly** and **string extraction**. It’s a useful reminder that many CTF binaries contain readable flag fragments or clues inside their compiled code.


---

## Methodology
**Step 1:** Download all the binary files

**Step 2:** Make the files executable 

chmod +x static
chmod +x ltdis.sh

**Step 3:** Run the binary 


<img width="756" height="79" alt="image" src="https://github.com/user-attachments/assets/16515b1e-effc-4c42-adf0-fbce4690d4b1" />


This indicates that the flag is hidden inside the binary, not printed during execution.

Step 4: Run the helper script


<img width="755" height="133" alt="image" src="https://github.com/user-attachments/assets/f47fc405-58cb-418b-810c-a93646fd6dbf" />


This command disassembles and extracts strings from `static`, generating two new files.

Step 5 — List the new files


<img width="758" height="75" alt="image" src="https://github.com/user-attachments/assets/3dc9f29b-5961-4b91-a51b-1b7a1c22042a" />


Step 6 — Inspect the strings file


<img width="759" height="55" alt="image" src="https://github.com/user-attachments/assets/4761f3b3-fa60-4384-bae9-cab28f3941a4" />


Step 7: Record the flag 


---

## Flag

picoCTF{d15---------08}

---

## Reflection
This challenge focuses on learning how to analyze binaries statically—without executing them. It emphasizes the importance of checking for embedded strings within binaries, as developers often leave readable information inside compiled executables. Tools such as `strings`, `objdump`, and helper scripts like `ltdis.sh` can greatly simplify this process. Overall, static analysis serves as a crucial preliminary step before dynamic execution, helping to prevent unintended behavior or potential malware execution.

---

## Tools
chmod — change file permissions to make executables runnable.

cat — view the content of text files.

grep — search for patterns like “picoCTF”.

strings — extract printable characters from binary files (used inside ltdis.sh).

----

## References

[chmod Command](https://man7.org/linux/man-pages/man1/chmod.1.html)

[cat Command](https://man7.org/linux/man-pages/man1/cat.1.html)

[grep Command](https://man7.org/linux/man-pages/man1/grep.1.html)

[strings Command](https://man7.org/linux/man-pages/man1/strings.1.html)
