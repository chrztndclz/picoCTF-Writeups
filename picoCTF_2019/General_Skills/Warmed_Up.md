# Warmed Up

**Platform:** picoCTF 2019
**Author:** SANJAY C / DANNY TUNITIS  
**Category:** General Skills  
**Difficulty:** Easy

---

## Description
What is 0x3D (base 16) in decimal (base 10)?

---

## Hints
Submit your answer in our flag format. For example, if your answer was '22', you would submit 'picoCTF{22}' as the flag.

---
## Analysis

The challenge asks to convert `0x3D` from hexadecimal (base 16) to decimal (base 10).  
We can solve this using any base conversion tool or manually by calculating the equivalent decimal value of the hexadecimal number.

---

## Methodology
**Step 1:** Copy the given hexadecimal number

`0x3D`

**Step 2:** Use a base converter such as **CyberChef**.

**Step 3:** In CyberChef, paste the input:

`0x3D`

**Step 4:** Add the following operations to the Recipe:

1. `From Base`
    
2. `To Base`
    

**Step 5:** Configure the **“From Base”** operation:

- Base: `16`
    

**Step 6:** Configure the **“To Base”** operation:

- Base: `10`

<img width="955" height="697" alt="image" src="https://github.com/user-attachments/assets/a9e42347-1d34-4cea-8928-0f1ad036a88c" />

**Step 7:** View the output.  

---

## Flag
picoCTF{6'REDACTED'}

---

## Reflection
This challenge was a simple warm-up exercise that helped reinforce the concept of number base conversions.  
It demonstrates the importance of understanding how different numeral systems work—especially when dealing with low-level programming, data representation, or cryptography.  
Tools like CyberChef make such conversions quick and reliable, but knowing how to do them manually strengthens problem-solving fundamentals.

---

## Tools

[CyberChef](https://gchq.github.io/CyberChef/)

----

## References

[“Hexadecimal”](https://en.wikipedia.org/wiki/Hexadecimal?) 
[“Decimal”](https://en.wikipedia.org/wiki/Decimal) 
[“Base Conversion Method”](https://www.mathsisfun.com/base-conversion-method.html?) 
[“CyberChef – Data decoding made easy”](https://www.csnp.org/post/cyberchef-data-decoding-made-easy?) 
