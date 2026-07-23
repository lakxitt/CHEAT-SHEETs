# 🪟 Windows Cheat Sheet

> A comprehensive Windows Cheat Sheet covering CMD commands, PowerShell basics, networking, file management, system administration, process management, user management, disk management, services, and troubleshooting.

![Windows](https://img.shields.io/badge/OS-Windows-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Markdown](https://img.shields.io/badge/Made%20With-Markdown-orange)

---

# 📖 Table of Contents

* CMD Basics
* Navigation
* File & Folder Management
* File Operations
* Search
* Networking
* System Information
* Process Management
* User Management
* Services
* Disk Management
* Environment Variables
* Task Scheduler
* Shutdown Commands
* PowerShell Basics
* Useful Keyboard Shortcuts
* Troubleshooting
* Best Practices

---

# What is CMD?

**Command Prompt (CMD)** is Windows' built-in command-line interpreter used for file management, networking, system administration, and automation.

---

# Open CMD

```
Win + R → cmd
```

Run as Administrator

```
Win + X → Terminal (Admin)
```

---

# Basic Commands

Show current directory

```cmd
cd
```

Clear screen

```cmd
cls
```

Show command history

```cmd
doskey /history
```

Exit CMD

```cmd
exit
```

Display help

```cmd
help
```

Help for a specific command

```cmd
ipconfig /?
```

---

# Directory Navigation

Go to a folder

```cmd
cd FolderName
```

Go back

```cmd
cd ..
```

Go to root

```cmd
cd \
```

Change drive

```cmd
D:
```

List files

```cmd
dir
```

List hidden files

```cmd
dir /a
```

Tree view

```cmd
tree
```

---

# File & Folder Management

Create folder

```cmd
mkdir Projects
```

Remove empty folder

```cmd
rmdir Projects
```

Force delete folder

```cmd
rmdir /s /q Projects
```

Create file

```cmd
type nul > notes.txt
```

Delete file

```cmd
del notes.txt
```

Rename file

```cmd
ren old.txt new.txt
```

Copy file

```cmd
copy source.txt backup.txt
```

Move file

```cmd
move report.txt Documents\
```

---

# File Operations

Display file contents

```cmd
type notes.txt
```

Compare files

```cmd
fc file1.txt file2.txt
```

Find text

```cmd
find "password" notes.txt
```

Search recursively

```cmd
findstr /s "admin" *.txt
```

---

# Networking

Show IP configuration

```cmd
ipconfig
```

Detailed network information

```cmd
ipconfig /all
```

Release IP

```cmd
ipconfig /release
```

Renew IP

```cmd
ipconfig /renew
```

Flush DNS cache

```cmd
ipconfig /flushdns
```

Ping a host

```cmd
ping google.com
```

Continuous ping

```cmd
ping -t google.com
```

Trace route

```cmd
tracert google.com
```

DNS lookup

```cmd
nslookup google.com
```

Display active connections

```cmd
netstat -ano
```

Display routing table

```cmd
route print
```

ARP cache

```cmd
arp -a
```

---

# System Information

System details

```cmd
systeminfo
```

Current hostname

```cmd
hostname
```

Current user

```cmd
whoami
```

Windows version

```cmd
ver
```

Check serial number

```cmd
wmic bios get serialnumber
```

---

# Process Management

Running tasks

```cmd
tasklist
```

Kill by name

```cmd
taskkill /IM chrome.exe /F
```

Kill by PID

```cmd
taskkill /PID 1234 /F
```

---

# User Management

List users

```cmd
net user
```

User information

```cmd
net user username
```

Create user

```cmd
net user student Password123 /add
```

Delete user

```cmd
net user student /delete
```

---

# Services

List services

```cmd
sc query
```

Start service

```cmd
net start Spooler
```

Stop service

```cmd
net stop Spooler
```

---

# Disk Management

Check disk

```cmd
chkdsk
```

Repair disk

```cmd
chkdsk C: /f
```

Disk partitions

```cmd
diskpart
```

List drives

```cmd
wmic logicaldisk get name,size,freespace
```

---

# Environment Variables

Show all variables

```cmd
set
```

Display PATH

```cmd
echo %PATH%
```

Set variable

```cmd
set NAME=Lakshit
```

---

# Shutdown & Restart

Shutdown

```cmd
shutdown /s /t 0
```

Restart

```cmd
shutdown /r /t 0
```

Log off

```cmd
shutdown /l
```

Abort shutdown

```cmd
shutdown /a
```

---

# Task Scheduler

List scheduled tasks

```cmd
schtasks
```

Run a task

```cmd
schtasks /run /tn "TaskName"
```

---

# PowerShell Basics

Open PowerShell

```powershell
powershell
```

Current directory

```powershell
Get-Location
```

List files

```powershell
Get-ChildItem
```

Running processes

```powershell
Get-Process
```

Running services

```powershell
Get-Service
```

Current execution policy

```powershell
Get-ExecutionPolicy
```

---

# Useful Keyboard Shortcuts

| Shortcut           | Action        |
| ------------------ | ------------- |
| Win + R            | Run dialog    |
| Win + E            | File Explorer |
| Win + L            | Lock PC       |
| Win + D            | Show Desktop  |
| Ctrl + Shift + Esc | Task Manager  |
| Win + X            | Quick Menu    |
| Alt + Tab          | Switch Apps   |
| Win + Tab          | Task View     |

---

# Troubleshooting Commands

System File Checker

```cmd
sfc /scannow
```

Repair Windows Image

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

Check drivers

```cmd
driverquery
```

Installed hotfixes

```cmd
wmic qfe list
```

---

# Common Networking Ports

| Port  | Service |
| ----- | ------- |
| 20/21 | FTP     |
| 22    | SSH     |
| 23    | Telnet  |
| 25    | SMTP    |
| 53    | DNS     |
| 80    | HTTP    |
| 110   | POP3    |
| 143   | IMAP    |
| 443   | HTTPS   |
| 445   | SMB     |
| 3389  | RDP     |

---

# Best Practices

* Run administrative commands in an elevated terminal.
* Be cautious with `del`, `rmdir /s`, and `diskpart`.
* Always verify commands before executing them.
* Keep Windows updated.
* Use `sfc` and `DISM` for system repair.
* Use PowerShell for automation and scripting.
* Back up important data before performing system maintenance.

---

# Quick Reference

| Command      | Description           |
| ------------ | --------------------- |
| `dir`        | List files            |
| `cd`         | Change directory      |
| `mkdir`      | Create folder         |
| `rmdir`      | Remove folder         |
| `copy`       | Copy files            |
| `move`       | Move files            |
| `del`        | Delete files          |
| `ipconfig`   | Network configuration |
| `ping`       | Test connectivity     |
| `tracert`    | Trace network path    |
| `netstat`    | Active connections    |
| `tasklist`   | Running processes     |
| `taskkill`   | Stop processes        |
| `systeminfo` | System information    |
| `whoami`     | Current user          |
| `hostname`   | Computer name         |
| `shutdown`   | Shutdown or restart   |

---

# Resources

* Microsoft Learn
* Windows Command Reference
* PowerShell Documentation
* Sysinternals Suite

---

⭐ **If you found this repository helpful, consider giving it a Star!**
