# 🛡️  OWASP ZAP

## 📌 Target
- **URL/IP:** http://192.168.1.110
- **Tool Used:** OWASP ZAP (Zed Attack Proxy)

---

## ⚙️ Scan Method
Used **Automated Scan** feature from ZAP GUI to run passive and active scans on the DVWA target.

---

## 📂 Output Files
- `zap-scan.html`: Full vulnerability report in HTML
- `zap-output.png`: Screenshot of ZAP alerts and findings

---

## 🚨 Key Findings
- SQL Injection in login page
- XSS vulnerabilities in reflected inputs
- Session ID exposed in URL
- Missing security headers (CSP, X-Frame-Options)
- Cookie without Secure flag

---

## 📚 What I Learned
- Understanding of passive vs active scans in OWASP ZAP
- Interpreting risk levels: Informational, Low, Medium, High
- Identifying common web application flaws visually
- How ZAP maps to the OWASP Top 10

---

## 🙋 About Me
I'm a Blue Teamer transitioning into Red Teaming, and this is part of my GitHub project:
**RedTeam-WAF-Detection-Bypass-Lab**

🔗 [Connect with me on LinkedIn](https://www.linkedin.com/in/aditya-kumar-goswami)  
📁 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
