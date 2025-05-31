# 🪟 Windows Fundamentals Part 3 — TryHackMe Room Writeup

**Author:** CryptoRapt0r  
**Platform:** [TryHackMe.com](https://tryhackme.com)  
**Room:** [Windows Fundamentals 3](https://tryhackme.com/room/windowsfundamentals3)  
**Difficulty:** �\dfe2 Easy  
**Type:** Walkthrough

---

## 🌟 Goal

Understand Windows system security features like updates, antivirus, firewall, and built-in tools such as BitLocker, SmartScreen, and Volume Shadow Copy Service.

---

## 🛠️ Tools Used

* TryHackMe Browser VM  
* Windows Server 2019  
* Windows Settings and Control Panel  
* Windows Defender, BitLocker, VSS, and built-in security modules

---

## 🧽 Steps

### 1. Windows Updates

* Delivered through "Update & Security" in Settings.
* Uses the concept of **Patch Tuesday** (2nd Tuesday of the month).
* Can be accessed via:  
  `control /name Microsoft.WindowsUpdate`
* Admins can control update policies — e.g., disabling automatic updates in an org.

---

### 2. Windows Security Dashboard

* Found under: `Settings > Update & Security > Windows Security`.
* Centralized panel showing status of protection areas:
  * **Virus & Threat Protection**
  * **Firewall & Network Protection**
  * **App & Browser Control**
  * **Device Security**
* Color indicators: Green (OK), Yellow (Attention), Red (Immediate action)

---

### 3. Virus & Threat Protection

* Built-in antivirus: **Windows Defender**
* Offers:
  * Quick, Full, Custom scans
  * History of threats
  * Automatic protection
* **Real-time Protection**: Must be ON to auto-block malware (off by default in the VM).

---

### 4. Firewall & Network Protection

* Controls incoming/outgoing traffic by network profile:
  * **Domain**
  * **Private**
  * **Public** (e.g., public Wi-Fi – most restrictive)
* Settings found in:
  * `Control Panel > Windows Defender Firewall`
  * `wf.msc` for advanced rules

---

### 5. App & Browser Control

* Uses **Microsoft Defender SmartScreen** to detect:
  * Phishing attempts
  * Malicious files from internet
* Has Exploit Protection built-in to defend against memory-based exploits
* Example: SmartScreen may block `.exe` from unknown sources

---

### 6. Device Security

* **Core Isolation** and **Memory Integrity** protect low-level system memory
* **Security Processor (TPM)**:
  * Stores cryptographic keys
  * Used with BitLocker for disk encryption
* Not all features shown on VM as it’s Server edition without compatible hardware

---

### 7. BitLocker

* Encrypts entire drives to protect against data theft
* Most effective with **TPM 1.2 or higher**
* If TPM is missing, uses a **Startup Key** stored on USB
* Not available in TryHackMe VM, but concept is crucial for Windows security

---

### 8. Volume Shadow Copy Service (VSS)

* Creates backup snapshots of files at specific points in time
* Can be configured via:  
  `System > System Protection > Configure`
* Used for:
  * Restoring previous versions
  * Creating restore points
  * Disaster recovery

---

## 🧠 Takeaways

* Gained insight into how Windows updates and secures itself
* Learned to monitor and configure protection settings via Windows Security
* Explored built-in antivirus, firewall, and drive encryption
* Understood the role of TPM in enterprise-grade security
* Saw how VSS provides versioning and backup restore capabilities

---

🚀 Up next: Deep dive into **PowerShell**, **Windows Event Logs**, and **auditing mechanisms** in future Windows rooms. Stay sharp, and stay secure!
