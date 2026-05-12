# FUTURE_CS_01
Cyber Security Internship - Task 1
## Project Overview

This project was completed as part of the Cyber Security Internship program.

The objective of this task was to perform a vulnerability assessment on a vulnerable web application using industry-standard security tools and produce a professional security report.

---

## 🎯 Objectives

- Identify common web vulnerabilities
- Classify risks (Low / Medium / High)
- Analyze exposed security weaknesses
- Provide remediation recommendations
- Document findings professionally

---

## 🛠️ Tools Used

- Kali Linux
- Nmap
- OWASP ZAP (Passive Scan)
- Browser DevTools
- Canva (Report Design)
- GitHub

---

## 🌐 Target Environment

- OWASP Juice Shop

---

## 🔍 Methodology

### 1. Reconnaissance
Performed network and service discovery using Nmap.

### 2. Web Vulnerability Assessment
Used OWASP ZAP passive scanning to identify:
- Missing security headers
- Cookie security issues
- Information disclosure risks
- Potential XSS vulnerabilities

### 3. Browser Analysis
Inspected requests, cookies, and responses using Browser DevTools.

---

## 📊 Findings Summary

| Vulnerability | Risk Level | Impact |
|---------------|------------|--------|
| Missing Security Headers | Low | Weak browser protection |
| Potential XSS | Medium | Possible session theft |
| Information Disclosure | Medium | Sensitive information exposure |

---

## 🛡️ Recommendations

- Implement Content Security Policy (CSP)
- Enable HTTP Strict Transport Security (HSTS)
- Sanitize user inputs
- Secure cookies using HttpOnly and Secure flags
- Minimize sensitive information exposure

---

## 📷 Screenshots

### Nmap Scan
scan du réseau afin de decouvrire tout les machines qui sont dans le réseai ainsi que des ports ouverts.

<img width="1362" height="763" alt="Capture d’écran du 2026-05-12 12-08-02" src="https://github.com/user-attachments/assets/41ed317f-751e-478e-a310-6c0bd527d8d3" />


### OWASP ZAP Alerts
![ZAP Alerts](screenshots/zap_alerts.png)

### Browser DevTools Analysis
![DevTools](screenshots/devtools.png)

---

## 📄 Report

The full professional vulnerability assessment report is available in the `/report` folder.

---

## 👨‍💻 Author

Cyber Security Intern – Future Interns
