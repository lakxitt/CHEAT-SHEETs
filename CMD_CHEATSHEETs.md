# 💻 Command Prompt (CMD) Cheat Sheet

> A quick reference guide for the most useful Windows Command Prompt (CMD) commands for system administration, networking, troubleshooting, and cybersecurity.

> **Tested on:** Windows 10 / Windows 11

---

# 📚 Table of Contents

- Navigation
- File & Directory Management
- File Operations
- System Information
- Network Commands
- User Management
- Process Management
- Disk Management
- Services
- Environment Variables
- Scheduling
- Startup & Shutdown
- Networking Troubleshooting
- Useful Shortcuts

---

# 📂 Navigation

| Command | Description |
|---------|-------------|
| `cd` | Change current directory |
| `cd..` | Move one directory up |
| `cd \` | Go to root directory |
| `dir` | List files and folders |
| `tree` | Display directory structure |
| `cls` | Clear screen |
| `exit` | Exit CMD |

### Examples

```cmd
cd Desktop

cd..

cd \

dir
```

---

# 📁 File & Directory Management

| Command | Description |
|---------|-------------|
| `mkdir folder` | Create folder |
| `rmdir folder` | Remove empty folder |
| `rmdir /s folder` | Remove folder and contents |
| `ren old new` | Rename file/folder |
| `move file destination` | Move files |
| `copy file destination` | Copy files |
| `xcopy` | Copy directories |
| `robocopy` | Advanced file copy |
| `del file` | Delete file |
| `erase file` | Delete file |
| `type file.txt` | View file contents |

---

# 📄 File Operations

| Command | Description |
|---------|-------------|
| `echo` | Print text |
| `more` | View long files page by page |
| `find` | Search text |
| `findstr` | Advanced text search |
| `fc` | Compare files |
| `attrib` | View/change file attributes |

Example

```cmd
findstr "admin" users.txt
```

---

# 🖥 System Information

| Command | Description |
|---------|-------------|
| `systeminfo` | Display system information |
| `hostname` | Show computer name |
| `ver` | Windows version |
| `whoami` | Current logged-in user |
| `date` | Current date |
| `time` | Current time |
| `set` | Environment variables |
| `path` | Display PATH variable |

---

# 🌐 Network Commands

| Command | Description |
|---------|-------------|
| `ipconfig` | Display IP configuration |
| `ipconfig /all` | Detailed network information |
| `ipconfig /release` | Release DHCP IP |
| `ipconfig /renew` | Renew DHCP IP |
| `ipconfig /flushdns` | Clear DNS cache |
| `ping` | Test connectivity |
| `tracert` | Trace network route |
| `pathping` | Ping + route analysis |
| `nslookup` | DNS lookup |
| `netstat` | Network connections |
| `arp -a` | ARP cache |
| `route print` | Routing table |
| `getmac` | Display MAC addresses |
| `netsh` | Network configuration utility |

Example

```cmd
ping google.com

tracert google.com

ipconfig /all
```

---

# 👤 User Management

| Command | Description |
|---------|-------------|
| `net user` | List users |
| `net user username` | Show user details |
| `net localgroup` | List local groups |
| `whoami /groups` | Show current user groups |

---

# ⚙ Process Management

| Command | Description |
|---------|-------------|
| `tasklist` | List running processes |
| `taskkill /PID PID` | Kill process by PID |
| `taskkill /IM app.exe /F` | Force kill process |
| `wmic process list brief` | List processes (legacy) |

---

# 💾 Disk Management

| Command | Description |
|---------|-------------|
| `diskpart` | Disk partition tool |
| `chkdsk` | Check disk health |
| `format` | Format drive |
| `vol` | Show volume label |
| `label` | Change drive label |

---

# 🔧 Services

| Command | Description |
|---------|-------------|
| `sc query` | List services |
| `sc start service` | Start service |
| `sc stop service` | Stop service |
| `net start` | Running services |
| `net stop service` | Stop service |

---

# 🌱 Environment Variables

| Command | Description |
|---------|-------------|
| `set` | Show variables |
| `echo %PATH%` | Display PATH |
| `echo %TEMP%` | Show temp folder |
| `set VAR=value` | Create variable |

---

# ⏰ Scheduling

| Command | Description |
|---------|-------------|
| `schtasks` | Manage scheduled tasks |
| `at` | Legacy scheduler (deprecated) |

---

# 🔄 Startup & Shutdown

| Command | Description |
|---------|-------------|
| `shutdown /s` | Shutdown PC |
| `shutdown /r` | Restart PC |
| `shutdown /l` | Log off |
| `shutdown /a` | Abort shutdown |
| `shutdown /t 60` | Shutdown after 60 seconds |

---

# 🔍 Networking Troubleshooting Workflow

```text
1. ipconfig

↓

2. ping 127.0.0.1

↓

3. ping Gateway

↓

4. ping 8.8.8.8

↓

5. ping google.com

↓

6. nslookup google.com

↓

7. tracert google.com

↓

8. netstat -ano
```

---

# 🔐 Useful Cybersecurity Commands

| Command | Purpose |
|---------|---------|
| `whoami /priv` | Show user privileges |
| `whoami /groups` | Display group memberships |
| `netstat -ano` | Show active connections and PIDs |
| `tasklist` | Running processes |
| `systeminfo` | System enumeration |
| `hostname` | Computer name |
| `ipconfig /all` | Network enumeration |
| `arp -a` | ARP table |
| `route print` | Routing table |
| `net user` | Local users |
| `net localgroup administrators` | Local administrators |

---

# ⚡ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `↑` | Previous command |
| `↓` | Next command |
| `Tab` | Auto-complete |
| `Ctrl + C` | Stop running command |
| `F7` | Command history |
| `F3` | Repeat last command |
| `Alt + Enter` | Fullscreen (legacy systems) |

---

# 📌 Quick Reference

```cmd
cls                     Clear screen

dir                     List files

cd                      Change directory

mkdir                   Create folder

rmdir                   Delete folder

copy                    Copy files

move                    Move files

del                     Delete file

systeminfo              System information

hostname                Computer name

whoami                  Current user

tasklist                Running processes

taskkill                Kill process

ipconfig                Network configuration

ping                    Test connectivity

tracert                 Trace route

netstat                 Active connections

nslookup                DNS lookup

arp -a                  ARP table

route print             Routing table

shutdown /r             Restart PC

shutdown /s             Shutdown PC
```

---

# 💡 Tips

- Run **Command Prompt as Administrator** for commands that require elevated privileges.
- Use **Tab** to auto-complete file and folder names.
- Add `/?` after most commands to view built-in help (for example, `ipconfig /?`).

---

# 📜 License

MIT License

---

⭐ **If you found this cheat sheet useful, consider starring the repository!**
