# 🐧 Linux - Complete Beginner's Guide

## What is Linux?

Linux is a **free**, **open-source**, and **Unix-like operating system** created by **Linus Torvalds** in 1991. It is one of the most reliable, secure, and widely used operating systems in the world.

Linux is used in:

- Personal Computers
- Servers
- Cloud Computing
- Android Smartphones
- Supercomputers
- Embedded Systems
- IoT Devices
- Networking Equipment

---

# Features of Linux

- Open Source
- Multiuser Operating System
- Multitasking
- Highly Secure
- Stable and Reliable
- Portable
- Fast Performance
- Command Line Interface (CLI)
- Graphical User Interface (GUI)
- Supports Multiple File Systems

---

# Advantages of Linux

- Free to use
- Secure from most viruses
- Highly customizable
- Excellent performance
- Large community support
- Stable for servers
- Efficient resource management
- Suitable for programming and development

---

# Linux Architecture

```
User
   │
Applications
   │
Shell (Bash)
   │
Linux Kernel
   │
Hardware
```

### Components

### 1. Kernel
The kernel is the core of Linux. It manages CPU, memory, devices, and processes.

### 2. Shell
The shell is a command interpreter that accepts user commands and communicates with the kernel.

### 3. File System
Linux stores everything as files.

### 4. Applications
Programs such as browsers, editors, compilers, and media players.

---

# Linux Directory Structure

| Directory | Purpose |
|------------|---------|
| / | Root directory |
| /home | User files |
| /root | Root user's home |
| /bin | Essential commands |
| /sbin | System commands |
| /etc | Configuration files |
| /usr | User programs |
| /var | Log and variable files |
| /tmp | Temporary files |
| /dev | Device files |
| /proc | Process information |
| /boot | Boot files |
| /lib | Libraries |
| /opt | Optional software |

---

# Basic Linux Commands

## 1. pwd
Displays the current working directory.

```bash
pwd
```

---

## 2. ls
Lists files and directories.

```bash
ls
ls -l
ls -a
```

---

## 3. cd
Changes the directory.

```bash
cd Documents
cd ..
cd ~
```

---

## 4. mkdir
Creates a new directory.

```bash
mkdir Project
```

---

## 5. rmdir
Removes an empty directory.

```bash
rmdir Project
```

---

## 6. touch
Creates an empty file.

```bash
touch file.txt
```

---

## 7. cp
Copies files or directories.

```bash
cp file1.txt file2.txt
cp -r Folder Backup
```

---

## 8. mv
Moves or renames files.

```bash
mv file.txt Documents/
mv old.txt new.txt
```

---

## 9. rm
Deletes files or directories.

```bash
rm file.txt
rm -r Folder
```

---

## 10. cat
Displays file contents.

```bash
cat file.txt
```

---

## 11. nano
Opens Nano text editor.

```bash
nano file.txt
```

---

## 12. vim
Opens Vim editor.

```bash
vim file.txt
```

---

## 13. clear
Clears the terminal.

```bash
clear
```

---

## 14. echo
Prints text or variables.

```bash
echo Hello
```

---

## 15. man
Displays command manual.

```bash
man ls
```

---

## 16. whoami
Shows current username.

```bash
whoami
```

---

## 17. date
Displays system date and time.

```bash
date
```

---

## 18. cal
Displays calendar.

```bash
cal
```

---

## 19. history
Shows previously executed commands.

```bash
history
```

---

## 20. uname
Displays system information.

```bash
uname
uname -a
```

---

## 21. hostname
Shows system hostname.

```bash
hostname
```

---

## 22. df
Displays disk usage.

```bash
df -h
```

---

## 23. du
Shows directory size.

```bash
du -sh Folder
```

---

## 24. free
Displays memory usage.

```bash
free -h
```

---

## 25. top
Shows running processes.

```bash
top
```

---

## 26. ps
Displays active processes.

```bash
ps
ps -ef
```

---

## 27. kill
Terminates a process.

```bash
kill PID
```

---

## 28. chmod
Changes file permissions.

```bash
chmod 755 script.sh
```

---

## 29. chown
Changes file ownership.

```bash
chown user file.txt
```

---

## 30. find
Searches for files.

```bash
find . -name file.txt
```

---

## 31. grep
Searches text inside files.

```bash
grep "Linux" file.txt
```

---

## 32. sort
Sorts lines.

```bash
sort file.txt
```

---

## 33. wc
Counts words, lines, and characters.

```bash
wc file.txt
```

---

## 34. head
Displays first lines.

```bash
head file.txt
```

---

## 35. tail
Displays last lines.

```bash
tail file.txt
tail -f log.txt
```

---

## 36. zip
Compresses files.

```bash
zip archive.zip file.txt
```

---

## 37. unzip
Extracts ZIP files.

```bash
unzip archive.zip
```

---

## 38. tar
Creates or extracts tar archives.

```bash
tar -cvf files.tar Folder
tar -xvf files.tar
```

---

## 39. ping
Checks network connectivity.

```bash
ping google.com
```

---

## 40. wget
Downloads files from the internet.

```bash
wget https://example.com/file.zip
```

---

# File Permissions

Linux permissions are represented by:

```
r = Read
w = Write
x = Execute
```

Example:

```
-rwxr-xr--
```

Permission values:

| Number | Permission |
|---------|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 3 | -wx |
| 2 | -w- |
| 1 | --x |
| 0 | --- |

Example:

```bash
chmod 755 file.sh
```

---

# Useful Keyboard Shortcuts

| Shortcut | Function |
|-----------|----------|
| Ctrl + C | Stop running process |
| Ctrl + Z | Suspend process |
| Ctrl + D | Logout/EOF |
| Ctrl + L | Clear screen |
| Ctrl + A | Move to beginning of line |
| Ctrl + E | Move to end of line |
| Ctrl + R | Search command history |
| Tab | Auto-complete |
| Up Arrow | Previous command |
| Down Arrow | Next command |

---

# Popular Linux Distributions

- Ubuntu
- Debian
- Fedora
- CentOS
- Rocky Linux
- AlmaLinux
- Kali Linux
- Arch Linux
- Linux Mint
- openSUSE

---

# Why Learn Linux?

- Essential for Software Development
- Used in Cloud Computing
- Required for DevOps
- Popular in Cybersecurity
- Widely used in Servers
- Foundation for Embedded Systems
- Valuable for Networking
- Improves Command-Line Skills

---

# Summary

Linux is a powerful, secure, and open-source operating system used worldwide. Understanding Linux commands, file systems, permissions, and process management is essential for developers, system administrators, cybersecurity professionals, and engineering students. Mastering the command line significantly improves productivity and is a valuable skill in modern IT and software development.

---

## Quick Command Cheat Sheet

| Command | Purpose |
|----------|---------|
| pwd | Current directory |
| ls | List files |
| cd | Change directory |
| mkdir | Create directory |
| rmdir | Remove directory |
| touch | Create file |
| cp | Copy files |
| mv | Move/Rename |
| rm | Delete files |
| cat | View file |
| nano | Edit file |
| clear | Clear terminal |
| whoami | Current user |
| uname -a | System info |
| df -h | Disk usage |
| free -h | Memory usage |
| ps | Running processes |
| top | Live processes |
| chmod | Change permissions |
| grep | Search text |
| find | Find files |
| history | Command history |
| head | First lines |
| tail | Last lines |
| ping | Network test |

---

**Author:** Your Name  
**License:** MIT License