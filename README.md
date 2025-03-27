# 🛡️ Vulnscan – Vulnerability Scanning Using Greenbone Security Assistant (GSA)

This project demonstrates vulnerability scanning using **Greenbone Security Assistant (GSA)** along with supporting tools like **Nmap**, **Nikto**, and **Wapiti**. Both authenticated and unauthenticated scans were launched from a Kali Linux attacker VM to evaluate vulnerabilities across a simulated environment. Results were verified via the GSA dashboard and supplemental CLI outputs.

---

## 📂 Project Structure

Vulnscan/<br/>
├── README.md<br/>
├── vulnscan.png<br/>
├── Vulnerability scanning using Greenbone Security Assistant.docx<br/>

---

## 🔧 Tools Used

- **Greenbone Security Assistant (GSA)** – GUI for configuring and reviewing vulnerability scans.
- **Nmap** – Host discovery and vulnerability probing via NSE scripts.
- **Nikto** – Basic web server scanner for misconfigurations and exposures.
- **Wapiti** – Web app vulnerability scanner (XSS, SQLi, etc.).
- **Kali Linux** – Used for launching scans and accessing GSA.

---

## 🚨 Scan Overview

### ✅ Setup & Launch

1. **Start GVM on Kali**  
   ```bash
   gvm-start
   
Access the GUI: https://127.0.0.1:9392

Configure Targets & Credentials
Add a new target with or without login creds in GSA UI.

Launch Scan from GSA
Monitor via Scans > Tasks.

🔎 Supporting Tools:
nmap --script vuln -sC -sV -O <target-ip>

nikto -h http://<target-ip>

wapiti http://<target-ip> -f html -o wapiti_report.html

📸 Evidence
GSA scans and CLI output samples:


📄 Full Walkthrough
See detailed methodology, screenshots, and tool output in the full write-up:
👉 Vulnerability scanning using Greenbone Security Assistant.docx

✅ Summary
This project reinforces:
Real-world vuln scanning workflows
The impact of authenticated vs unauthenticated assessments
Centralized reporting with GSA
Cross-validation with Nmap, Nikto, and Wapiti

