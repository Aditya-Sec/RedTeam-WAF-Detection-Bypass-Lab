# 📚 Custom Payload Log Analysis

## 🎯 Objective
Analyze web server and WAF logs to identify how different payloads are processed, blocked, or allowed, especially when encoded (e.g., Base64, Unicode).

---

## 🧪 Environment Setup

- **Target IP:** http://192.168.1.110
- **Platform:** DVWA behind ModSecurity WAF
- **Tools Used:** Apache logs / Burp Suite / Encoding tools

---

## 📂 Output Files

📁 `logs/`
- `waf-access-log.txt`: Simulated WAF and access log entries  
- `bypass-test-results.txt`: Annotated notes about each payload and response  

📁 `screenshots/`
- `log-analysis-insights.png`: Side-by-side screenshot showing logs and bypass impact  

---

## 🧠 Key Learnings

- How WAFs respond to known and encoded payloads
- The effectiveness of Base64 in bypassing filter logic
- Pattern recognition in HTTP status codes (403 = blocked, 200 = allowed)

---

## ✅ Summary

| Payload                               | Encoded | Result   |
|---------------------------------------|---------|----------|
| `<script>alert(1)</script>`           | ❌ No   | ❌ Blocked |
| `PHNj...Pg==` (Base64 of XSS)         | ✅ Yes  | ✅ Allowed |
| `' OR 1=1--`                          | ❌ No   | ❌ Blocked |
| `JyBP...LQ==` (Base64 of SQLi)        | ✅ Yes  | ✅ Allowed |

---

## 🙋 About Me
I’m a Blue Teamer transitioning into Red Teaming, building real-world attack & defense labs.

🔗 [Connect on LinkedIn](https://www.linkedin.com/in/aditya-kumar-goswami)  
📁 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
