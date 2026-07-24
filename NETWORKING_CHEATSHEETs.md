# 🌐 Networking Cheat Sheet

> A quick reference guide covering the most important networking concepts, protocols, commands, ports, and troubleshooting techniques.

---

# 📖 Table of Contents

- OSI Model
- TCP/IP Model
- Network Devices
- IP Addressing
- Subnetting
- Common Protocols
- Common Ports
- TCP vs UDP
- Packet Flow
- DNS Resolution
- DHCP Process
- NAT
- Routing
- Switching
- VLAN
- ARP
- ICMP
- Network Commands
- Wireshark Filters
- Nmap Basics
- Troubleshooting
- Common Attacks

---

# 🌍 OSI Model

| Layer | Name | Protocols | Devices |
|--------|------|-----------|---------|
| 7 | Application | HTTP, FTP, SMTP, DNS | Gateway |
| 6 | Presentation | SSL/TLS | Gateway |
| 5 | Session | NetBIOS | Gateway |
| 4 | Transport | TCP, UDP | Firewall |
| 3 | Network | IP, ICMP | Router |
| 2 | Data Link | Ethernet, ARP | Switch |
| 1 | Physical | Cables, Fiber | Hub |

**Remember**

```
All People Seem To Need Data Processing
```

---

# 📡 TCP/IP Model

| Layer | Protocols |
|---------|----------|
| Application | HTTP FTP SSH DNS SMTP |
| Transport | TCP UDP |
| Internet | IP ICMP ARP |
| Network Access | Ethernet WiFi |

---

# 🔀 TCP vs UDP

| TCP | UDP |
|------|------|
| Reliable | Unreliable |
| Connection Oriented | Connectionless |
| Slow | Fast |
| Error Checking | Minimal |
| Ordered Delivery | No Ordering |
| Web, SSH | DNS, VoIP, Streaming |

---

# 🌐 IPv4 Address Classes

| Class | Range | Default Mask |
|--------|---------|--------------|
| A | 1-126 | /8 |
| B | 128-191 | /16 |
| C | 192-223 | /24 |
| D | 224-239 | Multicast |
| E | 240-255 | Experimental |

---

# 🏠 Private IP Ranges

```
10.0.0.0/8

172.16.0.0 - 172.31.255.255

192.168.0.0/16
```

---

# 🔁 Loopback

```
127.0.0.1
```

---

# ⚡ APIPA

```
169.254.x.x
```

Automatically assigned when DHCP fails.

---

# 🧮 CIDR

| CIDR | Subnet Mask |
|-------|-------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |
| /30 | 255.255.255.252 |

---

# 🌐 Important Protocols

| Protocol | Purpose |
|-----------|---------|
| HTTP | Web |
| HTTPS | Secure Web |
| FTP | File Transfer |
| SFTP | Secure File Transfer |
| SSH | Secure Remote Login |
| Telnet | Remote Login |
| DNS | Name Resolution |
| DHCP | IP Assignment |
| SMTP | Send Email |
| POP3 | Receive Email |
| IMAP | Sync Email |
| SNMP | Network Monitoring |
| NTP | Time Synchronization |
| LDAP | Directory Services |
| SMB | File Sharing |
| RDP | Remote Desktop |

---

# 🔥 Common Ports

| Port | Service |
|------|----------|
| 20 | FTP Data |
| 21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 67 | DHCP Server |
| 68 | DHCP Client |
| 69 | TFTP |
| 80 | HTTP |
| 110 | POP3 |
| 123 | NTP |
| 143 | IMAP |
| 161 | SNMP |
| 389 | LDAP |
| 443 | HTTPS |
| 445 | SMB |
| 3389 | RDP |

---

# 📦 Packet Flow

```
Application

↓

Transport

↓

Network

↓

Data Link

↓

Physical

↓

Transmission

↓

Physical

↓

Data Link

↓

Network

↓

Transport

↓

Application
```

---

# 🌍 DNS Resolution

```
User

↓

Browser Cache

↓

Operating System Cache

↓

Router Cache

↓

ISP DNS

↓

Root Server

↓

TLD Server

↓

Authoritative DNS

↓

IP Address Returned
```

---

# ⚙ DHCP Process

```
Discover

↓

Offer

↓

Request

↓

Acknowledge
```

Remember:

```
DORA
```

---

# 🔁 TCP Three-Way Handshake

```text
Client              Server

SYN  ------------->

      <------------- SYN + ACK

ACK ------------->
```

---

# ❌ TCP Connection Termination

```
FIN

ACK

FIN

ACK
```

---

# 🌍 ARP

Maps

```
IP Address → MAC Address
```

Useful Commands

```
arp -a
```

---

# 📢 ICMP

Used for

- Ping
- Traceroute
- Error Reporting

---

# 🔀 NAT

Converts

```
Private IP

↓

Public IP
```

Types

- Static NAT
- Dynamic NAT
- PAT

---

# 📡 VLAN

Benefits

- Better Security
- Reduced Broadcast
- Easier Management
- Better Performance

---

# 🔀 Routing

Types

- Static
- Dynamic

Protocols

- RIP
- OSPF
- EIGRP
- BGP

---

# 🌐 Network Devices

| Device | Purpose |
|---------|----------|
| Hub | Broadcast Everything |
| Switch | Uses MAC Address |
| Router | Uses IP Address |
| Firewall | Filters Traffic |
| Access Point | Wireless Network |
| Modem | ISP Connection |

---

# 💻 Windows Commands

```cmd
ipconfig

ipconfig /all

ping

tracert

netstat

arp -a

route print

nslookup

hostname

getmac
```

---

# 🐧 Linux Commands

```bash
ip addr

ifconfig

ping

traceroute

netstat

ss

arp

route

dig

host

nslookup

tcpdump
```

---

# 📊 Wireshark Filters

```
ip.addr == 192.168.1.1

http

dns

tcp

udp

icmp

arp

tcp.port == 80

tcp.port == 443

frame contains "password"
```

---

# 🔎 Nmap Basics

```bash
nmap IP

nmap -sS IP

nmap -sV IP

nmap -A IP

nmap -O IP

nmap -Pn IP

nmap -p 80,443 IP

nmap -p- IP
```

---

# 🛠 Troubleshooting Steps

1. Check Cable
2. Check Link Light
3. Verify IP Address
4. Ping Localhost
5. Ping Gateway
6. Ping Remote Host
7. Check DNS
8. Check Firewall
9. Check Routing
10. Capture Packets

---

# 🚨 Common Network Attacks

| Attack | Description |
|----------|-------------|
| ARP Spoofing | Fake ARP Replies |
| DNS Poisoning | Fake DNS Records |
| SYN Flood | TCP DoS Attack |
| DDoS | Distributed Attack |
| MITM | Man in the Middle |
| MAC Flooding | Overflow Switch CAM Table |
| VLAN Hopping | Cross VLAN Attack |

---

# 📌 Important Numbers

```
IPv4 = 32 bits

IPv6 = 128 bits

MAC Address = 48 bits

TCP Header = 20 bytes

UDP Header = 8 bytes

Ethernet MTU = 1500 bytes

TTL Default = 64 or 128

Well Known Ports = 0-1023

Registered Ports = 1024-49151

Dynamic Ports = 49152-65535
```

---

# ⭐ Interview Questions

- Difference between TCP and UDP?
- Explain the OSI Model.
- What is Subnetting?
- What is NAT?
- What is ARP?
- Difference between Hub, Switch, and Router?
- Explain DNS Resolution.
- What happens when you type a URL?
- Difference between HTTP and HTTPS?
- Explain VLAN.
- What is DHCP?
- What is CIDR?
- Difference between Private and Public IP?
- What is ICMP?
- Explain the TCP Handshake.

---

# 📚 Useful Mnemonics

OSI Layers

```
All People Seem To Need Data Processing
```

DHCP

```
DORA

Discover

Offer

Request

Acknowledge
```

TCP Handshake

```
SYN

SYN-ACK

ACK
```

---

## 📜 License

MIT License

---

⭐ If this cheat sheet helped you, consider giving the repository a star!
