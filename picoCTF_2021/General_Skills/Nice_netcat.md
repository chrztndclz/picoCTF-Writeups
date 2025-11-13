## Nice netcat...

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
There is a nice program that you can talk to by using this command in a shell: $ nc mercury.picoctf.net 22902, but it doesn't speak English...

---

## Hints
- You can practice using netcat with this picoGym problem: what's a netcat?
- You can practice reading and writing ASCII with this picoGym problem: Let's Warm Up

---

## Analysis
From the description, this challenge involves using **netcat (nc)** to connect to a server and receive a message. The hint that it “doesn’t speak English” suggests that the output will likely be a list of numbers that must be translated into readable text to reveal the flag.

---

## Methodology
**Step 1:** Connect to the server  
Use the given command in the terminal:

nc mercury.picoctf.net 22902

**Step 2:** Observe the output  
After connecting, you’ll receive a sequence of numbers separated by spaces.  
These numbers represent decimals corresponding to characters in the flag.


<img width="277" height="743" alt="image" src="https://github.com/user-attachments/assets/79a1a572-eb7d-4759-b660-035b01919a15" />


**Step 3:** Convert the numbers to text  
You can use **CyberChef** or a simple Python script to decode the numbers.


**Step 3:** Add the following operation to the Recipe: 


<img width="984" height="333" alt="image" src="https://github.com/user-attachments/assets/ef100536-fcee-409a-9054-6528a323fac2" />


Step 4: Retrieve the flag
The decoded message reveals the flag.

---

## Flag

picoCTF{g00---------6df}


---

## Reflection
This challenge demonstrates how network tools like **netcat** can be used to interact with remote services and how data transmitted over such connections isn’t always human-readable. By decoding ASCII values, we learn to recognize encoded data formats and practice basic data translation — a fundamental skill in cybersecurity and CTF problem-solving.

---

## Tools

Netcat (nc) - A command-line utility for reading from and writing to network connections using TCP or UDP.

**CyberChef** – A web-based tool for performing a wide range of data format conversions, encodings, and decoding operations with a simple “recipe” interface.

----

## References
[Netcat (Kali Linux Docs)](https://www.kali.org/tools/netcat/)

 [Decimal](https://en.wikipedia.org/wiki/Decimal)
