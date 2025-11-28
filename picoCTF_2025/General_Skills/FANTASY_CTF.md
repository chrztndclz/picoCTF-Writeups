
## FANTASY CTF

**Platform:** picoCTF 2025

**Author:** SYREAL

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2025 
#General_Skills 
#Easy 

---

## Description

Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF.

Additional details will be available after launching your challenge instance.

---

## Hints
- When a choice is presented like (a/b/c), choose one, for example: c and then press Enter.

---

## Analysis

This introductory challenge acts as a tutorial for navigating picoCTF challenges via netcat. There is no exploitation or special parsing required — the objective is simply to interact with the terminal application correctly, read the prompts carefully, and advance the story until the flag appears.

---

## Methodology

**Step 1:** Connect to the program

nc verbal-sleep.picoctf.net 59537


<img width="648" height="246" alt="image" src="https://github.com/user-attachments/assets/2d9e261b-5a71-4d00-bc0b-544437e4a659" />


Just follow the lore and keep pressing enter unless a questions pops up

**Step 2:** Registration Page

<img width="620" height="231" alt="image" src="https://github.com/user-attachments/assets/30945141-93d0-4d6d-8b99-b48c24e955b2" />

Just follow the lore and keep pressing enter unless a questions pops up

**Step 3:** Play the game 

<img width="585" height="157" alt="image" src="https://github.com/user-attachments/assets/a8e611f6-0709-4cd5-be01-134b75c98214" />


Just follow the lore and keep pressing enter until you find the flag
---

## Flag

picoCTF{m11---------572}

---

## Reflection

This challenge reinforces familiarity with terminal-based interactions, a crucial skill for many picoCTF categories including binary exploitation, forensics, and general scripting. Although simple, it trains the player to read prompts closely and respond correctly — habits essential for more complex challenges.

---

## Tools

nc (netcat) - Used to connect to the remote server hosting the challenge. Enables interactive terminal communication.

----

## References

[Netcat Manual](https://nc110.sourceforge.io/)
