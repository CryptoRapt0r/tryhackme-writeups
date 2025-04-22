# 🦖 Defensive Security Intro — TryHackMe Room Writeup  
**Author:** CryptoRapt0r  
**Platform:** [TryHackMe.com](https://tryhackme.com)  
**Room:** [Defensive Security Intro](https://tryhackme.com/room/defensivesecurityintro)  
**Difficulty:** 🟢 Easy  
**Type:** Walkthrough  

---

## 🎯 Goal  
Learn the basics of defensive security and complete a hands-on SIEM challenge by identifying and escalating a malicious login event.

---

## 🧰 Tools Used  
- SIEM (Simulated)  
- IP Reputation Checker  
- TryHackMe platform interface  
- Threat intelligence tools (e.g., AbuseIPDB-style simulation)

---

## 🛠️ Steps  

### 1. Understand Defensive Security  
Reviewed concepts:  
- Preventing and detecting intrusions  
- Blue team responsibilities  
- SOC, Threat Intel, DFIR, Malware Analysis  

---

### 2. SIEM Dashboard Investigation  
Logged into the SIEM platform:  
- Discovered suspicious IP: `143.110.250.149`  
- Alert logs showed failed attempts → then a successful SSH login  

---

### 3. Reputation Check  
Searched IP on `ip-scanner.thm`  
- Result: **Malicious**  
- Confidence: 100%  
- Origin: 🇨🇳 China, Zhenjiang, Jiangsu  

---

### 4. Escalation  
Escalated the incident to appropriate staff:  
**SOC Team Lead: Will Griffin**  
→ Successfully handled incident, blocked IP

---

## 🏁 Flag  
**THM{THREAT-BLOCKED}**

![SIEM Dashboard](https://github.com/user-attachments/assets/your-screenshot.png)

---

## 🧠 Takeaways  
- SOC is the frontline of cyber defense  
- Not all alerts are threats—but analysis is critical  
- Escalating to the right team matters  
- Threat Intel helps validate suspicious behavior  

Another step toward mastering blue team fundamentals 🔹
