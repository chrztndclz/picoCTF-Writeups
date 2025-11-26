
## endianness

**Platform:** picoCTF 2024

**Author:** NANA AMA ATOMBO-SACKEY

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2024 
#General_Skills 
#Easy 

---

## Description

Know of little and big endian? Source

Additional details will be available after launching your challenge instance.

nc titan.picoctf.net 62405

---

## Hints
- You might want to check the ASCII table to first find the hexadecimal representation of characters before finding the endianness.
- Read more about how endianness here
  
  Little endian = reverse the byte order.

  Big endian = normal left-to-right byte order.

---

## Analysis

This challenge tests understanding of how data is stored in memory using different byte orders. Big endian preserves the natural left-to-right order of bytes, while little endian reverses them. By converting each character of the provided word into hexadecimal ASCII values, reversing the order, and submitting both formats, the server verifies whether you understand the concept of endianness.



---

## Methodology
**Step 1:** 

nc titan.picoctf.net 62405

<img width="690" height="160" alt="image" src="https://github.com/user-attachments/assets/75dba890-12f9-4ac7-a2ed-3113e373544b" />


**Step 2:** Convert the characters 'izqqr' into hex using cyberchef

i - 69
z - 7a
q - 71
q - 71
r - 72

<img width="866" height="250" alt="image" src="https://github.com/user-attachments/assets/e7683a2c-85c7-4521-8b89-03c5bf9d8fc1" />


**Step 3:** Little Endian reverse the byte order.

izqqr - rqqzi

r - 72
q - 71
q - 71
z - 7a
i - 69

`7271717a69`

<img width="654" height="160" alt="image" src="https://github.com/user-attachments/assets/0ca8b360-c865-41d8-9636-20b150970514" />


**Step 4:** Big Endian normal byte order.

izqqr

i - 69
z - 7a
q - 71
q - 71
r - 72

`697a717172`

<img width="653" height="198" alt="image" src="https://github.com/user-attachments/assets/7423f974-e665-40ce-9965-740d86662d8c" />


Step 5: Retrieve the flag 


---

## Flag

picoCTF{3nd---------ef0}

---

## Reflection

This challenge reinforces how computers store data in memory and why byte order matters when interpreting binary information. Converting characters to hex and manipulating the order helps build a deeper understanding of how low-level systems handle strings, integers, and other data structures. It also highlights why developers and security researchers must pay attention to endianness when analyzing binaries, network packets, or encoded data.

---

## Tools

Netcat (nc) – used to connect to the remote picoCTF instance.

ASCII Table – reference for converting characters to hexadecimal.

Hex Calculator / CyberChef (optional) – quick conversion and verification.

----

## References

[ASCII Table](https://www.asciitable.com)

[Endianness](https://developer.mozilla.org/en-US/docs/Glossary/Endianness)

[Netcat](https://nc110.sourceforge.net/)
