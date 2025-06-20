# 🛡️ Burp Suite – WAF Behavior Analysis

## 🎯 Target
- **IP/URL:** http://192.168.1.110
- **Tool Used:** Burp Suite Community Edition

## 🔍 Payload Testing

### Example Payloads:
- Reflected XSS: `<script>alert(1)</script>`
- SQL Injection: `' OR '1'='1`
- Command Injection: `; ls -la`
- Local File Inclusion: `../../etc/passwd`

### Observations:
- All input points filtered or returned HTTP 403
- `<script>` tags were encoded or stripped
- SQLi caused internal error logs
- Directory traversal blocked by ModSecurity

📄 Output Files:
- `payload-tests/reflected-xss.txt`
- `payload-tests/sql-injection.txt`
- `burp-logs/request-response-analysis.txt`

📷 Screenshots:
- `waf-xss-block.png`: WAF blocks script injection
- `waf-sqli-block.png`: WAF blocks SQL payload

## 📚 What I Learned
- Manual analysis shows WAF filters behavior changes per payload
- Burp Repeater is powerful for payload injection testing
- Observing status codes (403, 406) and header changes reveals protection

🙋 About Me
I’m a SOC Analyst transitioning into Red Teaming, testing WAFs manually in this series.

🔗 [Connect with me on LinkedIn](https://www.linkedin.com/in/aditya-kumar-goswami)  
📁 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
