## Bases

**Platform:** picoCTF 2019

**Author:** SANJAY C/DANNY T

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2019 
#General_Skills 
#Easy 

---

## Description

What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

---

## Hints
- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

---

## Analysis
The given string looks like Base64—its character set and padding-free format are typical of Base64-encoded data. Decoding it should reveal the plaintext that forms the flag.

---

## Methodology

**Step 1:** Copy the given string
bDNhcm5fdGgzX3IwcDM1

**Step 2:** Use a converter such as **CyberChef**.

**Step 3:** In CyberChef, paste the input:

**Step 3:** Add the following operation to the Recipe:

`From Base64`


<img width="782" height="260" alt="image" src="https://github.com/user-attachments/assets/3b9fa75d-1f6b-43e1-9566-78420e0c777e" />


**Step 4:** Observe the output and place it in the picoCTF flag format.

---

## Flag

picoCTF{l3a---------p35}

---

## Reflection

This challenge reinforces recognizing Base64 strings, which frequently appear in CTFs and everyday encoding scenarios. Knowing how to quickly identify Base64—based on its character patterns and length—is essential for fast decoding. Tools like CyberChef make this process effortless, but it’s equally important to understand what Base64 is and why it’s used.

---

## Tools

CyberChef (Base64 decoding)

----

## References

[Base64](https://en.wikipedia.org/wiki/Base64)

