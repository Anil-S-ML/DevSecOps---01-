# Lesson 08 — Security in Layers

Security in Layers, also known as **Defense-in-Depth**, is a strategy that protects systems using multiple independent security controls.  
Instead of relying on a single protective mechanism, each layer adds a barrier that attackers must bypass—significantly reducing the chance of full compromise.

The principle is simple:

**If one layer is breached, the remaining layers should still protect the system.**

---

# Layered Security Approach

A secure system must have protections at **multiple levels**, covering identity, network, applications, logging, and monitoring.

---

## 1. Access Management

Controlling **who** can access **what** is the foundation of security.

### Key Components
- **Role-Based Access Control (RBAC)**  
  Users receive permissions based on roles (Admin, Developer, Auditor, etc.).

- **Principle of Least Privilege (PoLP)**  
  Users and services should receive **only the minimum access** required to perform their tasks.

### Benefits
- Reduces impact of compromised accounts  
- Limits lateral movement inside the system  
- Prevents privilege escalation  

---

## 2. Network Security

Controls at the network layer restrict how traffic flows into and within the system.

### Key Security Mechanisms
- **Firewalls**  
  Block unwanted or malicious traffic; enforce ingress and egress rules.

- **Network Segmentation**  
  Splits the network into smaller isolated environments (e.g., production, staging, dev).  
  Compromise in one segment does not affect the others.

- **Zero-Trust Model**  
  Assumes no user or system is inherently trusted.  
  Every request must be authenticated, authorized, and encrypted.

### Benefits
- Reduces attack surface  
- Protects sensitive services from direct exposure  
- Limits the blast radius of attacks  

---

## 3. Application Security

Application-level protections guard against vulnerabilities commonly exploited by attackers.

### Key Controls
- **Input Validation**  
  Ensures only safe and expected input is processed.  
  Prevents SQL injection, XSS, and command injection.

- **Secure Coding Practices**  
  Avoid unsafe functions, hard-coded secrets, or insecure patterns.

- **Dependency Scanning**  
  Identify and fix vulnerabilities in third-party libraries and frameworks.

### Benefits
- Prevents exploitation of app logic  
- Reduces code-level vulnerabilities  
- Strengthens trust in application workflows  

---

## 4. Logging

Logging helps record critical information about system behavior and security events.

### What to Log
- Authentication attempts  
- Failed logins  
- Errors and exceptions  
- Changes to important configurations  
- Administrative actions  

### Benefits
- Provides forensic data after an incident  
- Helps trace user activity  
- Supports compliance requirements  

---

## 5. Monitoring

Monitoring ensures continuous visibility into system health and security status.

### Key Capabilities
- **Intrusion Detection**  
  Identifies abnormal access patterns or behavior.

- **Alerting**  
  Notifies administrators immediately about suspicious events or system failures.

- **Real-Time Observability**  
  Tracks performance metrics and error spikes to identify attacks like DDoS or brute force.

### Benefits
- Enables fast response to threats  
- Helps detect attacks before damage occurs  
- Reduces downtime and incident impact  

---

# Goal of Layered Security

The ultimate purpose of layered security is:

### **Even if one security layer is breached, attackers should NOT gain full access to the system.**

A failure in:
- Access control  
- Network segmentation  
- Application logic  
- Logging  
- Monitoring  

should not result in complete system compromise.

Each layer acts as a backup protection mechanism, increasing overall resilience and reducing risk.

---

