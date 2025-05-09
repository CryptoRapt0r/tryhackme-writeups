
# 🐧 Linux Fundamentals Part 3 — TryHackMe Room Writeup

**Author:** CryptoRapt0r  
**Platform:** [TryHackMe.com](https://tryhackme.com)  
**Room:** [Linux Fundamentals Part 3](https://tryhackme.com/room/linuxfundamentalspart3)  
**Difficulty:** 🟢 Easy  
**Type:** Walkthrough  

---

## 🌟 Goal

Learn how to manage processes, transfer files, use terminal editors, and understand automation in Linux.

---

## 🛠️ Tools Used

- TryHackMe AttackBox  
- Remote Linux Machine  
- SSH client / Terminal  
- Python3 HTTP server  
- SCP / Wget  

---

## 🧭 Steps

### 1. Setup & Access  

- Connected to both the Target and AttackBox environments  
- SSH login:  
  ```bash
  ssh tryhackme@<IP>
  ```

---

### 2. Terminal Editors

- Used **nano** to create/edit files:
  ```bash
  nano myfile
  ```
- Saved with Ctrl+O and exited with Ctrl+X  
- Brief intro to **vim** as a more advanced option

🟢 Flag: **THM{TEXT_EDITORS}**

---

### 3. File Transfers and HTTP Server  

- Downloaded with wget:
  ```bash
  wget http://<IP>:8000/file.txt
  ```
- Transferred with SCP:
  ```bash
  scp file.txt user@remote:/path/file.txt
  ```
- Started a Python3 web server:
  ```bash
  python3 -m http.server
  ```

🟢 Flag: **THM{WGET_WEBSERVER}**

---

### 4. Process Management  

- Checked running processes:
  ```bash
  ps aux
  top
  ```
- Killed processes with:
  ```bash
  kill -SIGTERM <PID>
  ```
- Managed services:
  ```bash
  systemctl start|stop|enable <service>
  ```
- Used backgrounding and foregrounding:
  ```bash
  ./script.sh &
  Ctrl+Z
  fg
  ```

🟢 Flag: **THM{PROCESSES}**

---

## 🏁 Flags Collected

- `THM{TEXT_EDITORS}`  
- `THM{WGET_WEBSERVER}`  
- `THM{PROCESSES}`  

---

# 🧠 Takeaways

- Practiced terminal text editing with nano and vim  
- Learned how to transfer files using SCP and HTTP  
- Explored process management and service control  
- Understood foregrounding and backgrounding of tasks  
- Gained experience using real Linux systems and commands  

---

🚀 Next up: **Windows Fundamentals Part 1** — time to shift into the Windows world!
