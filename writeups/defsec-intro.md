# 🛡️ TryHackMe: Defensive Security Intro — Writeup

Welcome to my writeup for the **Defensive Security Intro** room on TryHackMe.  
This was my second room in the series — a hands-on beginner walkthrough into blue team fundamentals.  

---

## ✅ Room Overview
- **Difficulty**: Easy
- **Type**: Walkthrough
- **Topics**: SOC, Threat Intelligence, Malware Analysis, DFIR
- **Flag**: `THM{THREAT-BLOCKED}`

---

## 🧠 Concepts Covered

### 🔵 Blue Team vs Red Team
- Blue Team = Defensive Security
- Tasks include monitoring, detection, logging, response, user training

### 🛡️ SOC (Security Operations Center)
- Detect & monitor malicious activity
- Respond to threats
- Use tools like **SIEM**

### 📊 Threat Intelligence
- Identify and track adversaries
- Understand attacker motives and techniques
- Examples: APTs, ransomware groups, nation-state actors

### 🔍 DFIR (Digital Forensics & Incident Response)
- **Digital Forensics**: Analyze disk, memory, network logs
- **Incident Response**: Preparation → Detection → Containment → Recovery

### 🦠 Malware Analysis
- Types: Virus, Trojan, Ransomware
- Static vs Dynamic Analysis

---

## 🖥️ Practical Task: Simulated SOC Scenario

### 🧾 Step-by-step:

1. **SIEM Dashboard**: Logged alert shows IP `143.110.250.149`
2. **Reputation Check**: IP confirmed 100% malicious (China Mobile ISP)
3. **Escalation**: Incident escalated to **SOC Team Lead**
4. **Result**: Flag captured `THM{THREAT-BLOCKED}` ✅

---

## 🧰 Tools Referenced

- `SIEM` dashboards
- `AbuseIPDB`, `Cisco Talos`, `IP-Scanner` (for reputation check)

---

## 📝 Lessons Learned
- Defensive security is not just about tools — it's about processes
- SOC work involves **investigation, correlation, and escalation**
- Knowing where to look and how to act quickly is crucial

---

## 📌 Notes & Resources

- 🔗 [Cisco Talos Intelligence](https://talosintelligence.com/)
- 🔗 [AbuseIPDB](https://www.abuseipdb.com/)
- 🔗 [TryHackMe](https://tryhackme.com)

---

Thanks for reading!  
Check out more labs and notes at 👉 [CryptoRapt0r.github.io](https://cryptorapt0r.github.io)

