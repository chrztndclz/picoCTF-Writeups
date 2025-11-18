
## Transformation

**Platform:** picoCTF 2021

**Author:** MADSTACKS

**Category:** Reverse Engineering

**Difficulty:** Easy

Tags:
#picoCTF_2021 
#Reverse_Engineering 
#Easy 

---

## Description

I wonder what this really is... enc ''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])

---

## Hints
- You may find some decoders online

---

## Analysis

The Python code describes how the original flag was **encoded** by taking two standard 8-bit characters and **packing** them into one larger 16-bit Unicode character. The process uses a **left bit shift** (`<< 8`) to move the first character's value into the upper half and then adds the second character's value into the lower half. To solve this, we must reverse the operation: take each 16-bit character from the encoded file and **unpack** it back into its two original 8-bit characters.

---

## Methodology
**Step 1:** Obtain the Encoded String
First, you must access the provided file (usually named enc) to get the encrypted payload.


<img width="1252" height="120" alt="image" src="https://github.com/user-attachments/assets/89b8d052-63ca-4c98-be5b-579bc81708c8" />


**Step 3:** Implement the Inverse Logic in Python
Start the Python interpreter and define the encoded string. Then, execute the single-line decoder. 


<img width="1242" height="183" alt="image" src="https://github.com/user-attachments/assets/f6f1c30d-3d23-4c9b-872a-b0a69e61dfc9" />


How the Decoding Line WorksThe expression [chr(ord(c) >> 8) + chr(ord(c) & 0xFF) for c in enc_str] iterates through the packed string (enc_str) and performs two operations on the integer value of each Unicode character ord(c)):
- ord(c) >> 8 (Extracts First Character):This is the inverse of << 8. The Right Bit Shift moves the 8 bits of the first original character back to the lowest position.
- ord(c) & 0xFF (Extracts Second Character): The Bitwise AND with 0xFF (which is $11111111_2$) isolates the lower 8 bits, cleanly retrieving the second original character.
- chr(...) + chr(...): Concatenates the two resulting 8-bit values back into their readable character forms.

Step 4: **Execute the Script** Running the script reveals the flag.


---

## Flag

picoCTF{16--------f7}

---

## Reflection

This challenge is a fundamental lesson in **data packing** and **bitwise operations**. We learned that complex-looking encoding is often just a simple manipulation of bytes and bits. By recognizing that two 8-bit pieces of information were **packed** into a single 16-bit container, we knew to use the inverse operations (`>> 8` and `& 0xFF`) to **unpack** them and recover the flag.

---

## Tools

Python Interactive Shell: Used to execute the decoding logic instantly.

Bitwise Operators: >> (Right Shift) and & (Bitwise AND)

----

## References

[Python](https://en.wikipedia.org/wiki/Python)

[Bitwise Operators](https://en.wikipedia.org/wiki/Bitwise_operation)
