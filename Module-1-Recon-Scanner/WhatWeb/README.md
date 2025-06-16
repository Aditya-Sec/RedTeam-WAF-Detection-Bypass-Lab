# 🔍 WhatWeb – Web Technology Fingerprinting

## 🧾 Objective:
Identify web technologies and configurations used by the target application (DVWA) hosted on `192.168.1.110`.

---

## 🛠 Tool Used:
- **WhatWeb**: A fast and powerful tool for identifying technologies used by websites.
  - Official site: [https://github.com/urbanadventurer/WhatWeb](https://github.com/urbanadventurer/WhatWeb)

---

## 🖥️ Target Information:
- **Target IP:** `192.168.1.110`
- **Application:** Damn Vulnerable Web Application (DVWA)

---

## 📄 Scan Command Used:
```bash
whatweb -a 3 http://192.168.1.110
📂 Output Files:
whatweb-output.txt: Full textual output of the WhatWeb scan.

whatweb-output.png: Bar chart visualizing the detected technologies.

🧠 Key Detections:
Technology	Detected
Apache 2.4.29	✅ Yes
PHP 7.2.24	✅ Yes
DVWA Title	✅ Yes
Ubuntu OS	✅ Yes
HTML5	✅ Yes
Meta Generator	✅ Yes
X-Frame-Options	✅ Yes
X-XSS-Protection	✅ Yes

📌 Insights:
DVWA is running on Apache with PHP on Ubuntu OS.

Uses modern HTTP headers for basic security (XSS protection, frame options).

Ideal target for further WAF fingerprinting and bypass exercises.

🙋 About Me:
I'm a Blue Teamer transitioning into Red Teaming, building real-world attack & defense labs.
This module is part of my GitHub series: [`RedTeam-WAF-Detection-Bypass-Lab`](https://github.com/Aditya-sec/RedTeam-WAF-Detection-Bypass-Lab)
[![Connect on LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/www.linkedin.com/in/aditya-kumar-goswami)



