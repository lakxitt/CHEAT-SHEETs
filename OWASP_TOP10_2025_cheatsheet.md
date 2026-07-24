# 🛡️ OWASP Top 10:2025 Cheat Sheet

> A quick reference guide to the **OWASP Top 10:2025**, the industry-standard awareness document for the most critical web application security risks.

> **Audience:** Developers • Pentesters • Security Engineers • DevSecOps • Students

---

# 📚 Table of Contents

- Overview
- OWASP Top 10:2025
- Risk Summary
- Prevention Checklist
- Secure Development Tips
- Useful Tools
- Best Practices

---

# 📖 What is OWASP Top 10?

The **OWASP Top 10** is a globally recognized list of the **most critical web application security risks**. It helps developers and security professionals build secure applications by focusing on the most impactful vulnerability categories.

---

# 🔥 OWASP Top 10:2025

| ID | Category | Description |
|----|----------|-------------|
| **A01** | Broken Access Control | Users can access resources or perform actions they should not be allowed to. |
| **A02** | Security Misconfiguration | Insecure default settings, exposed services, unnecessary features, or poor configurations. |
| **A03** | Software Supply Chain Failures | Risks from vulnerable dependencies, build systems, package repositories, and third-party software. |
| **A04** | Cryptographic Failures | Weak encryption, poor key management, or sensitive data exposed due to improper cryptography. |
| **A05** | Injection | Untrusted input causes commands or queries to execute unexpectedly (SQL, NoSQL, OS Command, etc.). |
| **A06** | Insecure Design | Missing or ineffective security controls caused by poor architecture or design decisions. |
| **A07** | Authentication Failures | Weak authentication, credential management, or session handling. |
| **A08** | Software & Data Integrity Failures | Untrusted software updates, insecure CI/CD pipelines, unsigned code, or integrity verification failures. |
| **A09** | Security Logging & Alerting Failures | Missing or inadequate logging, monitoring, and incident detection. |
| **A10** | Mishandling of Exceptional Conditions | Improper error handling, failure states, resource exhaustion, or applications that fail insecurely. |

---

# 📌 Risk Summary

## A01 - Broken Access Control

### Common Issues

- IDOR
- Privilege Escalation
- Missing Authorization
- Forced Browsing
- Directory Traversal

### Prevention

- Server-side authorization checks
- Deny by default
- Least privilege
- Validate every request

---

## A02 - Security Misconfiguration

### Common Issues

- Default passwords
- Debug mode enabled
- Open cloud storage
- Directory listing
- Missing security headers

### Prevention

- Harden servers
- Remove unused services
- Secure configurations
- Automate configuration checks

---

## A03 - Software Supply Chain Failures

### Common Issues

- Vulnerable packages
- Malicious dependencies
- Compromised build pipelines
- Dependency confusion
- Insecure package repositories

### Prevention

- Pin dependency versions
- Generate SBOMs
- Verify package signatures
- Scan dependencies regularly

---

## A04 - Cryptographic Failures

### Common Issues

- Weak hashing
- Hardcoded keys
- Plaintext passwords
- Weak TLS
- Poor key storage

### Prevention

- AES-256
- TLS 1.2+
- Argon2 / bcrypt
- Secure key management
- Encrypt sensitive data

---

## A05 - Injection

### Examples

- SQL Injection
- Command Injection
- LDAP Injection
- XPath Injection
- NoSQL Injection

### Prevention

- Prepared Statements
- Parameterized Queries
- Input Validation
- Output Encoding
- Least Privilege Database Accounts

---

## A06 - Insecure Design

### Common Issues

- Missing threat modeling
- Poor business logic
- No rate limiting
- Weak workflows
- Missing abuse cases

### Prevention

- Threat modeling
- Secure design reviews
- Security requirements
- Abuse case analysis

---

## A07 - Authentication Failures

### Common Issues

- Weak passwords
- Credential stuffing
- Session fixation
- Predictable session IDs
- Missing MFA

### Prevention

- Multi-Factor Authentication
- Strong password policies
- Secure session management
- Account lockout
- Secure cookies

---

## A08 - Software & Data Integrity Failures

### Common Issues

- Unsigned updates
- Insecure deserialization
- CI/CD compromise
- Tampered artifacts
- Trusting unverified data

### Prevention

- Code signing
- Verify update integrity
- Secure CI/CD pipelines
- Validate serialized data

---

## A09 - Security Logging & Alerting Failures

### Common Issues

- No audit logs
- Missing alerts
- Logs easily modified
- Insufficient monitoring
- Delayed incident detection

### Prevention

- Centralized logging
- SIEM integration
- Alert critical events
- Protect log integrity
- Regular log reviews

---

## A10 - Mishandling of Exceptional Conditions

### Common Issues

- Stack traces exposed
- Information leakage
- Fail-open behavior
- Resource exhaustion
- Unhandled exceptions

### Prevention

- Graceful error handling
- Generic user-facing errors
- Fail securely
- Validate exceptional paths
- Test failure scenarios

---

# 🛠 Useful Security Tools

| Tool | Purpose |
|------|---------|
| Burp Suite | Web Application Testing |
| OWASP ZAP | Automated Web Scanner |
| Nmap | Network Discovery |
| Nikto | Web Server Scanner |
| sqlmap | SQL Injection Testing |
| ffuf | Content Discovery |
| Trivy | Container & Dependency Scanning |
| Semgrep | Static Code Analysis |
| SonarQube | Code Quality & Security |
| Dependency-Check | Dependency Vulnerability Detection |

---

# ✅ Secure Development Checklist

- Validate all input
- Encode all output
- Use parameterized queries
- Implement least privilege
- Enable MFA
- Encrypt sensitive data
- Secure session management
- Patch dependencies
- Disable debug mode
- Configure security headers
- Log security events
- Monitor suspicious activity
- Perform regular code reviews
- Conduct penetration testing
- Automate security scanning

---

# 🔐 Security Headers

```http
Content-Security-Policy

Strict-Transport-Security

X-Content-Type-Options

X-Frame-Options

Referrer-Policy

Permissions-Policy
```

---

# 🧪 Secure SDLC

```
Requirements

↓

Threat Modeling

↓

Secure Design

↓

Secure Coding

↓

Code Review

↓

SAST

↓

Dependency Scan

↓

DAST

↓

Penetration Testing

↓

Deployment

↓

Continuous Monitoring
```

---

# ⭐ Quick Reference

| Category | Primary Defense |
|----------|-----------------|
| Access Control | Authorization Checks |
| Misconfiguration | Secure Defaults |
| Supply Chain | Dependency Management |
| Cryptography | Strong Encryption |
| Injection | Parameterized Queries |
| Design | Threat Modeling |
| Authentication | MFA + Strong Sessions |
| Integrity | Code Signing |
| Logging | SIEM + Monitoring |
| Error Handling | Fail Securely |

---

# 📖 Useful Resources

- OWASP Top 10
- OWASP Cheat Sheet Series
- OWASP ASVS
- OWASP Web Security Testing Guide (WSTG)
- OWASP Developer Guide

---

# 📜 License

MIT License

---

⭐ **If you found this cheat sheet useful, consider giving the repository a star!**
