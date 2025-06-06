# 🖥️ Windows Command Line - TryHackMe Room Writeup

**Author:** CryptoRapt0r  
**Platform:** [TryHackMe.com](https://tryhackme.com)  
**Room:** [Windows Command Line](https://tryhackme.com/room/windowscommandline)  
**Difficulty:** 🟢 Easy  
**Type:** Walkthrough

---

## 🎯 Goal  
Learn the basic Windows CLI commands (`cmd.exe`) for system diagnostics, file and network management, and process handling.

---

## 🧰 Tools Used  
- Windows Command Prompt (`cmd.exe`)  
- SSH access via AttackBox  
- TryHackMe VM  

---

## 🛠️ Steps

### ✅ Task 1: Introduction  
- CLI is faster and more efficient than GUI in administration  
- Advantages: low resources, automation, remote management  
- SSH connection to the target machine:  
  ```bash
  ssh user@<MACHINE_IP>
  Password: Tryhackme123!
  ```

---

### 📊 Task 2: Basic System Information  
- `set` - environment variables  
- `ver` - OS version  
- `systeminfo` - detailed system information  
- Useful tricks:  
  - `command | more`  
  - `help`, `cls`

**Flags:**  
- OS Version: `10.0.20348.2655`  
- Hostname: `WINSRV2022-CORE`

---

### 🌐 Task 3: Network Troubleshooting  
- `ipconfig`, `ipconfig /all` - IP, DNS, DHCP  
- `ping example.com` - ICMP reachability  
- `tracert example.com` - route to host  
- `nslookup` - domain name resolution  
- `netstat` and `netstat -abon` - current connections and process PIDs

**Flags:**  
- MAC: `ipconfig /all`  
- Port 3389: `TermService`  
- Subnet: `255.255.0.0`.

---

### 📁 Task 4: File and Disk Management  
- Working with directories: `cd`, `dir`, `tree`.  
- Create/delete: `mkdir`, `rmdir`  
- Working with files: `type`, `copy`, `move`, `del`.  
- Masks: `copy *.md C:\Markdown`  

**Flag:**  
- C:C:\Treasure\Hunt: `THM{CLI_POWER}`.

---

### 📋 Task 5: Task and Process Management  
- `tasklist` - list of processes  
- Filtering: `tasklist /FI “imagename eq notepad.exe”`  
- Termination: `taskkill /PID <pid>`.

**Flags:**  
- Notepad search command: `tasklist /FI “imagename eq notepad.exe”`  
- Completing PID 1516: `taskkill /PID 1516`.

---

### 🧼 Task 6: Conclusion  
- Additional commands:
  - `chkdsk`, `driverquery`, `sfc /scannow`.  
  - `/ ?` - view help  
- `more file.txt` and `command | more` - page output  
- Shutdown commands:
  - Restart: `shutdown /r`.  
  - Cancel: `shutdown /a`  

---

## 🏁 Final Flag  
**THM{CLI_POWER}**

---

## 🧠 Takeaways  
- CLI is a must-have skill for admins and safecrackers  
- The `netstat`, `systeminfo`, `taskkill` commands are real 🔧 tools  
- Normal commands are not so simple when you use them in combat

Translated with DeepL.com (free version)