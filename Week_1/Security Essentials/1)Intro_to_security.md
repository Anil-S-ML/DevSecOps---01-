# Lesson 01: Introduction to Security (DevSecOps)

##  Learning Objectives
- Understand limitations of traditional security practices  
- Learn what DevSecOps is and how it solves those limitations  
- Identify key DevSecOps concepts  
- Understand roles & responsibilities in a DevSecOps culture  

---

## 1. The Problem with Traditional Security

Traditional software development treats security as a **final step** before deployment.  
This creates several challenges:

### **Problems**
- Security issues are found very late in the lifecycle  
- Fixing vulnerabilities becomes expensive and time-consuming  
- Security acts as a *bottleneck* slowing down releases  
- Developers and Ops teams treat security as “someone else’s job”  
- Manual security checks cause delays  
- Attack surface increases when security isn’t continuous  

### **Why this approach fails**
- Modern apps use microservices, containers, cloud infra  
- Attackers exploit small misconfigurations quickly  
- Fast release cycles require **security to be as agile as DevOps**

---

## 2. What is DevSecOps?

**DevSecOps = Development + Security + Operations**

It integrates security throughout the software development lifecycle —  
from design → development → testing → deployment → operations.

### Core idea:
Security should be:
- **Built-in**, not bolted-on  
- **Continuous**, not one-time  
- **Automated**, not manual  
- **Shared**, not siloed  

### “Shift-Left” Security
Move security checks to earlier stages:
- during coding  
- during commit  
- during build  
- during automated tests  

This reduces risk and cost dramatically.

---

## 3. Why DevSecOps Matters (Benefits)

| Benefit | Explanation |
|--------|-------------|
| **Faster and safer releases** | Integrated security avoids last-minute delays |
| **Early vulnerability detection** | Issues caught during code stage |
| **Lower fix cost** | Cheaper to fix early |
| **Better collaboration** | Dev, Ops, and Security work together |
| **Reduced attack surface** | Continuous scanning reduces risk |
| **Compliance automation** | Meets ISO, PCI, SOC2 standards easily |

---

## 4. Key Concepts in DevSecOps

### **1. Continuous Security**
Security tools run automatically in CI/CD:
- Static Code Analysis (SAST)  
- Dependency Scanning (SCA)  
- Secrets scanning  
- Container image scanning  
- IaC (Terraform/Helm) scanning  

### **2. Secure-by-Design**
Security included from architecture/design phase.

### **3. Automation**
Automating security checks using:
- GitHub Actions  
- GitLab CI  
- Jenkins  
- Azure DevOps  

### **4. Continuous Monitoring**
Once deployed, monitor:
- Logs  
- Alerts  
- Runtime security  
- Audit trails  

### **5. Security as Culture**
Security is everyone's responsibility.

---

## 5. Roles & Responsibilities in DevSecOps

### **Developers**
- Write secure code  
- Fix vulnerabilities early  
- Follow secure coding guidelines  

### **Operations / DevOps Engineers**
- Maintain secure CI/CD pipelines  
- Enforce least privilege access  
- Secure infrastructure & configurations  

### **Security Engineers**
- Define security policies  
- Manage security tools  
- Review vulnerabilities  
- Educate teams  

### **Everyone**
- Share responsibility  
- Report risks  
- Follow standard security practices  

---

## 6. DevOps vs DevSecOps

| DevOps | DevSecOps |
|--------|-----------|
| Focus on speed | Focus on speed **with** security |
| Security at the end | Security at every stage |
| Dev fixes functional bugs | Dev also fixes security issues |
| CI/CD pipeline | CI/CD + automated security checks |

---

## Summary

- Traditional security is slow, expensive, and risky  
- DevSecOps integrates security into every DevOps stage  
- Automation + collaboration = secure & fast delivery  
- Security is a **shared responsibility**  
- DevSecOps is a mix of culture, processes, and automation  

---


