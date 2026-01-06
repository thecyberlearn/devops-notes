# Linux – Basic Commands (Day 1)

## What is Linux?
Linux is an operating system used to run servers and applications.

## Why Linux is important for DevOps?
Most servers run on Linux, and DevOps engineers manage everything using Linux commands.

## Linux Folder Structure
- /      → root
- /home  → user files
- /etc   → configuration files
- /var   → logs and data
- /bin   → system commands

## Navigation Commands
```bash
pwd        # show current directory
ls         # list files
ls -l      # detailed list
ls -a      # show hidden files
cd folder  # move into folder
cd ..      # go back
cd ~       # go to home
```

## Create & Delete Commands
```bash
mkdir app
touch file.txt
rm file.txt
rm -r app
```

## Working with File Content
```bash
cat file.txt
head file.txt
echo "Linux for DevOps" > info.txt     # write content
echo "Day 1 completed" >> info.txt    # append content
cat info.txt                          # view file content
``` 

## Daily Useful Linux Commands
```bash
clear       # clear terminal screen
history     # show command history
whoami      # show current user
uname -a    # show system information
```



