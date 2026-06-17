# Linux Permissions & System Commands

This document covers Linux file permissions, system navigation, and essential commands for Operating Systems practice.

---

## 📌 Terminal Modes

- `Ctrl + Alt + F2–F6` → Text-based terminal
- `init 3` → Text mode
- `Ctrl + Alt + F1 / F7` → Graphical interface
- `init 5` → Graphical interface

---

## 📂 File Viewing Commands

- `cat file` → Display full file content
- `head file` → First 10 lines
- `tail file` → Last lines
- `head -N file` → First N lines
- `wc file` → Lines, words, characters
- `wc -l file` → Line count only
- `wc -w file` → Word count only
- `wc -c file` → Character count only

---

## 💾 System & Utility Commands

- `df -h` → Disk usage information
- `dir -p` → Directory listing
- `man command` → Help manual
- `--help` → Command help
- `sort file` → Sort ascending
- `sort -r file` → Sort descending

---

## 🔐 File Permissions (chmod)

### Symbolic Mode

- `a` → all users
- `u` → owner
- `g` → group
- `o` → others

Operations:
- `+` → add permission
- `-` → remove permission

Permissions:
- `r` → read
- `w` → write
- `x` → execute

### Examples

- `chmod u+x file` → make executable for owner
- `chmod u-x file` → remove execute for owner
- `chmod a+rw file` → read/write for all
- `chmod a-w file` → remove write for all

---

## 🔢 Numeric Permission System

| Value | Meaning |
|------|--------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 3 | -wx |
| 2 | -w- |
| 1 | --x |
| 0 | --- |

### Common Modes

- `777` → full access for all
- `755` → owner full, others read/execute
- `700` → only owner full access
- `666` → read/write for all
- `644` → owner read/write, others read
- `600` → owner only read/write

---

## 📁 Directory Permissions

- `r` → list files
- `w` → create/delete files
- `x` → enter directory (traverse)

### Examples

- `chmod 777 dir` → full access
- `chmod 755 dir` → safe public access
- `chmod 700 dir` → private directory

---

## 🧭 File System Navigation

- `/` → root directory
- `cd /` → go to root
- `pwd` → current path
- `ls` → list contents

### Access Methods

- `cd dir1/dir2/file`
- direct path access without step-by-step navigation

---

## 🧑‍💻 System Directories

- `/boot` → boot files and kernel
- `/root` → admin home directory
- `/home` → user directories
- `/usr` → system programs
- `/usr/bin` → user commands
- `/usr/sbin` → admin commands
- `/sbin` → system binaries
- `/etc` → configuration files
- `/dev` → device files

---

## 🔁 Key Difference

- `chmod` → changes permissions
- `chown` → changes ownership

---

## ⚠️ Notes

- Files starting with `.` are hidden
- Linux is case-sensitive
- File names can be up to 255 characters
