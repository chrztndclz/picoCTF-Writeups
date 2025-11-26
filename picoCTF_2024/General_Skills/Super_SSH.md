
## Title

**Platform:** picoCTF 2024

**Author:** JEFFERY JOHN

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2024 
#General_Skills 
#Easy 

---

## Description

Using a Secure Shell (SSH) is going to be pretty important.

Additional details will be available after launching your challenge instance.

Using a Secure Shell (SSH) is going to be pretty important. Can you ssh as ctf-player to titan.picoctf.net at port 62426 to get the flag? You'll also need the password 6abf4a82. If asked, accept the fingerprint with yes. If your device doesn't have a shell, you can use: https://webshell.picoctf.org If you're not sure what a shell is, check out our Primer: https://primer.picoctf.com/#_the_shell

---

## Hints
- https://linux.die.net/man/1/ssh
- You can try logging in 'as' someone with )(user)@titan.picoctf.net
- How could you specify the port?
- Remember, passwords are hidden when typed into the shell

---

## Analysis

This challenge focuses on using SSH to remotely access a server. The goal is simply to connect to a specific host using a given username, port, and password. Once authenticated, the flag is printed immediately upon login. This exercise reinforces understanding of SSH basics, including specifying ports and handling remote authentication.

---

## Methodology
**Step 1:** log in to SSH 

`ssh -p 62426 ctf-player@titan.picoctf.net`

<img width="790" height="157" alt="image" src="https://github.com/user-attachments/assets/41b5904e-ade9-4ae4-a8cc-156f2a1fbb95" />

**Step 2:** Retrieve the flag 

---

## Flag

picoCTF{s3c---------106}

---

## Reflection

This challenge demonstrates how essential SSH is for remote access and system management. By specifying a custom port and authenticating with the provided credentials, it becomes clear how secure remote communication works. It also highlights that SSH hides password input for security and emphasizes familiarity with basic command-line operations for connecting to remote systems.

---

## Tools

ssh – A secure shell client used to remotely access servers. It allows specifying ports, usernames, and host addresses to authenticate and retrieve information.

----

## References

[SSH Manual](https://linux.die.net/man/1/ssh)
