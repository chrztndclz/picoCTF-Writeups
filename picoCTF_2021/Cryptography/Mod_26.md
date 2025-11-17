
## Mod 26

**Platform:** picoCTF 2021

**Author:** PANDU

**Category:** Cryptography

**Difficulty:** Easy

Tags:
#picoCTF_2021 
#Cryptography
#Easy 

---

## Description

Cryptography can be easy, do you know what ROT13 is? cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_uJdSftmh}

---

## Hints

This can be solved online if you don't want to do it by hand!

---

## Analysis

The given cipher text uses **ROT13**, a substitution cipher that shifts each letter by 13 positions in the alphabet. Applying ROT13 twice returns the original message, so decrypting it is straightforward using online tools such as CyberChef.

---

## Methodology
**Step 1:** Copy the encryption

cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_uJdSftmh}

**Step 2:** Use a converter such as **CyberChef**.

Tools like **CyberChef** can decode ROT13 instantly.

**Step 4:** ### In CyberChef:

Paste the encrypted text into the input field.
Add the operation **ROT13** to the Recipe.


<img width="1056" height="234" alt="image" src="https://github.com/user-attachments/assets/69a8c8f8-d58e-42a7-9a3f-93fffe5430e7" />


### **Step 4:** Get the decoded output

CyberChef will automatically display the decrypted flag.


---

## Flag

picoCTF{nex--------gzu}

---

## Reflection

This challenge introduces a classic substitution cipher. ROT13 is commonly used in CTF problems and can be solved manually or with any online decoder. It reinforces understanding of basic alphabet shifts and the usefulness of tools like CyberChef for quick decryption.

---

## Tools

**CyberChef** – A web-based tool for performing a wide range of data format conversions, encodings, and decoding operations with a simple “recipe” interface.

----

## References

[CyberChef/](https://gchq.github.io/CyberChef/)
[ROT13](https://en.wikipedia.org/wiki/ROT13)
