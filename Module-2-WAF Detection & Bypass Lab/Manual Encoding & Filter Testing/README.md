# 🧬 Manual Encoding & Filter Testing

## 🎯 Objective
Manually encode payloads to study how WAFs respond to non-standard input formats and evade signature-based detections.


## 🛠️ Tools Used
- Burp Suite Repeater
- CyberChef (encoding helper)
- Browser Developer Tools (for manual injection and header editing)



## 📍 Target
- **IP/URL:** http://192.168.1.110
- **Environment:** DVWA with ModSecurity or similar WAF protection



## 🔤 Encoded Payload Examples

| Attack Type      | Original Payload               | Encoded Version                                  |
|------------------|--------------------------------|--------------------------------------------------|
| **XSS (URL Enc.)**  | `<script>alert(1)</script>`    | `%3Cscript%3Ealert(1)%3C%2Fscript%3E`             |
| **XSS (Unicode)**   | `<script>`                    | `\u003Cscript\u003E`                             |
| **SQLi (Base64)**   | `' OR '1'='1`                 | `JTI3JTIwT1IlMjAnMSUzRCcx` (URL-safe Base64)     |
| **User-Agent Injection** | `User-Agent: evil<script>` | Header fuzzing to trigger filter response        |



## 📄 Output Files

- `encoded-payloads/encoding-tests.txt`  
  ➤ Contains original and encoded payloads tested during the session

- `screenshots/encoding-responses.png`  
  ➤ Screenshot showing request/response behavior from Burp Suite



## 🔍 Key Observations
- Some WAFs allow payloads with Unicode format
- WAFs block obvious XSS but fail to catch altered encodings
- Headers like `User-Agent` or `Referer` are overlooked in some filter setups



## 🧠 What I Learned
- Deep understanding of how encoding affects payload filtering
- Which encodings are effective against WAFs (ModSecurity, Cloudflare, etc.)
- Manual bypass logic before using automated fuzzers



## 🙋 About Me
I’m a Blue Teamer transitioning into Red Teaming, building real-world WAF attack & evasion labs.

🔗 [Connect on LinkedIn](https://www.linkedin.com/in/aditya-kumar-goswami)  
📁 GitHub: [Aditya-Sec](https://github.com/Aditya-Sec)
