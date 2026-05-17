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

### Nmap Scan
scan du réseau afin de decouvrire tout les machines qui sont dans le réseai ainsi que des ports ouverts.

<img width="1362" height="763" alt="Capture d’écran du 2026-05-12 12-08-02" src="https://github.com/user-attachments/assets/41ed317f-751e-478e-a310-6c0bd527d8d3" />

<img width="1362" height="763" alt="Capture d’écran du 2026-05-12 12-20-25" src="https://github.com/user-attachments/assets/5a92ad43-ed47-4240-aa41-27268c309197" />

### OWASP ZAP Alerts

1. Installer Zapproxy

les commandes au quel nous pouvons installer le zapproxy dans kali linux
~~~fraper
sudo apt update
sudo apt install zaproxy -y
~~~
puis lance :
~~~fraper
 zaproxy
~~~
2. Installer OWASP Juice Shop

Étape 1 : installer Docker
~~~fraper
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
~~~
~~~fraper
sudo usermod -aG docker $USER
~~~
puis rédemare la session

Étape 2 : lancer Juice Shop
~~~fraper
docker pull bkimminich/juice-shop
docker run -d -p 3000:3000 bkimminich/juice-shop
~~~
Lance ZAP
Dans ZAP → “Automated Scan”
Mets : http://localhost:3000

<img width="1362" height="763" alt="Capture d’écran du 2026-05-13 10-41-58" src="https://github.com/user-attachments/assets/df0db5bc-e0d3-434c-8fe1-d578261becc8" />

Lance le scan
Tu vas voir des vulnérabilités comme :
XSS,
SQL Injection,
mauvaises configurations

<img width="1362" height="763" alt="Capture d’écran du 2026-05-13 11-06-31" src="https://github.com/user-attachments/assets/a599bfd5-4eee-436d-a3e6-b8f3823f38dd" />

<img width="1362" height="763" alt="Capture d’écran du 2026-05-13 11-07-06" src="https://github.com/user-attachments/assets/f129c20a-47ec-4240-818e-47d9f63959f9" />

<img width="1362" height="763" alt="Capture d’écran du 2026-05-13 11-07-34" src="https://github.com/user-attachments/assets/1b5c5e4d-0d51-4d46-940b-e8b79ea4dbbc" />

<img width="1362" height="763" alt="Capture d’écran du 2026-05-13 11-09-16" src="https://github.com/user-attachments/assets/9315dc5e-32eb-4262-9049-7f141ec7c6ec" />

