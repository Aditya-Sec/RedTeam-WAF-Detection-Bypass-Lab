
# 🧾 Executive Summary – Red Team WAF Detection & Bypass Lab

## 📌 Objective
This Red Team simulation aimed to assess the effectiveness of Web Application Firewall (WAF) protection on a vulnerable web application hosted at `http://192.168.1.110`. The objective was to identify, fingerprint, and bypass WAF rules using various techniques.

---

## 🔍 Scope

- Perform reconnaissance and web fingerprinting using Nmap, WhatWeb, Nikto, and WAFW00F
- Detect WAF signatures and identify rule types (e.g., ModSecurity)
- Actively test WAF filtering mechanisms using obfuscation, fuzzing, header tampering, and encoding
- Document all payloads, detections, and evasion results in a structured format

---

## 🧪 Techniques Used

| Phase                 | Tools Used                              |
|----------------------|------------------------------------------|
| Recon & Fingerprinting | Nmap, WhatWeb, Nikto, WAFW00F           |
| WAF Fingerprinting    | WAFW00F, Manual Detection                |
| Bypass Techniques     | Burp Suite, FFUF, Payload Obfuscation   |
| Fuzzing & Encoding    | Unicode, Base64, Path Traversal         |
| Header Manipulation   | `X-Forwarded-For`, `Referer`, etc.      |

---

## 🔐 Summary of Findings

- **WAF Detected:** ModSecurity (via WAFW00F, response headers)
- **Filter Evasion Success:**
  - Base64 + Unicode payload chaining partially bypassed filters
  - Header tampering allowed access to restricted areas
  - Obfuscated payloads bypassed keyword-based regex detection
- **WAF Block Behavior:**
  - 403 Forbidden pages
  - Rate limiting observed during fuzzing attempts

---

## 🧠 Key Takeaways

- Many basic WAF rules can be bypassed with layered encoding and header manipulation
- Regex-based filters are predictable and can be fuzzed
- Combining multiple evasion techniques increases bypass success
- Manual validation (e.g., Burp Repeater) helps confirm impact

---

## 🙋 Author

- **Name:** Aditya Goswami  
- **GitHub:** [Aditya-Sec](https://github.com/Aditya-Sec)  
- **LinkedIn:** [aditya-kumar-goswami](https://www.linkedin.com/in/aditya-kumar-goswami)

---

📌 **Disclaimer:** This lab was performed in a safe and isolated test environment for educational purposes only. Unauthorized testing on real-world assets is illegal and unethical.
