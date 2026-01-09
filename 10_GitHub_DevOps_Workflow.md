# GitHub – DevOps Workflow (Day 10)

## What is GitHub?
GitHub is a cloud platform to host Git repositories.
It allows teams to collaborate, review code, and trigger CI/CD pipelines.

DevOps engineers use GitHub daily.

---

## Why GitHub is Important for DevOps?
- Central code storage
- Team collaboration
- CI/CD integration
- Code reviews and approvals

---

## Create GitHub Account
Go to https://github.com and create a free account.

---

## Connect Local Repository to GitHub

Create a new repository on GitHub (do NOT add README).

Then run:
```bash
git remote add origin https://github.com/username/repo-name.git
```

Verify:
```bash
git remote -v
```

---

## Push Code to GitHub
```bash
git push -u origin main
```

---

## Clone a Repository
```bash
git clone https://github.com/username/repo-name.git
```

---

## Pull Latest Changes
```bash
git pull origin main
```

---

## GitHub DevOps Workflow
1. Create feature branch
2. Push branch to GitHub
3. Open Pull Request
4. Code review & approval
5. Merge to main
6. CI/CD deploys automatically

---

## Pull Requests (PR)
A Pull Request is a request to merge code into the main branch.
Used for safe deployments and team collaboration.

---

## Real DevOps Scenario
Multiple developers working together:
- Everyone works on own branch
- PRs ensure stability
- CI checks before merge

---

## Common Mistakes
- Pushing directly to main
- Not pulling latest changes
- Ignoring PR reviews

---

## DevOps Rule
✅ Always use Pull Requests  
❌ Never push directly to main

---

## Summary
Today I learned GitHub basics for DevOps including clone, push, pull,
and Pull Request workflow used in real companies.
