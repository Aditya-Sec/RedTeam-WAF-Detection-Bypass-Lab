# ⚡ Nuclei

## 📌 Target
- **URL/IP:** http://192.168.1.110  
- **Tool Used:** Nuclei by ProjectDiscovery

---

## 🛠 Command Executed
```bash
nuclei -u http://192.168.1.110 -o nuclei-scan.txt -s critical,high,medium,low -v
```

---

## 📂 Output Files
- `nuclei-scan.txt`: Full vulnerability scan report  
- `nuclei-output.png`: Screenshot of terminal during scan

---

## 🚨 Key Findings
- **[critical]** Path Traversal Vulnerability (CVE-2021-41773)
- **[medium]** Apache HTTP Server Misconfiguration
- **[low]** Potential SSN exposure in test files

---

## 📚 What I Learned
- How to run fast and targeted scans using Nuclei
- Interpreting templated results and severity levels
- Mapping detected issues to known CVEs and MITRE ATT&CK
- Understanding low-hanging web misconfigurations

---

## 🙋 About Me
I'm a Blue Teamer transitioning into Red Teaming, building hands-on labs with real-world tools.
This module is part of my GitHub project: **RedTeam-WAF-Detection-Bypass-Lab**

🔗 [Connect with me on LinkedIn](https://www.linkedin.com/in/aditya-kumar-goswami)  
📁 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
