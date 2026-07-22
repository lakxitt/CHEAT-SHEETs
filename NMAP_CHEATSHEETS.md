# Nmap Command Cheat Sheet

A quick reference guide for the most commonly used **Nmap** commands.

> **Syntax**
>
> ```bash
> nmap [Scan Type(s)] [Options] <Target>
> ```

---

# Basic Scans

```bash
nmap 192.168.1.1
```
Basic scan of the top 1000 TCP ports.

```bash
nmap scanme.nmap.org
```
Scan a hostname.

```bash
nmap 192.168.1.1 192.168.1.2
```
Scan multiple hosts.

```bash
nmap 192.168.1.1-100
```
Scan an IP range.

```bash
nmap 192.168.1.0/24
```
Scan an entire subnet.

```bash
nmap -iL targets.txt
```
Scan targets from a file.

```bash
nmap --exclude 192.168.1.5 192.168.1.0/24
```
Exclude a host.

```bash
nmap --excludefile exclude.txt 192.168.1.0/24
```
Exclude hosts from a file.

---

# Host Discovery

```bash
nmap -sn 192.168.1.0/24
```
Ping scan only.

```bash
nmap -Pn 192.168.1.10
```
Treat host as online.

```bash
nmap -PS 80,443 192.168.1.10
```
TCP SYN Ping.

```bash
nmap -PA 80 192.168.1.10
```
TCP ACK Ping.

```bash
nmap -PU 53 192.168.1.10
```
UDP Ping.

```bash
nmap -PE 192.168.1.10
```
ICMP Echo Ping.

```bash
nmap -PP 192.168.1.10
```
ICMP Timestamp Ping.

```bash
nmap -PM 192.168.1.10
```
ICMP Netmask Ping.

```bash
nmap -PR 192.168.1.0/24
```
ARP Scan.

---

# Port Scanning

```bash
nmap -sS target
```
SYN Scan.

```bash
nmap -sT target
```
TCP Connect Scan.

```bash
nmap -sU target
```
UDP Scan.

```bash
nmap -sA target
```
ACK Scan.

```bash
nmap -sW target
```
Window Scan.

```bash
nmap -sM target
```
Maimon Scan.

```bash
nmap -sN target
```
NULL Scan.

```bash
nmap -sF target
```
FIN Scan.

```bash
nmap -sX target
```
Xmas Scan.

```bash
nmap -sY target
```
SCTP INIT Scan.

```bash
nmap -sZ target
```
SCTP COOKIE Scan.

```bash
nmap -sI zombie target
```
Idle Scan.

---

# Port Selection

```bash
nmap -p 22 target
```

```bash
nmap -p 22,80,443 target
```

```bash
nmap -p 1-1000 target
```

```bash
nmap -p- target
```

```bash
nmap --top-ports 100 target
```

```bash
nmap -F target
```

---

# Service & Version Detection

```bash
nmap -sV target
```

```bash
nmap --version-light target
```

```bash
nmap --version-all target
```

```bash
nmap --version-intensity 0 target
```

```bash
nmap --version-intensity 9 target
```

---

# Operating System Detection

```bash
nmap -O target
```

```bash
nmap -A target
```

```bash
nmap --osscan-limit target
```

```bash
nmap --osscan-guess target
```

---

# Aggressive Scan

```bash
nmap -A target
```

Includes:

- OS Detection
- Version Detection
- Default NSE Scripts
- Traceroute

---

# Nmap Scripting Engine (NSE)

```bash
nmap -sC target
```

```bash
nmap --script default target
```

```bash
nmap --script vuln target
```

```bash
nmap --script safe target
```

```bash
nmap --script discovery target
```

```bash
nmap --script auth target
```

```bash
nmap --script brute target
```

```bash
nmap --script broadcast
```

```bash
nmap --script dos
```

```bash
nmap --script exploit
```

```bash
nmap --script external
```

```bash
nmap --script malware
```

```bash
nmap --script intrusive
```

```bash
nmap --script ftp*
```

```bash
nmap --script smb*
```

```bash
nmap --script http*
```

```bash
nmap --script ssh*
```

```bash
nmap --script dns*
```

```bash
nmap --script smtp*
```

```bash
nmap --script snmp*
```

```bash
nmap --script mysql*
```

```bash
nmap --script redis*
```

---

# Useful NSE Examples

```bash
nmap --script http-title target
```

```bash
nmap --script http-enum target
```

```bash
nmap --script smb-os-discovery target
```

```bash
nmap --script smb-enum-shares target
```

```bash
nmap --script ftp-anon target
```

```bash
nmap --script ssh-hostkey target
```

```bash
nmap --script dns-brute target
```

```bash
nmap --script ssl-cert target
```

```bash
nmap --script ssl-enum-ciphers target
```

```bash
nmap --script vulners target
```

---

# Timing Templates

```bash
nmap -T0 target
```

```bash
nmap -T1 target
```

```bash
nmap -T2 target
```

```bash
nmap -T3 target
```

```bash
nmap -T4 target
```

```bash
nmap -T5 target
```

---

# Performance

```bash
nmap --min-rate 1000 target
```

```bash
nmap --max-rate 5000 target
```

```bash
nmap --min-parallelism 10 target
```

```bash
nmap --max-parallelism 100 target
```

```bash
nmap --host-timeout 30s target
```

---

# Firewall & IDS Evasion

```bash
nmap -f target
```

```bash
nmap -ff target
```

```bash
nmap -D RND:10 target
```

```bash
nmap -S spoofed_ip target
```

```bash
nmap -e eth0 target
```

```bash
nmap --source-port 53 target
```

```bash
nmap --data-length 25 target
```

```bash
nmap --randomize-hosts target
```

```bash
nmap --spoof-mac 0 target
```

---

# Output Formats

```bash
nmap -oN normal.txt target
```

```bash
nmap -oX output.xml target
```

```bash
nmap -oG output.gnmap target
```

```bash
nmap -oA report target
```

```bash
nmap -v target
```

```bash
nmap -vv target
```

---

# DNS

```bash
nmap -n target
```

```bash
nmap -R target
```

```bash
nmap --system-dns target
```

```bash
nmap --dns-servers 8.8.8.8 target
```

---

# IPv6

```bash
nmap -6 target
```

---

# Traceroute

```bash
nmap --traceroute target
```

---

# Resume Scan

```bash
nmap --resume scan.xml
```

---

# Scan Specific Protocols

```bash
nmap -sU -p 53 target
```

```bash
nmap -sS -p 80,443 target
```

```bash
nmap -sV -p 21 target
```

---

# Vulnerability Scan

```bash
nmap --script vuln target
```

```bash
nmap -sV --script=vuln target
```

---

# Common One-Liners

```bash
nmap -A target
```

```bash
nmap -Pn -A target
```

```bash
nmap -sV -O target
```

```bash
nmap -sC -sV target
```

```bash
nmap -Pn -sC -sV target
```

```bash
nmap -T4 -F target
```

```bash
nmap -T4 -A -v target
```

```bash
nmap -p- -T4 target
```

```bash
nmap -sS -sV -O -A target
```

```bash
nmap -sU -sV target
```

```bash
nmap -Pn -p- --min-rate 1000 target
```

```bash
nmap -oA scan_results target
```

---

# Help

```bash
nmap --help
```

```bash
man nmap
```

```bash
nmap --version
```

---

⭐ If you found this cheat sheet useful, consider giving this repository a star.
