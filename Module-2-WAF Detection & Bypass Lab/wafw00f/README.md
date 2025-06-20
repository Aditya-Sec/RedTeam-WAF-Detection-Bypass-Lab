# 🛡️ WAFW00F (WAF Bypass Analysis)

## 🎯 Objective
Identify the active WAF (Web Application Firewall) and analyze its detection pattern to prepare for bypass attempts.

## 🧪 Test Target
- **IP/URL:** http://192.168.1.110 (DVWA Lab)
- **Detected WAF in Module 1:** ModSecurity

---

## ⚙️ Commands Executed

wafw00f http://192.168.1.110 -a -v > wafw00f-bypass.txt

📄 Output Files
File Name	Description
wafw00f-bypass.txt	Full verbose WAF detection scan
wafw00f-bypass.png	Screenshot of terminal during scan

📊 Analysis Summary
WAF Detected: ModSecurity
Fingerprint based on:
HTTP header responses
Response body characteristics
HTTP status codes
Defense observed:
Blocking suspicious payloads (SQLi, XSS patterns)
Detecting common reconnaissance tools

🧠 What I Learned

WAFW00F can identify WAFs using both passive and active probes.
ModSecurity blocks specific patterns — useful for crafting bypass payloads.
Knowing the WAF rules helps in building tailored attacks for bypass.

📁 Folder Path Structure

RedTeam-WAF-Detection-Bypass-Lab/
└── Module-3-WAF-Bypass/
    └── Tool-1-WAFW00F/
        ├── wafw00f-bypass.txt
        ├── wafw00f-bypass.png
        └── README.md

🙋 About Me
I'm a Blue Teamer transitioning into Red Teaming, building real-world detection & bypass labs using tools like WAFW00F, Burp Suite, and Nuclei.

🔗 Connect on LinkedIn
📁 GitHub: Aditya-Sec

        

