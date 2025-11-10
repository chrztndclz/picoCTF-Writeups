## vault-door-training

**Platform:** picoCTF 2019

**Author:**  MARK E. HAASE

**Category:**  Reverse Engineering 

**Difficulty:** Easy

Tags:
#picoCTF_2019 
#Reverse_Engineering 
#Easy 

---

## Description
Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility. The source code for the training vault is here: VaultDoorTraining.java

---

## Hints
The password is revealed in the program's source code.

---

## Analysis

Base on the description this is a series of challenges and here we just have the training. All we need to do is to access and open the file to view the source code because password for the training vault is just in the source code. 


---

## Methodology
**Step 1:** Download the Java File 

**Step 2:** Open the file
Use a text editor like `nano` to view the source code:


<img width="626" height="54" alt="image" src="https://github.com/user-attachments/assets/7fa4747f-d389-422d-b3d5-4526648c5a40" />


**Step 3:** Inspect the Source Code 
Look through the Java file for any lines that define or return a password.


<img width="693" height="499" alt="image" src="https://github.com/user-attachments/assets/c28dc61c-d9bc-427a-8f8f-7f72ec282333" />


Step 4: Retrieve the Flag

---

## Flag

picoCTF{w4r----------713}

---

## Reflection
This challenge serves as an introduction to **reverse engineering source code**.  
It demonstrates how reading and analyzing simple program logic can reveal hardcoded secrets — a common pattern in beginner-level reverse engineering and CTF puzzles.

---

## Tools

- **Nano** – Terminal text editor for inspecting the `.java` file.
- (Alternative tools: `cat`, `vim`, or `VS Code`)

----

## References

- [GNU Nano Manual](https://www.nano-editor.org/docs.php) 
