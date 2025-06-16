# 🛠️ Nmap Scan

## 🔎 Objective:
Perform port scanning and service detection on the target machine.

---

## ✅ Command Used:
nmap -sS -sV -T4 -p- -oN full-scan.txt 192.168.1.110

---

## 📄 Sample Findings:
- Port 80 open (Apache 2.4.41)
- Port 22 open (OpenSSH 8.2)
- No unexpected services detected

---

## 📸 Screenshot:
Add `nmap-output.png` in this folder once the scan is performed.

---

## 📁 Files in this folder:
- `full-scan.txt`: Raw output of Nmap
- `nmap-output.png`: Visual screenshot of result
