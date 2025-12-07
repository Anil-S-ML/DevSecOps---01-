# Lesson 06 — OWASP Top 10 (Part 1)

OWASP (Open Web Application Security Project) is a global nonprofit organization focused on improving software security.  
One of its most influential contributions is the **OWASP Top 10**, a regularly updated list of the most critical web application security risks.

The Top 10 helps developers, architects, and security engineers understand the highest-impact vulnerabilities and how to prevent them.

---

## 1. Broken Access Control

Broken Access Control occurs when users can perform actions or access resources **outside their intended permissions**.

### How Broken Access Control Happens
- Users exceed their allowed privilege levels  
- Manipulating URLs or parameters to access admin or restricted pages  
- Missing authorization checks  
- Unauthorized exposure of sensitive data  
- Hijacking or misusing active sessions  

### Impact
- Data breaches  
- Privilege escalation  
- Unauthorized modifications or deletions  
- Full account compromise  

### Prevention
- Enforce strict access control checks on every request  
- Implement role-based access control (RBAC)  
- Deny-by-default security posture  

---

## 2. Cryptographic Failures

Previously called “Sensitive Data Exposure,” this category covers failures in protecting data at rest or in transit.

### Causes of Cryptographic Failures
- Weak or missing encryption  
- Hard-coded passwords, API keys, or secrets  
- Using insecure communication protocols  
- Poor key management practices  

### Impact
- Unauthorized data access  
- Exposure of personal and financial information  
- Credential leakage  
- Compliance violations (GDPR, PCI-DSS)

### Prevention
- Use modern encryption standards (TLS 1.3, AES-256)  
- Store secrets securely (Vault, KMS, environment variables)  
- Enforce HSTS and secure cookies  

---

## 3. Injection Attacks

Injection vulnerabilities occur when untrusted data is misinterpreted as part of a command or query, allowing attackers to execute unintended operations.

### Common Types of Injection
- SQL Injection  
- Template Injection  
- OS Command Injection  
- LDAP or NoSQL injection  

### Why Injection Happens
- Unsanitized user input  
- Dynamic query construction  
- Direct execution of user-supplied commands or templates  

### Prevention
- Validate all input strictly  
- Use parameterized queries and prepared statements  
- Avoid generating templates or commands directly from user input  

---

## 4. Insecure Design

Insecure Design refers to systemic security weaknesses at the architectural level—not just implementation bugs.

### Examples of Insecure Design
- Poor credential management strategies  
- Improper permission model or access flow  
- Weak infrastructure configuration  
- Lack of defense-in-depth and secure workflows  

### How to Address Insecure Design
- Perform **threat modeling** during design phase  
- Adopt secure design patterns  
- Document security requirements early  
- Build applications assuming attackers will try to exploit logic flaws  

---

# Lesson 07 — OWASP Top 10 (Part 2)

---

## 5. Security Misconfiguration

Security misconfigurations are one of the most common vulnerabilities and arise when systems are not securely set up.

### Examples
- Default usernames or passwords  
- Unnecessary open ports  
- Debug mode enabled in production  
- Improperly configured access controls  
- Revealing error messages that expose internal details  

### Prevention
- Harden configurations  
- Disable unnecessary features  
- Apply secure defaults  
- Regular configuration audits  

---

## 6. Vulnerable & Outdated Components

Applications often depend on external libraries, frameworks, and packages. If these components are outdated or vulnerable, your entire system becomes at risk.

### Signs You Are Vulnerable
- Not tracking component versions  
- Not scanning dependencies for known CVEs  
- Not testing updates before deployment  
- Relying on unsupported or unmaintained packages  

### Impact
- Remote code execution  
- Data theft  
- Application compromise  

---

## 7. Identification & Authentication Failures

Failures in authentication mechanisms allow attackers to impersonate users or access systems without proper verification.

### Examples
- Weak passwords allowed by the system  
- No Multi-Factor Authentication (MFA)  
- Storing passwords in plain text  
- Sessions not properly invalidated after logout  
- Session IDs exposed in URLs  

### Impact
- Account takeover  
- Privilege escalation  
- Fraudulent transactions  

### Prevention
- Enforce password policies  
- Implement MFA  
- Use secure hashing algorithms (bcrypt, Argon2)  
- Regenerate and invalidate session IDs correctly  

---

## 8. Software & Data Integrity Failures

This occurs when applications rely on untrusted or unverified components, updates, or data.

### Causes
- Using plugins, libraries, or modules from unverified sources  
- Automatic updates without integrity checks  
- Unsigned or tampered software releases  

### Impact
- Supply chain attacks  
- Malware injection  
- Complete system compromise  

### Prevention
- Validate integrity using checksums or signatures  
- Use trusted repositories  
- Avoid blind auto-update mechanisms  

---

## 9. Logging & Monitoring Failures

Without proper logging and monitoring, attacks may go undetected for long periods.

### Problems Caused by Poor Logging
- Inability to detect brute force attacks  
- No visibility into suspicious or abnormal behavior  
- No audit trail for investigations  
- Slow incident response  

### Prevention
- Enable centralized logging  
- Monitor login failures, privilege changes, and anomalies  
- Ensure logs are protected and retained securely  

---

## 10. Server-Side Request Forgery (SSRF)

SSRF vulnerabilities allow attackers to trick the server into making unintended requests to internal or external systems.

### Impact
- Accessing internal network services  
- Internal host and port scanning  
- Exposure of sensitive service metadata  
- Bypassing firewalls and network segmentation  

### Prevention
- Validate and sanitize all user-controlled URLs  
- Block internal IP ranges  
- Enforce allowlists for outbound requests  

---
