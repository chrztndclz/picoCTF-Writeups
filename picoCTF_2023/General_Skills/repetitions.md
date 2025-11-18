
## repetitions

**Platform:** picoCTF 2023

**Author:** THEONESTE BYAGUTANGAZA

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2023
#General_Skills 
#Easy 

---

## Description

Can you make sense of this file? Download the `file` here.

---

## Hints
- Multiple decoding is always good.

---

## Analysis

The file contains a message that has been encoded multiple times using Base64. Each time you decode it, you reveal a new layer until the final readable flag appears. The key is to recognize that it’s nested encoding and to decode step by step until you reach the end.

---

## Methodology
**Step 1:** Download the File 
**Step 2:** Access the file using cat command

VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZhTTBKUFdXdGtlbVF4V2tkWGJYUllDbUY2UWpSWmEyaFRWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==

**Step 3:**  use cyberchef

Step 4: First Decode

Input:
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZhTTBKUFdXdGtlbVF4V2tkWGJYUllDbUY2UWpSWmEyaFRWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==

Operation: from base64 

Ouput: 
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlVaM0JPWWtkemQxWkdXbXRYCmF6QjRZa2hTVjJGdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==


Step 5: Second Decode

Input: 
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlVaM0JPWWtkemQxWkdXbXRYCmF6QjRZa2hTVjJGdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==

Operation: from base64 

Output: 
V1RCa2MyRnRTWGRVYkZaVFltNVNjRmRXYUU5aVJUVnhWVzFhYVdGck5UWmFSVkpQWVRGbmVWVnVR
bHBsYTBweVUxWmpNRTVHWjNsVgpXR1JyVFdwV2VsUlZVbE5oTURCNVZXMWFUZ3BOYkdzd1ZGWmtX
azB4YkhSV2FteEVXbm93T1VOblBUMEsK


Step 6: Third Decode

Input: 
V1RCa2MyRnRTWGRVYkZaVFltNVNjRmRXYUU5aVJUVnhWVzFhYVdGck5UWmFSVkpQWVRGbmVWVnVR
bHBsYTBweVUxWmpNRTVHWjNsVgpXR1JyVFdwV2VsUlZVbE5oTURCNVZXMWFUZ3BOYkdzd1ZGWmtX
azB4YkhSV2FteEVXbm93T1VOblBUMEsK

Operation: from base64 

Output: 
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aTgpNbGswVFZkWk0xbHRWamxEWnowOUNnPT0K


Step 7: Forth Decode

Input: 
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aTgpNbGswVFZkWk0xbHRWamxEWnowOUNnPT0K

Operation: from base64 

Output: 
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZN
Mlk0TVdZM1ltVjlDZz09Cg==


Step 8: Fifth Decode

Input: 
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZN
Mlk0TVdZM1ltVjlDZz09Cg==

Operation: from base64 

Output: 
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfM2Y4MWY3YmV9Cg==


Step 8: Sixth Decode

Input: 
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfM2Y4MWY3YmV9Cg==

Operation: from base64 

Output: 
picoCTF{}

---

## Flag

picoCTF{bas---------7be}

---

## Reflection

This challenge shows how important it is to recognize repeatedly encoded data. Even if the text looks unreadable, applying multiple layers of decoding—especially Base64—often reveals the real message. It’s a good reminder that in CTFs, encoded data is rarely encoded only once, so trying repeated decoding is a simple but effective strategy.

---

## Tools

cat – Used to display the contents of the downloaded file.

CyberChef – A powerful online tool for decoding and analyzing data.

Base64 Decoder – Built into CyberChef, used repeatedly to decode each layer.

----

## References
[Base64](https://developer.mozilla.org/en-US/docs/Glossary/Base64)

[CyberChef](https://gchq.github.io/CyberChef/)

[cat](https://linux.die.net/man/1/cat)
