# Git – Basics for DevOps (Day 8)

## What is Git?
Git is a version control system.
It helps you track changes in code and collaborate safely.

DevOps engineers use Git DAILY.

---

## Why Git is Important for DevOps?
- Track code changes
- Collaborate with teams
- Rollback broken deployments
- CI/CD depends on Git

---

## Install Git
```bash
git --version
```

If not installed:
```bash
sudo apt install git
```

---

## Configure Git (One-time Setup)
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Check config:
```bash
git config --list
```

---

## Create a Git Repository
```bash
mkdir devops-project
cd devops-project
git init
```

---

## Git Workflow (Basic)
1. Modify files
2. Stage changes
3. Commit changes

---

## Check Repository Status
```bash
git status
```

---

## Add Files to Staging
```bash
git add file.txt
```

Add all files:
```bash
git add .
```

---

## Commit Changes
```bash
git commit -m "Initial commit"
```

---

## View Commit History
```bash
git log
```

Short view:
```bash
git log --oneline
```

---

## Check File Differences
```bash
git diff
```

---

## Undo Changes (Basic)

Undo unstaged changes:
```bash
git checkout -- file.txt
```

---

## Real DevOps Scenario
Problem: New code broke production

Solution:
1. Check commit history
2. Roll back to stable commit

Git saves lives in production.

---

## Common Mistakes
- Committing without message
- Forgetting git add
- Working directly on main branch

---

## DevOps Rule
✅ Commit small changes  
❌ Commit everything at once

---

## Summary
Today I learned Git basics: init, add, commit, status, and log.
These are core DevOps skills.
