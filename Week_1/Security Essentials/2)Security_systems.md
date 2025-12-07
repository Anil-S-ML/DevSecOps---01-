# Lesson 03 — How to Secure Systems Against Attacks

## 1. Why Security Matters

Modern systems face continuous threats from attackers whose primary goals include:

###  Attackers Target:
- Customer data  
- Company data  
- Internal applications  
- User applications  

A successful breach can lead to financial loss, legal issues, and reputation damage.

---

## 2. Defense-in-Depth Mindset

**Defense-in-Depth (DiD)** is a layered security approach ensuring that even if one control fails, others continue to protect the system.

###  Principles:
- Multiple security layers  
- Isolation and containment  
- Limited blast radius  
- Continuous monitoring and alerting  

Even if one internal system is hacked, attackers should NOT gain access to all systems.

---

## 3. Application Security

Security must be enforced across the entire application stack.

###  Layers to Secure:
- **Frontend:** input validation, XSS/CSRF protection  
- **Backend:** authentication, authorization, rate limiting  
- **UI:** secure sessions, no sensitive data exposure  
- **Database:** encryption, backups, least privilege  
- **Runtime:** secure containers, patched dependencies  
- **Servers:** OS hardening, firewalls, disabled unused services  
- **Cloud Platform:** IAM, VPC isolation, monitoring tools  

Each layer forms part of the system’s overall security.

---

## 4. Security Posture

Describes how secure your systems, infrastructure, and practices are.

###  Includes:
- Application security  
- Infrastructure security  
- Monitoring and alerting  
- Incident response  
- Compliance and governance  

###  Goal:
Build systems that are:
- **Resilient** to attacks  
- **Monitored** continuously  
- **Designed for failures** with minimal impact  

A good security posture reduces risks, improves reliability, and enhances trust.

---
