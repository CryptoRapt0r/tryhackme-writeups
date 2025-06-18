# 🌐 OWASP Top 10 Web App Vulnerabilities — TryHackMe Room Writeup

**Author:** CryptoRapt0r
**Platform:** [TryHackMe.com](https://tryhackme.com)
**Room:** OWASP Top 10 Web Application Vulnerabilities
**Difficulty:** 🟢 Easy
**Type:** Checklist Walkthrough

---

## 🎯 Goal

Practical overview and exploitation of the most critical web vulnerabilities defined by OWASP Top 10. Use this writeup as a checklist for real-world engagements.

---

## 🔧 Tools Used

* Burp Suite
* Firefox DevTools / Chrome DevTools
* curl / wget
* sqlmap / wfuzz / gobuster
* hashcat / john / CyberChef
* jwt.io / sqlite3 / netcat
* Exploit-DB / searchsploit

---

## 🛍️ Tasks Summary

### Task 1: Introduction

* No interaction needed.

---

### Task 2: Cryptographic Failures

* Look for exposed directories (`/assets`, `/backup`, etc.)
* Sensitive files: `.db`, `.bak`, `.sqlite`
* Extract hashes and crack them (e.g., `hashcat`, `john`)

✅ **Flag:** `THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl}`

---

### Task 3: Injection

* SQL Injection via classic `' OR 1=1-- -` techniques
* Command Injection via `passthru()` and inline bash (`$(whoami)`, etc.)
* Check GET/POST params that go to system commands

✅ **Flag:** `THM{Not_3ven_c4tz_c0uld_sav3_U!}`

---

### Task 4: Insecure Design

* No lockout mechanism on sensitive endpoints (e.g. password reset)
* Brute-force verification tokens across IPs
* Watch for logic flaws

✅ **Flag:** `THM{Not_3ven_c4tz_c0uld_sav3_U!}`

---

### Task 5: Security Misconfiguration

* Werkzeug console open on `/console`
* Execute `import os; print(os.listdir())`, `cat app.py`, etc.

✅ **Flag:** `THM{Just_a_tiny_misconfiguration}`

---

### Task 6: Vulnerable & Outdated Components

* Check software banner (e.g., `Nostromo 1.9.6`)
* Use `searchsploit` or Exploit-DB
* Adjust and launch the exploit script

✅ **Flag:** `THM{But_Its_n0t_my_f4ult!}`

---

### Task 7: Identification & Authentication Failures

* Re-register existing users with space prefix (`" admin"`, `"darren"`)
* Bypass to access existing content of privileged users

✅ **Flag (Darren):** `fe86079416a21a3c99937fea8874b667`
✅ **Flag (Arthur):** `d9ac0f7db4fda460ac3edeb75d75e16e`

---

### Task 8: Software & Data Integrity Failures

#### Software:

* Scripts linked from CDNs without SRI check
* Manipulate external libraries (e.g. jQuery)

#### Data:

* JWT tampering (alg: none + empty signature)
* Modify payload to `admin`

✅ **Flag:** `THM{Dont_take_cookies_from_strangers}`

---

### Task 9: Logging & Monitoring Failures

* Analyze logs
* Detect brute-force attempts, known payloads, user-agents

✅ **Attacker IP:** `49.99.13.16`
✅ **Attack type:** `Brute Force`

---

### Task 10: SSRF (Server-Side Request Forgery)

* Param like `server=` used to build backend request
* Intercept with your machine → retrieve API keys
* Access internal resources (e.g., `localhost/admin`)

✅ **Flag:** `THM{Hello_Im_just_an_API_key}`

---

## 🌟 Final Notes

Use this document as a quick-reference for testing critical OWASP Top 10 web issues. Adapt, extend, automate.

**Flags validate successful exploitation and confirm understanding.**

---

## 🏁 Final Flags

```
THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl}
THM{Not_3ven_c4tz_c0uld_sav3_U!}
THM{Just_a_tiny_misconfiguration}
THM{But_Its_n0t_my_f4ult!}
d9ac0f7db4fda460ac3edeb75d75e16e
fe86079416a21a3c99937fea8874b667
THM{Dont_take_cookies_from_strangers}
THM{Hello_Im_just_an_API_key}
```

---
