
## CanYouSee

**Platform:** picoCTF 2024

**Author:** MUBARAK MIKAIL

**Category:** Forensics

**Difficulty:** Easy

Tags:
#picoCTF_2024 
#Forensics 
#Easy 

---

## Description

How about some hide and seek? Download this file here. 

---

## Hints
- How can you view the information about the picture?
- If something isn't in the expected form, maybe it deserves attention?

---

## Analysis

This challenge focused on inspecting an image file for hidden metadata rather than analyzing its visible content. By checking the file’s EXIF and additional metadata fields, an unusual “Attribution URL” entry appeared that wasn’t a real URL but Base64-encoded text. Decoding this string revealed the flag directly, demonstrating how metadata can hide valuable information in forensic challenges.

---

## Methodology

**Step 1:** Download the file 

**Step 2:** Unzip the file 


<img width="599" height="162" alt="image" src="https://github.com/user-attachments/assets/4c263d52-c2f8-4232-88b8-25ef03e934b5" />


**Step 3:** display the file 


<img width="1740" height="718" alt="image" src="https://github.com/user-attachments/assets/dd87f959-021f-469b-8f75-dd357d721a41" />


**Step 4:** View file metadata

<img width="678" height="522" alt="image" src="https://github.com/user-attachments/assets/710fee84-e045-4cce-8bc3-8f9e4c6f3467" />

The "Attribution URL" seems like in encrypted in Base64 let's try to decrypt it

**Step 4:** Use CyberChef

Add `From Base64` Operation 
Input: cGljb0NURntNRTc0RDQ3QV9ISUREM05fZGVjYTA2ZmJ9Cg==

<img width="1073" height="252" alt="image" src="https://github.com/user-attachments/assets/f700bb21-327e-471a-a061-c105fda41947" />

**Step 5:** Retrieve the Flag

---

## Flag

picoCTF{ME7--------06fb}

---

## Reflection

The challenge reinforced the importance of examining files beyond what is visually displayed. Metadata often contains hidden clues or embedded data, and knowing how to decode common formats like Base64 is essential. It was a simple but effective exercise in forensic investigation, reminding me to always check the “unseen” parts of a file.

---

## Tools

exiftool - Used to inspect image metadata and locate the suspicious Base64-encoded field.

CyberChef	- Decoded the Base64 string quickly using the From Base64 operation.

Unzip -	Extracted the challenge contents from the provided ZIP file.

----

## References

[ExifTool](https://exiftool.org/)

[CyberChef](https://gchq.github.io/CyberChef/)

[Base64](https://en.wikipedia.org/wiki/Base64)
