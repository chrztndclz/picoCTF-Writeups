## Binary Search

**Platform:** picoCTF 2024

**Author:**  JEFFERY JOHN

**Category:** General Skills

**Difficulty:** Easy

Tags:
#picoCTF_2024 
#General_Skills 
#Easy 

---

## Description

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses. Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools! You can download the challenge files here:

    challenge.zip

Additional details will be available after launching your challenge instance.

ssh -p 59538 ctf-player@atlas.picoctf.net Using the password 1ad5be0d. Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden!

---

## Hints
- Have you ever played hot or cold? Binary search is a bit like that.
- You have a very limited number of guesses. Try larger jumps between numbers!
- The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

---

## Analysis

The challenge demonstrates how binary search efficiently narrows a large search space. With 1000 possibilities and only 10 guesses, linear guessing would fail. Using binary search, each guess halves the range, showing how algorithms optimize decision-making in cybersecurity tasks like log analysis or vulnerability scanning.

---

## Methodology
**Step 1:** Log in to ssh

ssh -p 61892 ctf-player@atlas.picoctf.net 
password: 1ad5be0d

**Step 2:** Guess the number using binary search algorithm

<img width="667" height="418" alt="image" src="https://github.com/user-attachments/assets/3a963639-88a3-4f6a-813d-f2bbe6deea3f" />


Here's the formula

`mid=left+(right−left​/2)`

Always go for the middle number

**Step 3:** Retrieve the flag

---

## Flag

picoCTF{g00--------3d18}

---

## Reflection

This task highlights the importance of efficient problem-solving. Binary search reduces guesses from 1000 to ≤10, illustrating how algorithmic thinking saves time and improves accuracy in practical cybersecurity scenarios.

---

## Tools

SSH Client – Used to securely connect to the remote challenge environment and interact with the shell.

----

## References

[Binary Search Algorithm](https://en.wikipedia.org/wiki/Binary_search_algorithm)

[SSH (Secure Shell)](https://en.wikipedia.org/wiki/Secure_Shell)
