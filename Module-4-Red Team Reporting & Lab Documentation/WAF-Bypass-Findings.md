# 🧪 WAF Bypass Techniques – Technical Findings Report

## 🔍 Target Web Application

- **IP:** `http://192.168.1.110`
- **Environment:** DVWA / Custom Lab Setup
- **Security Layer:** ModSecurity WAF detected (via WAFW00F)

---

## 🧰 Tools & Techniques Overview

| Tool / Method                | Objective                              | Status        |
|-----------------------------|----------------------------------------|---------------|
| Nmap                        | Port scanning & service detection      | ✅ Done        |
| WhatWeb                     | Web fingerprinting                     | ✅ Done        |
| Nikto                       | Basic web vuln scanner                 | ✅ Done        |
| WAFW00F                     | WAF detection                          | ✅ Done        |
| Burp Suite Repeater         | Manual bypass validation               | ✅ Done        |
| Payload Obfuscation         | Split payloads, reversed/encoded       | ✅ Bypassed    |
| Header Tampering            | Faked origin/IP via headers            | ✅ Bypassed    |
| FFUF/WFuzz                  | Path + parameter fuzzing               | ✅ Bypassed    |
| Unicode/Base64 Encoding     | WAF rule evasion via transformations   | ✅ Partial     |
| Regex Pattern Detection     | Simulated custom rule testing          | ✅ Done        |

---

## 🧬 Observations Per Technique

### 🔹 1. Payload Chaining

- Combined Base64 + Unicode + traversal (e.g. `%2e%2e%2fetc/passwd`)
- **Result:** Partial bypass, some payloads allowed by WAF
- **Lesson:** Multi-layer encoding increases success

---

### 🔹 2. Header Tampering

- Used `X-Forwarded-For: 127.0.0.1` and `Referer: internal`
- **Result:** WAF bypassed access control based on IP filtering
- **Lesson:** Improper origin validation = critical misconfiguration

---

### 🔹 3. Fuzzing

- Paths: `/admin`, `/backup`, `/debug`
- Params: `token=`, `bypass=`, `debug=true`
- **Result:** Discovered hidden admin page and upload interface
- **Lesson:** WAF didn’t block all brute-force paths or params

---

### 🔹 4. Manual Payload Testing

- Used Burp Repeater to send variants of:
  - `' OR 1=1--`
  - `<script>alert(1)</script>`
  - Obfuscated headers and Unicode
- **Result:** Some responses returned 200 OK
- **Lesson:** Manual testing verifies automation results

---

### 🔹 5. Base64 + Unicode Bypass

- Transformed XSS payloads using Base64 and Unicode
- **Result:** Encoded payloads bypassed regex filters
- **Lesson:** Signature-based filtering is weak against encoding

---

### 🔹 6. Regex-Based Filtering

- Tested simulated WAF rules like:
  - `<script>`, `UNION SELECT`, `../`
- **Result:** Default regex filters caught obvious patterns but failed when payloads were encoded
- **Lesson:** Real WAF filters need layered detection logic

---

## 🧠 Summary of WAF Behavior

| Detection Type   | Result                   |
|------------------|--------------------------|
| Raw Payloads     | Mostly Blocked (403)     |
| Encoded Payloads | Partially Allowed        |
| Header Tampering | Bypassed access controls |
| Obfuscation      | Bypassed simple filters  |

---

## ✅ Key Learning Outcomes

- WAFs are often misconfigured and rely heavily on pattern-based detection
- Encoding + header manipulation = highly effective bypass strategy
- Tools like Burp Suite, FFUF, and WAFW00F are essential for testing defense depth
- Manual validation is a must after automated testing

---

📌 **Disclaimer:** This report is based on simulated penetration testing in a legal, isolated lab environment. No real systems were harmed.

🙋 Author: [Aditya Goswami](https://www.linkedin.com/in/aditya-kumar-goswami)  
🔗 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
