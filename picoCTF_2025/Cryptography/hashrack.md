
## hashcrack

**Platform:** picoCTF 2025

**Author:** NANA AMA ATOMBO-SACKEY

**Category:** Cryptography

**Difficulty:** Easy

Tags:
#picoCTF_2025 
#Cryptography 
#Easy 

---

## Description

A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?

Additional details will be available after launching your challenge instance.

Access the server using nc verbal-sleep.picoctf.net 58318

---

## Hints
- Understanding hashes is very crucial. Read more here.
- Can you identify the hash algorithm? Look carefully at the length and structure of each hash identified.
- Tried using any hash cracking tools?

---

## Analysis

This challenge presents a single hash during a netcat session and asks for its corresponding password, suggesting a focus on basic hash recognition and lookup. The format strongly resembles an unsalted MD5 value, indicating that the task likely revolves around identifying the hash type and retrieving the plaintext through common cracking or reference tools.

---

## Methodology

**Step 1:** Connect to the challenge server

`nc verbal-sleep.picoctf.net 50080`


<img width="501" height="152" alt="image" src="https://github.com/user-attachments/assets/0c4d27b3-a622-4d84-8227-2a3095ff2d0b" />


**Step 2:** Analyze the Hash using CyberChef 

482c811da5d5b4bc6d497ffa98491e38


<img width="1431" height="421" alt="image" src="https://github.com/user-attachments/assets/e36aad0d-aa66-4bb9-ae28-29f2a950fec4" />


**Step 3:** Decrypt the MD5 Hash using online Hash Database to find the password 

`Hashes.com`

<img width="1571" height="371" alt="image" src="https://github.com/user-attachments/assets/1234e380-cc39-4c87-acc8-01f3e6d4226a" />


**Step 4:** Enter the password 

`password123`

<img width="707" height="222" alt="image" src="https://github.com/user-attachments/assets/c47d2246-ef04-4127-8d7e-90cbc267f3c3" />


**Step 5:** Analyze the Hash using CyberChef 

b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3

<img width="1452" height="419" alt="image" src="https://github.com/user-attachments/assets/f15629de-2126-42eb-800f-a7d6b14a6a67" />

**Step 6:** Decrypt the SHA-1 Hash using online Hash Database to find the password 

`Hashes.com`

<img width="1582" height="384" alt="image" src="https://github.com/user-attachments/assets/9960cff5-c070-420f-853b-9bdc45279b5e" />

**Step 7:** Enter the password 

`letmein`

<img width="800" height="300" alt="image" src="https://github.com/user-attachments/assets/a2003180-0ba6-46e1-8fca-87ed2284d3e3" />

**Step 8:** Analyze the Hash using CyberChef 

916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745

<img width="1428" height="487" alt="image" src="https://github.com/user-attachments/assets/d367b566-f8a4-4e33-94c1-e284a73500de" />

**Step 9:** Decrypt the SHA-256 Hash using online Hash Database to find the password 

`Hashes.com`

<img width="1592" height="378" alt="image" src="https://github.com/user-attachments/assets/ad8ac56c-9841-4bfd-a943-e964911974ce" />

**Step 10:** Enter the password 

`qwerty098`

<img width="779" height="279" alt="image" src="https://github.com/user-attachments/assets/e0f8c4e6-25cb-41cb-87df-735c5cf0f857" />


---

## Flag

picoCTF{Use---------69f}

---

## Reflection

This challenge reinforced the importance of recognizing hash formats quickly and understanding how weak, unsalted hashing leaves passwords vulnerable to simple lookups. By using tools like CyberChef and online hash databases, it became clear how easily common passwords can be recovered, highlighting why secure hashing practices—such as salting, stretching, and stronger algorithms—are essential in real-world systems.

---

## Tools

CyberChef – Used to identify hash types and inspect hash characteristics.

Hashes.com – Online database used to look up and crack weak unsalted hashes.

netcat (nc) – Used to connect to the remote challenge server and interact with the prompts.

----

## References

[CyberChef](https://gchq.github.io/CyberChef/)

[Hashes.com](https://hashes.com/en/decrypt/hash)

[Netcat reference](https://nc110.sourceforge.net/)
