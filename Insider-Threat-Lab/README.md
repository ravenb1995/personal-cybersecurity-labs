# 🔐 Insider Threat Detection Lab

## 🧠 Objective
Simulate an insider threat attack (exfiltration of sensitive data) and detect it using Sysmon + Windows Event Logs.

---

## ⚙️ Tools Used
- Windows 10 VM
- Sysmon + SwiftOnSecurity config
- Event Viewer
- Kali Linux (analyst machine)
- Wireshark (optional)

---

## 🧪 Simulated Attack Steps
1. Opened `confidential.pdf` in HR folder
2. Sent via Gmail in Chrome
3. Copied to USB folder
4. Pinged `8.8.8.8` as fake C2 traffic

---

## 📝 Logs Collected
- Sysmon Event ID 1 (Process Creation)
- Event ID 3 (Network Connect)
- Event ID 11 (File Access)

---

## 📊 Timeline
| Time | Event |
|------|-------|
| 12:01 PM | Login |
| 12:05 PM | Opened file |
| 12:07 PM | Used Chrome to email |
| 12:10 PM | Copied to USB |
| 12:15 PM | Pinged external IP |

---

## 📸 Screenshots
_Add screenshots of the Event Viewer logs, file access, browser, and ping activity here._

---

## 🎯 Lessons Learned
This lab demonstrates how simple internal behaviors (file access + Gmail + USB) can show up in logs, giving SOC teams an opportunity to catch insider threats.
