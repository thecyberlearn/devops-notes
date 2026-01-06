# Linux – File Permissions (Day 2)

## What are File Permissions?
File permissions control **who can read, write, or execute** a file or folder in Linux.

They protect the system from:
- accidental deletion
- unauthorized access
- hacking

---

## Why Permissions are Important for DevOps?
DevOps engineers manage **live servers**.
Wrong permissions can:
- break applications
- expose data
- allow hackers access

So permissions are **critical**.

---

## Permission Types

There are 3 permissions:

- r → read
- w → write
- x → execute

---

## Permission Groups

Permissions are set for 3 types of users:

- u → user (owner)
- g → group
- o → others

Order is always:

## user | group | others

---

## Checking Permissions

```bash
ls -l
-rwxr-xr--
Meaning:

user → rwx

group → r-x

others → r--

Add values to set permissions.

Examples:

7 = rwx (4+2+1)

6 = rw- (4+2)

5 = r-x (4+1)

4 = r--
```

---

## Setting Permissions

```bash
chmod 755 file.txt
```

Meaning:

user → 7 (rwx)

group → 5 (r-x)

others → 5 (r-x)

## Symbolic Method

```bash
chmod u+x file.sh
chmod g-w file.sh
chmod o+r file.sh
```

## Common Permission Examples

```bash
chmod 755 file.txt
chmod 644 file.txt
chmod 777 file.txt
chmod 666 file.txt
chmod 700 file.txt
chmod 600 file.txt
```

## Execute Permission (Very Important)

To run a script:

```bash
./script.sh
```


If permission denied:

```bash
chmod +x script.sh
```

## Folder Permissions Rule

```bash
r → list files
w → create/delete files
x → enter folder
```

    Without x, you cannot cd into folder.

## Execute Permission (Very Important)

To run a script:

```bash
./script.sh
```


If permission denied:

```bash
chmod +x script.sh
```

## Folder Permissions Rule

```bash
r → list files

w → create/delete files

x → enter folder
```
Without x, you cannot cd into folder.


## Mini Practice Task

```bash
mkdir test
touch test/app.sh
ls -l test
chmod 755 test/app.sh
ls -l test
```

## Common Mistakes

- Giving 777 permissions (very dangerous)
- Not understanding folder execute permission
- Changing permissions blindly on production servers


## Changing Ownership

To change the owner of a file:
```bash
sudo chown username file.txt
```

To change both owner and group:
```bash
sudo chown username:groupname file.txt
```

To change the group ownership:
```bash
sudo chgrp groupname file.txt
```

## Recursive Changes
Apply permissions or ownership to a directory and all its contents:
```bash
chmod -R 755 folder_name/
chown -R username:groupname folder_name/
```

## Checking Current Permissions
To see detailed permissions for all files in a directory:
```bash
ls -la
```

