# What's a net cat?

**Platform:** picoCTF 2019

**Author:**  SANJAY C/ DANNY TUNITIS

**Category:** General Skills

**Difficulty:** Easy

**Tags:**
#picoCTF_2019 
#General_Skills 
#Easy 


---

## Description
Using netcat (nc) is going to be pretty important. Can you connect to jupiter.challenges.picoctf.org at port 64287 to get the flag?

---

## Hints
nc tutorial

---

## Analysis

The challenge gives us a **hostname** and a **port number**.  
Netcat is a simple command-line tool that lets you open TCP or UDP connections and communicate directly with a server — like a manual way to “talk” to services on specific ports.

By connecting to the given server and port, we can receive the hidden flag from the challenge service.


---

## Methodology

**Step 1:** Open your terminal in Kali Linux (or any Linux/macOS system).

**Step 2:** Check the `nc` command syntax and options with:

<img width="627" height="565" alt="image" src="https://github.com/user-attachments/assets/d4c0e35e-9fe4-4416-8ad9-a5e99122e282" />


This prints a short help message showing the available flags on your installed `nc` variant (useful because implementations differ: `netcat-traditional`, `netcat-openbsd`, or `ncat`).

**Step 3:** Use `nc` to connect to the provided host and port:

<img width="356" height="44" alt="image" src="https://github.com/user-attachments/assets/21501981-9a2a-45bc-9c8a-2eccc40ce1d2" />

**Step 4:** After connecting, read the output sent by the server — it contains the flag.

---

## Flag

picoCTF{nEtCat----------284be8f7}


---

## Reflection
This challenge is a hands-on intro to **netcat**, a valuable tool for debugging and interacting with network services. Running `nc -h` first helps you confirm which flags and behaviors your installed version supports before you connect.

---

## Tools

Netcat (nc) - A command-line utility for reading from and writing to network connections using TCP or UDP.


----

## References

[Netcat (Kali Linux Docs)](https://www.kali.org/tools/netcat/)



