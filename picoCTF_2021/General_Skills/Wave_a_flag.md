## Wave a flag

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
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...


---

## Hints
- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
- Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.

---

## Analysis
This challenge tests basic command-line interaction and familiarity with program help flags. The binary prints a message guiding you to request help. Typical behavior: when run with `-h` or `--help`, a program will print usage information or additional messages. Because the program explicitly asks for `-h`, the flag is likely revealed as part of the help output. The correct approach is to download, make executable, run the program, and try common help arguments.


---

## Methodology
**Step 1:** Download the binary

<img width="657" height="47" alt="image" src="https://github.com/user-attachments/assets/77c69e06-42b2-4f32-baad-ba93978f7673" />


**Step 2:** Make it executable using `chmod` command 

chmod +x warm

**Step 3:** run the program

./warm

Output: Hello user! Pass me a -h to learn what I can do!


<img width="663" height="119" alt="image" src="https://github.com/user-attachments/assets/bf0d7100-e353-41a4-9687-947133c35a1f" />


Step 4: Request help using -h option as the output suggested
./warm -h 

Output: Oh, help? I actually don't do much, but I do have this flag here: picoCTF


<img width="652" height="74" alt="image" src="https://github.com/user-attachments/assets/9419a3b0-f968-4080-bc66-325b9ff7fadb" />


---

## Flag


picoCTF{b1s---------44}


---

## Reflection
This is an introductory challenge that reinforces a few small but important habits:

- Always try common options like `-h` and `--help` when interacting with binaries.

- Read program output carefully — many challenge authors include explicit hints.


---

## Tools

`wget` — to download the binary.
    
`chmod +x` — to make the binary executable.
    
`./warm` — run the binary.
    
`-h` / `--help` — common help/usage flags.

----

## References


- [Wget Manual](https://www.gnu.org/software/wget/manual/wget.html)

- [chmod)](https://man7.org/linux/man-pages/man1/chmod.1.html)


