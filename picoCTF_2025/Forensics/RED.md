
## RED

**Platform:** picoCTF 2025

**Author:** SHUAILIN PAN (LECONJUROR)

**Category:** Forensics

**Difficulty:**  Easy

Tags:
#picoCTF_2025 
#Forensics 
#Easy 

---

## Description

RED, RED, RED, RED Download the image: red.png

---

## Hints

- The picture seems pure, but is it though?
- Red?Ged?Bed?Aed?
- Check whatever Facebook is called now.

---

## Analysis

This challenge focuses on image metadata and pixel-level analysis. The file contains intentional redaction using solid red pixels, but instead of removing data, the red layer encodes hidden text directly in the RGB values.

---

## Methodology

**Step 1:** Download the png file

**Step 2:** Check the file 

<img width="573" height="79" alt="image" src="https://github.com/user-attachments/assets/f93b9b04-58ca-43fd-b7a9-978594d61e1b" />

**Step 3:** Display file

<img width="1185" height="384" alt="image" src="https://github.com/user-attachments/assets/fe33c49b-d3da-4021-bc2f-8a233db353a5" />

**Step 4:** Check metadata because of the hint "Facebook" which relate meta

exiftool red.png      

<img width="562" height="456" alt="image" src="https://github.com/user-attachments/assets/79baf980-4d90-429c-84fa-2575e4154367" />

You can see that there's a poem. 

Crimson heart, vibrant and bold,.Hearts flutter at your sight..Evenings glow softly red,.Cherries burst with sweet life..Kisses linger with your warmth..Love deep as merlot..Scarlet leaves falling softly,.Bold in every stroke.

Taking the first letter of each line:

```
C
H
E
C
K
L
S
B
```

This directly confirms that the hidden data is inside the PNG’s Least Significant Bits (LSB).

Running zsteg on the red image reveals the hidden flag.

Step 5: Run zsteg.


<img width="1915" height="324" alt="image" src="https://github.com/user-attachments/assets/fa47ab6b-8616-4978-9e39-66addb3af749" />


`cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==`

Step 6: Use Cyberchef and Convert this from Base64 


<img width="1209" height="252" alt="image" src="https://github.com/user-attachments/assets/9c26de8a-b917-4526-ac33-22ad625197eb" />


---

## Flag

picoCTF{r3d----------355_}

---

## Reflection

This challenge reinforces the idea that redaction does not equal deletion. Many real-world data leaks come from improper masking techniques where sensitive content is visually hidden but technically still present in metadata or pixel values.
It’s a reminder that forensics requires checking every data layer and never trusting what appears on the surface.

The challenge also introduces or reinforces LSB steganography concepts and encourages experimenting with tools like zsteg and Python image parsing.

---

## Tools

zsteg - A steganography analysis tool specialized for PNG and BMP, used to extract hidden data from pixel channels.

exiftool- Metadata extractor for images; used to inspect EXIF, comments, and embedded info that may hide clues.

CyberChef	- A web-based data transformation toolkit used for decoding (Base64, hex), conversion, and analysis.

----

## References

[zsteg](https://github.com/zed-0xff/zsteg)

[Base64 decoder](https://gchq.github.io/CyberChef/)

