
## Secret of the Polyglot

**Platform:** picoCTF 2024

**Author:**  SYREAL

**Category:** Forensics

**Difficulty:** Easy

Tags:
#picoCTF_2024 
#Forensics 
#Easy 

---

## Description

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file? Download the suspicious file here. 

---

## Hints

This problem can be solved by just opening the file in different ways

---

## Analysis

This challenge tests understanding of **file signatures** (magic bytes) and how some files can be crafted as **polyglots**, meaning they contain valid headers for more than one file format. By renaming the suspicious PDF to a `.jpg`, we force the system to interpret a different embedded format. Because the JPEG header is present inside the file, image viewers ignore the PDF content and render the hidden image, which contains the flag.  
The key idea: **file format ≠ file extension**—extensions are just labels, while magic bytes determine how the file is actually parsed.

---

## Methodology
**Step 1:** Download and view the suspicious PDF file.


<img width="1060" height="628" alt="image" src="https://github.com/user-attachments/assets/14e762b3-d1e9-4221-82de-4e9c7a69a48e" />


**Step 2:** Copy it as a jpg file 

cp flag2of2-final.pdf polygot.jpg

The file used in the challenge is a polyglot file—a specially crafted file that is valid in more than one format at the same time. File formats like PDF and JPEG identify themselves using “magic numbers” in their headers. The challenge creator embedded both a valid PDF header and a valid JPEG header inside the same file.

When opened as a PDF, your system reads the PDF header and interprets the file as a document.

When you rename it to .jpg, image viewers ignore the PDF structure and instead parse the JPEG header and image data hidden inside the file.

Because the hidden JPEG contains the actual flag, changing the extension forces your viewer to process a different part of the binary data, revealing the embedded image.

**Step 3:** display the image 

display polygot.jpg 


<img width="514" height="183" alt="image" src="https://github.com/user-attachments/assets/392958a9-2f4c-4088-b7c5-686a427c29ba" />


Step 4: Retrieve the flag 

---

## Flag

picoCTF{f1u--------5c0}

---

## Reflection

This challenge reinforces the importance of inspecting files beyond their extensions. It shows how attackers can hide information inside polyglot files to bypass detection. By exploring the raw structure and trying multiple formats, it becomes clear that understanding how different file headers work is crucial for digital forensics. The activity also highlights practical use of Linux tools like file, cp, and image viewers when analyzing suspicious artifacts.

---

## Tools

cp - used here to duplicate and rename the PDF as a .jpg.

display -	Image viewers used to open the renamed JPEG and reveal the hidden flag.

----

## References

[Magic bytes and file signatures](https://en.wikipedia.org/wiki/List_of_file_signatures)

[Polyglot file concept](https://en.wikipedia.org/wiki/Polyglot_(computing))
