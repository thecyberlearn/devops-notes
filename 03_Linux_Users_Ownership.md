# Linux – Users & Ownership (Day 3)

## What are Users in Linux?
Linux is a multi-user system.
Each file and process runs under a specific user.

This prevents:
- accidental damage
- security issues
- one app affecting another

---

## Why Users Matter in DevOps?
Applications **never run as root** in production.
Each service has its own user for safety.

DevOps engineers:
- create users
- assign ownership
- control access

---

## User Types
- root → superuser (full access)
- normal user → regular work
- system user → runs services (nginx, docker)

---

## Check Current User
```bash
whoami
```

## View All Users
```bash
cat /etc/passwd
```

## Create a New User
```bash
sudo useradd devuser
```

## Set password:
```bash
sudo passwd devuser
```

## Switch User
```bash
su devuser
```

## Exit user
```bash
exit
```

## Groups in Linux

Users belong to groups.
Groups help manage permissions easily.

## Check groups:

```bash
groups
```

## Add user to group:

```bash
sudo usermod -aG sudo devuser
```

## File Ownership

Each file has:

owner

group

## Check ownership:

```bash
ls -l
```

## Change Ownership (chown)
```bash
sudo chown devuser file.txt
sudo chown devuser:devuser file.txt
```

## Change Group Only
```bash
sudo chgrp devuser file.txt
```

## Real DevOps Scenario

Application folder:

owned by app user

not by root

correct permissions

Example:

```bash
sudo mkdir /var/myapp
sudo chown devuser:devuser /var/myapp
sudo chmod 755 /var/myapp
```

## Common Mistakes

Running apps as root

Wrong ownership causing permission denied

Using sudo unnecessarily

DevOps Rule

❌ root everywhere
✅ least privilege access


## Exit user:

```bash
exit
```

## Groups in Linux

Users belong to groups.
Groups help manage permissions easily.

## Check groups:

groups

## Add user to group:

sudo usermod -aG sudo devuser

## File Ownership

Each file has:

owner

group

## Check ownership:

```bash
ls -l
```

## Change Ownership (chown)
```bash
sudo chown devuser file.txt
sudo chown devuser:devuser file.txt
```

## Change Group Only
```bash
sudo chgrp devuser file.txt
```

## Real DevOps Scenario

Application folder:

owned by app user

not by root

correct permissions

Example:

sudo mkdir /var/myapp
sudo chown devuser:devuser /var/myapp
sudo chmod 755 /var/myapp

## Common Mistakes

Running apps as root

Wrong ownership causing permission denied

Using sudo unnecessarily

## DevOps Rule

❌ root everywhere
✅ least privilege access