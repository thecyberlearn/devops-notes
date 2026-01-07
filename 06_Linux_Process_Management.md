# Linux – Process Management (Day 6)

## What is a Process?
A process is a running program in Linux.
Every application or service runs as a process.

---

## Why Process Management is Important for DevOps?
DevOps engineers must:
- check if an app is running
- monitor CPU and memory usage
- stop or restart stuck applications

Most production issues are process-related.

---

## View Running Processes

### ps command
```bash
ps
ps aux
```

a → all users  
u → user format  
x → background processes

---

## top Command
Shows live CPU and memory usage.

```bash
top
```

Exit:
```bash
q
```

---

## htop (If Installed)
Better version of top.

```bash
htop
```

---

## Find Process by Name
```bash
ps aux | grep nginx
```

---

## Kill a Process

### Normal kill
```bash
kill PID
```

### Force kill (DANGEROUS)
```bash
kill -9 PID
```

⚠️ Use kill -9 only if normal kill fails.

---

## Kill by Process Name
```bash
pkill nginx
```

---

## Background & Foreground Jobs

Run in background:
```bash
command &
```

Example:
```bash
sleep 100 &
```

View jobs:
```bash
jobs
```

Bring to foreground:
```bash
fg
```

---

## Check Process Using a Port
```bash
sudo netstat -tulnp
```
or
```bash
sudo ss -tulnp
```

---

## Real DevOps Scenario
Problem: App not responding

Steps:
1. Check if process is running
2. Check CPU/memory usage
3. Restart process

Commands:
```bash
ps
top
kill
```

---

## Common Mistakes
- Killing wrong PID
- Using kill -9 unnecessarily
- Not checking process owner

---

## DevOps Rule
✅ Inspect first  
❌ Kill blindly

---

## Summary
Today I learned Linux process management using ps, top, kill,
and background jobs. These skills are essential for production servers.
