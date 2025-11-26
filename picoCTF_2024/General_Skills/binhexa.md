
## binhexa

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

How well can you perfom basic binary operations?

Additional details will be available after launching your challenge instance.

nc titan.picoctf.net 57884

---

## Hints
(none)

---

## Analysis

This challenge tests the ability to perform fundamental binary operations:

Bitwise AND &

Bitwise OR |

Left shift <<

Right shift >>

Binary addition +

Binary multiplication *

The server gives two fixed binary numbers and requires solving each operation step-by-step. The final result must be converted to hexadecimal to obtain the flag. The key challenge is accuracy — any mistake forces you to retry.

---

## Methodology

**Step 1:** Listen to the website 

nc titan.picoctf.net 57884


<img width="1049" height="273" alt="image" src="https://github.com/user-attachments/assets/76ed8e14-cf44-4319-a9a6-a7081ec7ff82" />


**Step 2:** Binary Number 1 & Binary Number 2 

'&' uses boolen logic 

  1 0 1 1 1 1 0 1
& 0 1 0 0 1 0 0 0
-----------------
  0 0 0 0 1 0 0 0


<img width="434" height="234" alt="image" src="https://github.com/user-attachments/assets/52bb4f4f-5f93-4b4c-bc33-761792942e9d" />


**Step 3:** Binary Number 1 >> Binary Number 2 

01001000 >> 1  =  00100100

<img width="430" height="209" alt="image" src="https://github.com/user-attachments/assets/172c0945-eaa2-44df-9e88-f1fafd1ff955" />

**Step 4:** Binary Number 1 << Binary Number 2 

10111101 << 1 = 101111010

<img width="373" height="142" alt="image" src="https://github.com/user-attachments/assets/789a84ac-6570-43d2-b1f0-79bedae8db01" />

**Step 5:** Binary Number 1 * Binary Number 2 

10111101 × 01001000
= 011010100101000


<img width="363" height="149" alt="image" src="https://github.com/user-attachments/assets/e7287df3-9f4a-4a10-9a38-31d98956fdba" />


**Step 5:** Binary Number 1 + Binary Number 2 

10111101 + 01001000
= 0100000101


<img width="380" height="205" alt="image" src="https://github.com/user-attachments/assets/d0c6f136-b02c-4de3-8695-1a2a2d700ec0" />

**Step 6:** Binary Number 1 | Binary Number 2 

10111101
01001000
---------
11111101


<img width="478" height="154" alt="image" src="https://github.com/user-attachments/assets/78a0cdb2-b2d0-4fb9-9bc2-42112fa2d838" />


**Step 6:** Result of the last operation in hexadecimal


<img width="488" height="75" alt="image" src="https://github.com/user-attachments/assets/92828957-7bbe-4437-bde1-5e3ab540648b" />


---

## Flag

picoCTF{b1t---------b09}

---

## Reflection

This challenge highlights how essential binary operations are in low-level programming, embedded systems, and cybersecurity. The difficulty lies not in the concepts but in avoiding manual calculation mistakes. It reinforces bitwise logic and shifting—skills often used in exploit development, microcontroller programming, and cryptographic reasoning.

---

## Tools

Netcat (nc) — used to connect to the remote challenge server.

Binary Calculator — for verifying operations (optional, but helpful).

----

## References

[Binary Operations](https://www.geeksforgeeks.org/binary-operations-in-computer-programming/)

[Bitwise Operators](https://docs.python.org/3/library/stdtypes.html#bitwise-operations)
