# 🔍 WAFW00F

## 📌 Target
- **URL/IP:** http://192.168.1.110  
- **Tool Used:** WAFW00F

## ⚙️ Command Executed
bash'''
wafw00f http://192.168.1.110 -a -v > wafw00f-scan.txt

## 📂 Output Files
- `wafw00f-scan.txt` – Complete WAF detection result  
- `wafw00f-output.png` – Terminal screenshot during execution

## 🚨 Detection Summary
- Detected possible WAF vendor(s): **ModSecurity**  
- WAF fingerprinting based on response patterns and headers  
- Site might be protected against generic attacks (e.g., SQLi, XSS)

## 📚 What I Learned
- Basics of WAF detection via passive and active fingerprinting  
- Importance of identifying WAFs before performing scans  
- Mapping WAF defenses to bypass techniques in future modules

## 🙋 About Me
I’m a Blue Teamer transitioning into Red Teaming, building real-world attack & defense labs.  
This module is part of my GitHub series: `RedTeam-WAF-Detection-Bypass-Lab`

🔗 Connect with me on [LinkedIn](https://www.linkedin.com/in/aditya-kumar-goswami)  
📁 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
