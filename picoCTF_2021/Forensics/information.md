## information

**Platform:** picoCTF 2021

**Author:** SUSIE

**Category:** Forensics 

**Difficulty:** Easy

Tags:
#picoCTF_2021 
#Forensics 
#Easy 

---

## Description
Files can always be changed in a secret way. Can you find the flag? cat.jpg

---

## Hints
- Look at the details of the file
- Make sure to submit the flag as picoCTF{XXXXX}

---

## Analysis
This challenge is about discovering **hidden information inside a file’s metadata**.  
Metadata stores details like author, license, timestamps, and more. Since the description suggests something is hidden, we can assume the flag is stored in the image’s metadata — possibly encoded in Base64.

---

## Methodology
**Step 1:** Download the file `cat.jpg`. 
**Step 2:** Inspect the image metadata using the `exiftool` command:

exiftool cat.jpg

**Step 3:** Review the metadata output.  
You’ll notice a suspicious “License” field containing a Base64-encoded string.


<img width="637" height="575" alt="image" src="https://github.com/user-attachments/assets/0de20948-6795-4e52-acd7-bad4cedfd8de" />


**Step 4:** Decode the Base64 text using CyberChef

- In CyberChef, paste the Base64 string.
- Add the operation `From Base64` to your recipe.


<img width="974" height="298" alt="image" src="https://github.com/user-attachments/assets/253f15d3-5ade-4ed0-9f36-af4957272112" />


**Step 5:** Once decoded, the text reveals the hidden flag.

---

## Flag

picoCTF{the_m3tadata_1s_modified}

picoCTF{the----------fied}

---

## Reflection
This challenge demonstrates how data can be hidden in plain sight using **metadata manipulation**.  
It teaches the importance of checking not just the visible content of files but also their internal properties. In digital forensics, tools like `exiftool` are essential for uncovering clues that are invisible to normal inspection.

---

## Tools

exiftool - A command-line tool used to read, write, and edit metadata in image, audio, and video files.

CyberChef - A web-based tool for encoding, decoding, and analyzing data formats (e.g., Base64, Hex, etc.).

----

## References

[ExifTool](https://exiftool.org/)

[What is Metadata?](https://www.nist.gov/publications/metadata-basics)

[CyberChefe](https://gchq.github.io/CyberChef/)

