# 🛡️ Nikto Scan – Web Application Vulnerability Scanner

## 📌 Target
**IP:** 192.168.1.110  
**Web App:** DVWA (Damn Vulnerable Web App)

---

## 🛠️ Tool Used
**Nikto** – A web server scanner which performs comprehensive tests against web servers for multiple vulnerabilities.

---

## 📤 Scan Command Used

nikto -h http://192.168.1.110 -output nikto-scan.txt

## 📄 Output Files

- **nikto-scan.txt**: Full vulnerability scan report  
- **nikto-output.png**: Screenshot of terminal during scan

---

## 🚨 Key Findings

- Outdated Apache version with known vulnerabilities  
- Directory indexing enabled  
- Possible XSS issues detected  
- HTTP methods allowed: GET, POST, OPTIONS  
- Cookie issues and security headers missing

---

## 📚 What I Learned

- Basics of automated web vulnerability scanning  
- Interpreting Nikto output for quick insights  
- Mapping findings to OWASP Top 10

---

## 🙋 About Me

I'm a Blue Teamer transitioning into Red Teaming, building real-world attack & defense labs.  
This module is part of my GitHub series: [RedTeam-WAF-Detection-Bypass-Lab](https://github.com/Aditya-Sec/RedTeam-WAF-Detection-Bypass-Lab)


