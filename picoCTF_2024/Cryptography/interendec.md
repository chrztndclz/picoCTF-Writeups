
## interendec

**Platform:** picoCTF 2024

**Author:** NGIRIMANA SCHADRACK

**Category:** Cryptography

**Difficulty:** Easy

Tags: 
#picoCTF_2024 
#Cryptography 
#Easy 

---

## Description

Can you get the real meaning from this file. Download the file here. 

---

## Hints
- Engaging in various decoding processes is of utmost importance

---

## Analysis

---

## Methodology

**Step 1:** download the file 

**Step 2:** use cat command to view the file 

<img width="637" height="145" alt="image" src="https://github.com/user-attachments/assets/6b062ed9-e845-440d-ba6b-7731d3666c18" />


**Step 3:** Use Cyberchef 

Add Base64 operation

Input: 
`YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyeG9OakJzTURCcGZRPT0nCg==`
Output: 
`b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ=='`


Add Base64 operation
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ=='
remove b'...'
The leading b'...' means it’s a Python bytes literal, but the contents inside the quotes is still just a Base64 string:

Input:
`d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ==`
Output: 
`wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}`


Looks like a ROT13 or Ceasar Cipher variation try different ROT13 variation

Add ROT13 operation 
Input:
wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}

Modify the amount until you get the correct format of the flag. 


<img width="935" height="246" alt="image" src="https://github.com/user-attachments/assets/1b84ff6f-07b5-4c84-ac51-872b7f4b51c8" />


**Step 4:** Retrieve the Flag

---

## Flag

picoCTF{cae---------00b}

---

## Reflection

This challenge emphasized the importance of recognizing layered encodings and testing different decoding techniques. Using CyberChef made the workflow efficient, and applying iterative reasoning helped identify when to switch from Base64 decoding to rotational ciphers. The challenge reinforces a systematic approach: decode, inspect, and repeat until meaningful output appears.

---

## Tools

CyberChef – Online tool for chaining encoding/decoding operations.

cat – Used for quickly viewing file contents.

ROT/ Caesar Cipher Decoder – For brute-force shifting to reveal readable text.

----

## References

[Base64 Info](https://en.wikipedia.org/wiki/Base64)

[Caesar Cipher](https://en.wikipedia.org/wiki/Caesar_cipher)
