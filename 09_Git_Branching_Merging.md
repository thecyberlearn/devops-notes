# Git – Branching & Merging (Day 9)

## Why Branching is Important?
Branching allows teams to:
- work on features safely
- fix bugs without breaking main code
- collaborate without conflicts

DevOps uses branching DAILY.

---

## What is a Branch?
A branch is a separate line of development.

Main branch = stable production code  
Feature branch = new changes

---

## View Branches
```bash
git branch
```

---

## Create a New Branch
```bash
git branch feature-login
```

Switch to branch:
```bash
git checkout feature-login
```

Shortcut (create + switch):
```bash
git checkout -b feature-login
```

---

## Check Current Branch
```bash
git branch
```
(* shows active branch)

---

## Make Changes in Branch
```bash
echo "Login feature" >> login.txt
git add .
git commit -m "add login feature"
```

---

## Merge Branch into Main
Switch to main:
```bash
git checkout main
```

Merge:
```bash
git merge feature-login
```

---

## Delete Branch (After Merge)
```bash
git branch -d feature-login
```

---

## Merge Conflicts (Important)
Occurs when same file is changed in two branches.

Git will stop and ask you to fix manually.

Steps:
1. Open conflicted file
2. Fix content
3. Save file
4. Add & commit

```bash
git add .
git commit -m "resolve merge conflict"
```

---

## Real DevOps Scenario
Problem: Multiple developers pushing code

Solution:
- Each dev uses own branch
- Merge after testing

---

## Common Mistakes
- Working directly on main
- Not pulling latest code
- Deleting branch before merge

---

## DevOps Rule
✅ One feature = one branch  
❌ Direct commits to main

---

## Summary
Today I learned Git branching, merging, and conflict handling.
This is essential for DevOps collaboration.
