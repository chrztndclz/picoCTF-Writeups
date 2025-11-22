
## Scan Surprise

**Platform:** picoCTF 2024

**Author:**  JEFFERY JOHN

**Category:** Forensics

**Difficulty:** Easy

Tags:
#picoCTF_2024
#Forensics 
#Easy 

---

## Description

I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead? You can download the challenge files here:

    challenge.zip

Additional details will be available after launching your challenge instance.

---

## Hints
- QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
- Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11
- If you don't have access to a phone, you can also use zbar-tools to convert an image to text

---

## Analysis

This challenge provides an image file that contains a QR code instead of a text-based flag. QR codes can encode text, URLs, or other data in a scannable format. The task is to extract the hidden information from the QR code, either using a mobile device or a command-line tool like zbar-tools. The challenge tests your ability to recognize non-traditional flag formats and use basic forensic tools to retrieve hidden information.

---

## Methodology
**Step 1:** Download the file

**Step 2:** Unzip the file 


<img width="634" height="106" alt="image" src="https://github.com/user-attachments/assets/6f3bb04d-c98c-493c-ab1b-b5666cec8bf4" />


**Step 3:** Navigate file 


<img width="633" height="455" alt="image" src="https://github.com/user-attachments/assets/6c08db45-2dca-4da6-bfa6-c7f7e5d9519c" />


**Step 4:** Display the file


<img width="574" height="43" alt="image" src="https://github.com/user-attachments/assets/792b5f5f-0e48-4b1c-9524-a5ca7cb631f6" />


**Step 5:** Scan the file zbar-tools


<img width="569" height="47" alt="image" src="https://github.com/user-attachments/assets/9fe6c469-6353-41f6-9b31-e2fa6d4918ff" />


---

## Flag

picoCTF{p33---------77c}

---

## Reflection

This task highlights how information can be concealed in images using QR codes, a common technique in digital forensics and cybersecurity. It demonstrates the value of thinking beyond plain text and using available tools to decode hidden data. Simple utilities like zbar-tools make it easy to extract the encoded information, reinforcing the importance of versatility in forensic analysis.

---

## Tools

zbar-tools – Command-line tool to scan QR codes from images.

unzip – Extracts files from compressed archives.

ls / cd – Navigate directories and list contents.

cat / display – View file content or images.

----

## References

[ZBar QR Code Scanner](https://zbar.sourceforge.net/)

[QR Code](https://en.wikipedia.org/wiki/QR_code)
