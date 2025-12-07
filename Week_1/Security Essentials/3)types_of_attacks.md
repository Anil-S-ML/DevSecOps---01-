# Lesson 04 — Types of Security Attacks (Part 1)

Security attacks exploit weaknesses in human behavior, browser functionality, or server-side trust. Understanding these attacks helps design secure applications and mitigate risks effectively.

---

## 1. Phishing Attack

Phishing targets **humans**, not systems. Attackers deceive users into revealing sensitive information or installing malware.

### How Phishing Works
- **Personalized phishing emails** designed to look legitimate.  
- **Fake login pages** mimic real websites to steal credentials.  
- **Malicious links or attachments** install malware like keyloggers or ransomware.  
- **Data-stealing scripts** capture usernames, passwords, credit card information, or session tokens.

### Impact
- Account compromise  
- Unauthorized access to corporate systems  
- Financial theft  
- Data leaks and identity theft  

---

## 2. Cross-Site Scripting (XSS)

XSS occurs when attackers inject malicious scripts into trusted websites through unsanitized input.

### How XSS Happens
- Inserting scripts via **comments**, **input fields**, **URLs**, or **forms**.  
- Website fails to sanitize or escape user input.  
- Malicious code executes in the victim’s browser.

### Impact
- Theft of cookies, tokens, and sensitive data  
- Redirecting users to attacker-controlled sites  
- Executing actions as the user  
- Full session hijacking  

---

## 3. CSRF — Cross-Site Request Forgery

CSRF forces a victim’s browser to perform unintended actions while authenticated.

### How CSRF Works
1. User logs in to a trusted site (e.g., banking).  
2. Session cookies remain stored in the browser.  
3. User clicks a malicious link or visits a malicious page.  
4. Browser sends an authenticated request to the trusted site.  

### Impact
- Unauthorized money transfers  
- Changing user profile information  
- Password or email changes  
- Deleting accounts  

### Why It Works
Browsers automatically include cookies with requests, making it difficult for servers to distinguish malicious requests from legitimate ones.

---

## 4. SSRF — Server-Side Request Forgery

SSRF tricks the server into making unauthorized requests, often to internal systems not intended for public access.

### How SSRF Happens
- Attackers manipulate parameters like:  
  `?url=http://internal-service/admin`  
- Server fetches the URL without validation.  
- Attackers pivot through the server to reach protected internal systems.

### Targets
- Internal APIs  
- Admin dashboards  
- Private database endpoints  
- Cloud metadata services (AWS/GCP/Azure)

### Impact
- Exposure of internal network  
- Unauthorized access to sensitive resources  
- Credential theft (e.g., cloud instance tokens)  
- Potential remote code execution  

---

# Lesson 05 — Types of Security Attacks (Part 2)

Application ecosystems face additional risks from unvalidated input, insecure dependencies, weak authentication, and resource exhaustion attacks.

---

## 1. SQL Injection

SQL Injection occurs when raw user input is directly inserted into SQL queries.

### Why SQL Injection Happens
- Direct string concatenation in SQL queries  
- No input sanitization or validation  
- Failure to use parameterized queries  

### Impact
- Exfiltration of sensitive data  
- Modification or corruption of records  
- Deletion of tables or databases  
- Authentication bypass  
- Full database compromise  

---

## 2. Security Issues in Third-Party Libraries

Applications rely on numerous external packages that may introduce vulnerabilities.

### Risks
- Libraries may contain **known vulnerabilities** (CVEs).  
- Outdated or unmaintained dependencies pose hidden risks.  
- Attackers may exploit insecure transitive dependencies.  
- Supply chain attacks may distribute malicious packages.  

### Impact
- Remote code execution  
- Data leaks  
- Application compromise  

---

## 3. Weak Passwords / Brute Force Attacks

Weak authentication enables attackers to guess credentials by automating login attempts.

### Weak Practices
- Reusing the same password across multiple services  
- Using simple or predictable passwords (e.g., Password@123)  
- No multi-factor authentication  
- Poor organizational password policies  

### Attack Methods
- Brute force attacks trying all combinations  
- Dictionary attacks using common passwords  
- Credential stuffing from leaked password lists  

### Impact
- Account takeover  
- Privilege escalation  
- Lateral movement within systems  

---

## 4. DoS — Denial of Service Attack

A DoS attack overwhelms systems with traffic, preventing normal operation.

### How DoS Works
- Flooding applications with excessive requests  
- Consuming CPU, memory, network bandwidth, and disk I/O  
- Often executed through botnets in distributed attacks (DDoS)

### Impact
- Service unavailability  
- Financial and operational loss  
- SLA breaches  
- Reputation damage  

---

## 5. Security Principle — “Easier to Hack Than Defend”

Security is asymmetric: attackers only need one weakness, while defenders must secure every layer.

### Key Points
- Attackers need **one vulnerability** to exploit.  
- Defenders must secure **authentication**, **input validation**, **networks**, **servers**, **cloud**, and **dependencies**.  
- Increasing system complexity expands the attack surface.  
- Missed patches, misconfigurations, or outdated libraries frequently lead to compromise.  

### Why This Matters
This principle highlights the importance of:
- Continuous monitoring  
- Automated security testing  
- DevSecOps practices  
- Defense-in-depth strategies  

---

