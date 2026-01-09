# Linux – Logs & Disk Management (Day 7)

## Why Logs Are Important in DevOps?
Logs tell you:
- what happened
- when it happened
- why something failed

In production, logs are the FIRST place to check.

---

## Log Directory
Most Linux logs are stored here:
```bash
/var/log
```

List log files:
```bash
ls /var/log
```

Common logs:
- syslog
- auth.log
- kern.log
- boot.log

---

## View Log Files

### cat (small files)
```bash
cat /var/log/syslog
```

### less (recommended)
```bash
less /var/log/syslog
```

Navigation:
- Up / Down arrows
- q → quit

---

## Live Log Monitoring
```bash
tail -f /var/log/syslog
```

Very useful when debugging live issues.

---

## Search Inside Logs
```bash
grep error /var/log/syslog
```

Case-insensitive:
```bash
grep -i error /var/log/syslog
```

---

## Disk Space Management

### Check Disk Usage
```bash
df -h
```

---

### Check Folder Size
```bash
du -sh /var/log
```

---

### Find Large Files
```bash
du -ah / | sort -rh | head -10
```

⚠️ Use carefully (may need sudo)

---

## Clear Log Files (Safe Method)
```bash
sudo truncate -s 0 /var/log/syslog
```

❌ Do NOT delete system log files blindly.

---

## Real DevOps Scenario
Problem: Server disk full

Steps:
1. Check disk usage
2. Identify large directories
3. Clear old logs safely

Commands:
```bash
df -h
du -sh
tail -f
```

---

## Common Mistakes
- Deleting log files directly
- Ignoring disk alerts
- Not monitoring log growth

---

## DevOps Rule
✅ Monitor logs regularly  
❌ Ignore disk usage

---

## Summary
Today I learned Linux log monitoring and disk management.
These skills are critical for production troubleshooting.
