# Linux – SSH & Remote Server Access (Day 5)

## What is SSH?
SSH (Secure Shell) is used to securely connect to a remote server.
DevOps engineers use SSH daily to manage cloud servers.

---

## Why SSH is Important for DevOps?
- Access cloud servers (AWS EC2, VPS)
- Deploy applications
- Debug production issues
- Manage configurations

No SSH = no DevOps work.

---

## Basic SSH Syntax
```bash
ssh user@server_ip
```

Example:
```bash
ssh ubuntu@13.234.56.78
```

---

## Default SSH Port
- Port 22

Custom port example:
```bash
ssh -p 2222 user@server_ip
```

---

## SSH First-Time Connection
You may see:
```
Are you sure you want to continue connecting (yes/no)?
```

Type:
```text
yes
```

---

## SSH Key-Based Authentication (VERY IMPORTANT)

Instead of passwords, DevOps uses SSH keys.

Benefits:
- More secure
- No password typing
- Required by cloud providers

---

## Generate SSH Key
```bash
ssh-keygen
```

Press Enter for defaults.

This creates:
- private key → ~/.ssh/id_rsa
- public key → ~/.ssh/id_rsa.pub

---

## Copy SSH Key to Server
```bash
ssh-copy-id user@server_ip
```

Or manually copy:
```bash
cat ~/.ssh/id_rsa.pub
```

Paste into server:
```bash
~/.ssh/authorized_keys
```

---

## Login Using SSH Key
```bash
ssh user@server_ip
```

(No password needed)

---

## SSH Config File (PRO TIP)
Create:
```bash
~/.ssh/config
```

Example:
```text
Host myserver
    HostName 13.234.56.78
    User ubuntu
    IdentityFile ~/.ssh/id_rsa
```

Now connect using:
```bash
ssh myserver
```

---

## Common SSH Commands
```bash
exit            # logout
whoami          # check user
hostname        # server name
uptime          # server running time
```

---

## Common SSH Errors
- Permission denied
- Wrong user
- Wrong key
- Port blocked by firewall

---

## DevOps Best Practices
- Disable password login
- Use key-based auth only
- Never share private key
- Use least privilege users

---

## Real DevOps Scenario
1. Create EC2 instance
2. SSH into server
3. Install Docker
4. Deploy application

SSH is the entry point.

---

## Summary
Today I learned SSH basics, key-based authentication,
and how DevOps engineers securely connect to remote servers.
