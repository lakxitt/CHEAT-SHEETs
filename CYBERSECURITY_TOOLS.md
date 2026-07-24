# 🐧 Linux Tools Every Hacker Should Know

> A curated cheat sheet of essential Linux tools used by penetration testers, ethical hackers, system administrators, and cybersecurity professionals.
>
> **Disclaimer:** These tools are intended for **authorized security testing, learning, and system administration only**. Always obtain permission before testing any system.

---

# 📚 Table of Contents

- Information Gathering
- Network Analysis
- Web Testing
- Password Security
- Wireless Security
- Exploitation Frameworks
- Digital Forensics
- Reverse Engineering
- Traffic Analysis
- System Monitoring
- File Analysis
- Linux Utilities

---

# 🔍 Information Gathering

| Tool | Description |
|------|-------------|
| **Nmap** | Network scanner for host discovery, port scanning, service detection, OS detection, and vulnerability discovery. |
| **Masscan** | Extremely fast Internet-scale port scanner. |
| **Netcat (nc)** | Read/write network connections; often called the "Swiss Army Knife of Networking." |
| **Whois** | Retrieves domain registration information. |
| **Dig** | Advanced DNS lookup utility. |
| **Nslookup** | Basic DNS query tool. |
| **Host** | Quick DNS resolution utility. |
| **Traceroute** | Displays the path packets take to a destination. |
| **Ping** | Checks host availability and network latency. |
| **arp** | Displays and manages the ARP cache. |

---

# 🌐 Network Analysis

| Tool | Description |
|------|-------------|
| **tcpdump** | Command-line packet capture and traffic analysis tool. |
| **Wireshark** | GUI packet analyzer for inspecting network traffic. |
| **ss** | Displays active network sockets and connections. |
| **netstat** | Shows network connections, routing tables, and listening ports. |
| **iftop** | Real-time network bandwidth monitor. |
| **ip** | Modern Linux networking configuration utility. |
| **route** | Displays or modifies the routing table. |

---

# 🌍 Web Application Testing

| Tool | Description |
|------|-------------|
| **Burp Suite** | Intercepting proxy for web application security testing. |
| **Nikto** | Web server vulnerability scanner. |
| **Gobuster** | Directory, DNS, and virtual host brute-forcing tool. |
| **Dirsearch** | Fast web directory discovery scanner. |
| **ffuf** | High-speed web fuzzing and content discovery tool. |
| **WhatWeb** | Identifies technologies used by websites. |
| **Wappalyzer** | Detects frameworks, CMSs, and technologies. |
| **sqlmap** | Automated SQL injection detection and exploitation tool. |

---

# 🔐 Password Security

| Tool | Description |
|------|-------------|
| **John the Ripper** | Password hash cracking tool supporting many hash formats. |
| **Hashcat** | GPU-accelerated password recovery tool. |
| **Hydra** | Network login password auditing tool. |
| **Medusa** | Parallel brute-force login testing tool. |
| **CeWL** | Generates custom wordlists from websites. |
| **Crunch** | Creates custom password wordlists. |

---

# 📶 Wireless Security

| Tool | Description |
|------|-------------|
| **Aircrack-ng** | Complete Wi-Fi security auditing suite. |
| **Airodump-ng** | Captures wireless packets and collects network information. |
| **Aireplay-ng** | Packet injection tool used for Wi-Fi testing. |
| **Airmon-ng** | Enables monitor mode on wireless interfaces. |
| **Reaver** | Tests WPS PIN vulnerabilities. |
| **Kismet** | Wireless network detector and passive packet sniffer. |

---

# 💥 Exploitation Frameworks

| Tool | Description |
|------|-------------|
| **Metasploit Framework** | Popular penetration testing and exploit development framework. |
| **Searchsploit** | Offline search utility for Exploit Database exploits. |
| **msfvenom** | Payload generation utility included with Metasploit. |

---

# 🔎 Digital Forensics

| Tool | Description |
|------|-------------|
| **Autopsy** | Digital forensic investigation platform. |
| **Binwalk** | Firmware extraction and analysis tool. |
| **Foremost** | File recovery utility based on file headers. |
| **ExifTool** | Reads and edits file metadata. |
| **Strings** | Extracts readable strings from binary files. |

---

# ⚙ Reverse Engineering

| Tool | Description |
|------|-------------|
| **GDB** | GNU debugger for analyzing executables. |
| **Ghidra** | Software reverse engineering suite developed by the NSA. |
| **Radare2** | Reverse engineering framework for binaries. |
| **Objdump** | Displays executable file information and disassembly. |
| **readelf** | Displays ELF binary file information. |

---

# 📦 File Analysis

| Tool | Description |
|------|-------------|
| **file** | Identifies file types. |
| **xxd** | Creates and reverses hexadecimal dumps. |
| **hexdump** | Displays files in hexadecimal format. |
| **md5sum** | Calculates MD5 checksums. |
| **sha256sum** | Calculates SHA-256 hashes. |

---

# 📊 System Monitoring

| Tool | Description |
|------|-------------|
| **top** | Displays running processes and CPU usage. |
| **htop** | Interactive process viewer. |
| **ps** | Lists running processes. |
| **lsof** | Lists open files and network connections. |
| **journalctl** | Views systemd logs. |
| **dmesg** | Displays kernel messages. |

---

# 📁 Linux Utilities

| Tool | Description |
|------|-------------|
| **grep** | Searches text using patterns. |
| **awk** | Powerful text processing language. |
| **sed** | Stream editor for modifying text. |
| **find** | Searches files and directories. |
| **locate** | Quickly finds files using a database. |
| **sort** | Sorts lines of text. |
| **uniq** | Removes duplicate lines. |
| **cut** | Extracts columns from text. |
| **tr** | Replaces or deletes characters. |
| **tee** | Writes output to both terminal and file. |
| **curl** | Transfers data to/from servers using URLs. |
| **wget** | Downloads files from the web. |
| **tar** | Archives files. |
| **zip / unzip** | Compresses and extracts ZIP archives. |
| **chmod** | Changes file permissions. |
| **chown** | Changes file ownership. |
| **scp** | Securely copies files over SSH. |
| **rsync** | Efficient file synchronization utility. |

---

# ⭐ Most Essential Tools

| Category | Tool |
|----------|------|
| Port Scanning | Nmap |
| Packet Capture | tcpdump |
| Traffic Analysis | Wireshark |
| Web Testing | Burp Suite |
| SQL Injection | sqlmap |
| Directory Discovery | ffuf |
| Password Cracking | Hashcat |
| Password Auditing | Hydra |
| Wi-Fi Testing | Aircrack-ng |
| Exploitation | Metasploit |
| Exploit Search | Searchsploit |
| DNS Lookup | dig |
| Networking | Netcat |
| File Transfer | curl |
| Process Monitoring | htop |
| Reverse Engineering | Ghidra |

---

# 📖 Recommended Learning Order

1. Linux Commands
2. Nmap
3. Netcat
4. tcpdump
5. Wireshark
6. Burp Suite
7. ffuf
8. Gobuster
9. sqlmap
10. Hydra
11. John the Ripper
12. Hashcat
13. Aircrack-ng
14. Metasploit
15. Ghidra

---

# 📜 License

This repository is licensed under the **MIT License**.

---

⭐ **If you found this cheat sheet useful, consider giving the repository a star!**
