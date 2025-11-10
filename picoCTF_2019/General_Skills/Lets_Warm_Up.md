
## Lets Warm Up

**Platform:** picoCTF 2019

**Author:** SANJAY C/DANNY TUNITIS  

**Category:** General Skills

**Difficulty:** Easy

**Tags:** 
#picoCTF_2019 
#General_Skills 
#Easy 


---

## Description

If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

---

## Hints

Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

---

## Analysis

Based on the description, this challenge is simply about converting a hexadecimal value into its corresponding ASCII character.

---

## Methodology

**Step 1:** Copy the given hexadecimal number

`0x70`

**Step 2:** Use a converter such as **CyberChef**.

**Step 3:** In CyberChef, paste the input:

`0x70`

**Step 4:** Add the following operation to the Recipe:

- `From Hex`
    

**Step 5:** Set the delimiter to “Auto” and click **Bake**.


<img width="1101" height="327" alt="image" src="https://github.com/user-attachments/assets/f9efead7-8037-4c7f-bdb8-c942c66ba960" />


---

## Flag

picoCTF{---------}

---

## Reflection

This problem reinforces a fundamental skill in CTF challenges — understanding base conversions. Recognizing that “0x” indicates hexadecimal helps in quickly identifying that you just need to decode it to ASCII. These simple conversions often appear in more advanced cryptography or encoding challenges, making it important to master the basics early on.

---

## Tools

**CyberChef** – A web-based tool for performing a wide range of data format conversions, encodings, and decoding operations with a simple “recipe” interface.

---

## References

- [Hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal)
    
- [ASCII Table and Character Codes](https://www.asciitable.com/)
