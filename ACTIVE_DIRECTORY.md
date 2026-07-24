# 🏢 Active Directory Cheat Sheet

> A quick reference guide covering the most important Active Directory (AD) concepts, components, authentication protocols, administration tools, and security basics.

> **Audience:** System Administrators, SOC Analysts, Blue Teams, Penetration Testers, and Cybersecurity Students.

---

# 📚 Table of Contents

- What is Active Directory?
- Active Directory Components
- Active Directory Structure
- Authentication
- Important Services
- Common Ports
- Common Tools
- User & Group Management
- PowerShell Commands
- Administrative Utilities
- Common Attacks
- Hardening Best Practices
- Important Terms

---

# 📖 What is Active Directory?

**Active Directory (AD)** is Microsoft's directory service that stores and manages information about users, computers, groups, printers, and other resources within a Windows domain.

### Main Functions

- Centralized Authentication
- Authorization
- User Management
- Computer Management
- Group Policy Management
- Resource Access Control

---

# 🏗 Active Directory Structure

```
Forest
│
├── Tree
│   │
│   ├── Domain
│   │    │
│   │    ├── Organizational Unit (OU)
│   │    │      ├── Users
│   │    │      ├── Computers
│   │    │      └── Groups
│   │
│   └── Domain
│
└── Tree
```

---

# 🧩 Active Directory Components

| Component | Description |
|----------|-------------|
| Forest | Highest AD container |
| Tree | Collection of related domains |
| Domain | Administrative boundary |
| OU | Organizes users and computers |
| Domain Controller (DC) | Authenticates users and stores AD database |
| Global Catalog (GC) | Stores searchable directory information |
| Group Policy (GPO) | Applies security and system configurations |
| Sites | Represents physical network locations |

---

# 👤 Active Directory Objects

- Users
- Groups
- Computers
- Printers
- Shared Folders
- Contacts
- Service Accounts
- Organizational Units

---

# 🔐 Authentication

### NTLM

- Older authentication protocol
- Challenge-response authentication
- Less secure
- Still supported for legacy systems

---

### Kerberos

- Default authentication protocol
- Ticket-based authentication
- More secure than NTLM

Flow

```
Client

↓

Authentication Server (AS)

↓

Ticket Granting Ticket (TGT)

↓

Ticket Granting Service (TGS)

↓

Service Ticket

↓

Access Resource
```

---

# 🖥 Domain Controller (DC)

Responsibilities

- Stores AD Database
- Authenticates Users
- Applies Group Policy
- Replicates Directory Information
- DNS Integration

---

# 📂 Organizational Unit (OU)

Used to organize:

- Users
- Groups
- Computers
- Policies

Example

```
Company

│

├── HR

├── IT

├── Finance

└── Management
```

---

# 👥 Group Types

| Type | Purpose |
|------|----------|
| Security Group | Permission management |
| Distribution Group | Email distribution |

---

# 🌍 Active Directory Services

| Service | Purpose |
|----------|---------|
| DNS | Name Resolution |
| LDAP | Directory Access |
| Kerberos | Authentication |
| SMB | File Sharing |
| RPC | Remote Communication |
| DFS | Distributed File System |

---

# 🔌 Important Ports

| Port | Service |
|------|----------|
| 53 | DNS |
| 88 | Kerberos |
| 135 | RPC |
| 137 | NetBIOS |
| 138 | NetBIOS |
| 139 | SMB |
| 389 | LDAP |
| 445 | SMB |
| 464 | Kerberos Password Change |
| 636 | LDAPS |
| 3268 | Global Catalog |
| 3269 | Secure Global Catalog |

---

# 🛠 Administrative Tools

| Tool | Purpose |
|------|----------|
| Active Directory Users and Computers (ADUC) | User and computer management |
| Active Directory Administrative Center | Modern AD management |
| Group Policy Management | Manage GPOs |
| DNS Manager | DNS administration |
| Event Viewer | Security logs |
| Server Manager | Server administration |

---

# 💻 PowerShell Commands

### Domain Information

```powershell
Get-ADDomain
```

---

### Forest Information

```powershell
Get-ADForest
```

---

### List Users

```powershell
Get-ADUser -Filter *
```

---

### List Computers

```powershell
Get-ADComputer -Filter *
```

---

### List Groups

```powershell
Get-ADGroup -Filter *
```

---

### Domain Controllers

```powershell
Get-ADDomainController -Filter *
```

---

### Search User

```powershell
Get-ADUser username
```

---

### User Properties

```powershell
Get-ADUser username -Properties *
```

---

### List OUs

```powershell
Get-ADOrganizationalUnit -Filter *
```

---

# 🔍 Useful Windows Commands

```cmd
whoami

hostname

systeminfo

net user

net group

net accounts

gpresult /r

nltest

nslookup

ipconfig /all
```

---

# 🔑 Important Active Directory Terms

| Term | Description |
|------|-------------|
| SID | Security Identifier |
| RID | Relative Identifier |
| ACL | Access Control List |
| ACE | Access Control Entry |
| SPN | Service Principal Name |
| GPO | Group Policy Object |
| TGT | Ticket Granting Ticket |
| TGS | Ticket Granting Service |
| OU | Organizational Unit |
| DC | Domain Controller |

---

# 🛡 Security Best Practices

- Use Multi-Factor Authentication (MFA)
- Disable unused accounts
- Apply Least Privilege
- Rotate passwords regularly
- Monitor failed logins
- Enable auditing
- Restrict Domain Admin membership
- Patch Domain Controllers
- Secure LDAP with LDAPS
- Backup Active Directory regularly

---

# 🚨 Common Active Directory Attacks

| Attack | Description |
|---------|-------------|
| Password Spraying | Try common passwords against many accounts |
| Kerberoasting | Request service tickets to crack service account passwords offline |
| AS-REP Roasting | Obtain crackable authentication data from misconfigured accounts |
| Pass-the-Hash | Authenticate using password hashes instead of plaintext passwords |
| Pass-the-Ticket | Reuse valid Kerberos tickets |
| Golden Ticket | Forge Kerberos TGT using the KRBTGT account hash |
| Silver Ticket | Forge service tickets for specific services |
| DCSync | Abuse replication privileges to request password hashes from a Domain Controller |
| LDAP Enumeration | Gather information from LDAP |
| SMB Enumeration | Discover shared resources and systems |

---

# 📋 Common Enumeration Commands

```powershell
Get-ADUser -Filter *

Get-ADComputer -Filter *

Get-ADGroup -Filter *

Get-ADDomain

Get-ADForest

Get-ADDomainController -Filter *

Get-ADOrganizationalUnit -Filter *
```

---

# ⭐ Quick Reference

```
Forest
│
├── Tree
│
├── Domain
│
├── OU
│
├── Users
│
├── Groups
│
└── Computers
```

Authentication

```
Kerberos

↓

TGT

↓

TGS

↓

Service Ticket
```

---

# 📜 License

MIT License

---

⭐ **If you found this cheat sheet useful, consider giving the repository a star!**
