
## Collaborative Development

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

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together? You can download the challenge files here:

    challenge.zip

---

## Hints
- git branch -a will let you see available branches
- How can file 'diffs' be brought to the main branch? Don't forget to git config!
- Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.

---

## Analysis

This challenge tested basic Git workflows, including inspecting branches, merging feature branches into main, and resolving merge conflicts manually. Each feature branch (part-1, part-2, and part-3) contributed a portion of the final flag inside flag.py. Successful completion required configuring Git user details, merging branches in sequence, manually editing conflicts, staging resolved files, and committing after each merge. The final execution confirmed the full reconstructed flag.

---

## Methodology

**Step 1:** Download the file

**Step 2:** Unzip the file 

<img width="1169" height="545" alt="image" src="https://github.com/user-attachments/assets/346b9936-6dec-47e1-8714-fef05edc64b0" />


**Step 3:** Navigate drop-in directory and print the file 


<img width="779" height="202" alt="image" src="https://github.com/user-attachments/assets/abfd56b8-9884-4108-981b-d3ccec65b482" />

**Step 4:** Add a test username and email

`git config user.name "test"
git config user.email "test@test.com"`

<img width="766" height="103" alt="image" src="https://github.com/user-attachments/assets/2787811b-5129-4f21-8473-723d925c49fd" />

**Step 5:**

`git branch -a`

<img width="775" height="127" alt="image" src="https://github.com/user-attachments/assets/c8902a64-58f0-4700-ab1a-b472fd2a60ed" />

**Step 6:** Checkout main

`git checkout main`

<img width="770" height="77" alt="image" src="https://github.com/user-attachments/assets/30718e64-4e13-40d0-b9fe-48d3139cb71c" />

**Step 7:**  Merge part 1

`git merge feature/part-1`

<img width="771" height="128" alt="image" src="https://github.com/user-attachments/assets/ad28f3b7-1bb0-4413-ab9a-de5550aa663d" />

**Step 8:** Add and commit the flag.py ofr part 1

`git add flag.py
git commit`

<img width="771" height="114" alt="image" src="https://github.com/user-attachments/assets/c19f5d5d-a125-4798-b429-6605c9a4af65" />

**Step 9:** Merge part 2

`git merge feature/part-2`

<img width="781" height="111" alt="image" src="https://github.com/user-attachments/assets/bc68a732-f677-4552-b045-cd855b4f75cf" />

**Step 10:** Add and commit the flag.py for part 2

`git add flag.py
git commit`

<img width="772" height="111" alt="image" src="https://github.com/user-attachments/assets/1783ad79-5ee1-4518-bf30-7eb2442a82b3" />

**Step 11:** Merge part 3

`git merge feature/part-3`

<img width="777" height="112" alt="image" src="https://github.com/user-attachments/assets/e41d3035-da05-4a58-bc34-b6e1ea5b5cb8" />

**Step 12:** print the flag 


<img width="766" height="145" alt="image" src="https://github.com/user-attachments/assets/24bf3d12-caf7-4df9-9c66-bd4920cf8f5e" />


---

## Flag

picoCTF{t3@--------0077}

---

## Reflection

This activity reinforced practical skills in version control, particularly conflict resolution—an essential part of collaborative development. Understanding how Git tracks changes and how multiple contributors' edits interact helped build confidence in handling real-world merge scenarios. The challenge also emphasized careful attention to diffs and deliberate conflict resolution to ensure the final output is complete and correct.

---

## Tools

Git – For branch management, merging, conflict resolution, and repository navigation

unzip – Extracted the challenge.zip contents for analysis.

----

## References

[Git Merge](https://git-scm.com/docs/git-merge)

[Git Branch](https://git-scm.com/docs/git-branch)
