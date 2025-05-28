# 🪟 Windows Fundamentals Part 1 — TryHackMe Room Writeup

**Author:** CryptoRapt0r
**Platform:** [TryHackMe.com](https://tryhackme.com)
**Room:** [Windows Fundamentals 1](https://tryhackme.com/room/windowsfundamentals1)
**Difficulty:** 🟢 Easy
**Type:** Walkthrough

---

## 🌟 Goal

Gain a beginner-friendly overview of the Windows operating system: its structure, versions, GUI interface, file system, user management, and tools like Task Manager and Control Panel.

---

## 🛠️ Tools Used

* TryHackMe Browser VM
* RDP / Windows Server 2019
* Windows Explorer

---

## 🧭 Steps

### 1. Introduction to Windows

* Windows OS explained as GUI-based and complex.
* Deployed VM via RDP.
* Access with:

  * **User:** administrator
  * **Password:** letmein123!

---

### 2. Windows Editions

* Discussed the evolution from XP > Vista > 7 > 8 > 10 > 11.
* Mentioned Windows Server 2025.
* Difference between Home and Pro editions.
* **BitLocker** is available on Pro but not Home.

---

### 3. The Desktop (GUI)

* Elements: Desktop, Taskbar, Start Menu, Search, Notification Area.
* Access to apps via taskbar/start.
* Right-click desktop > Personalize for wallpaper, font changes.
* **Display Settings**: Adjust resolution and layout.

---

### 4. The File System

* Windows uses **NTFS** (New Technology File System).

* Compared with FAT32.

* Permissions in NTFS:

  * Full control
  * Modify
  * Read & Execute
  * List contents
  * Read
  * Write

* Introduced **Alternate Data Streams (ADS)**:

  * Hidden metadata in files (e.g., `$DATA`).
  * Can be explored via PowerShell.

---

### 5. The Windows\System32 Folders

* Critical folder: `C:\Windows\System32`
* Contains core OS files and services.
* Environment variable: `%windir%`
* Warning: Deleting System32 can break Windows.

---

### 6. User Accounts, Profiles, and Permissions

* Two types of accounts:

  * **Administrator**
  * **Standard User**

* Create user via `Other users` settings.

* Use `lusrmgr.msc` to manage users/groups.

* Example account: `tryhackmebilly`

* Example group memberships: `Remote Desktop Users`, `Users`

---

### 7. User Account Control (UAC)

* UAC prevents silent elevation of privileges.
* Prompt appears when admin-level tasks run.
* Standard user prompted to provide admin credentials.

---

### 8. Settings and the Control Panel

* **Settings**: modern GUI since Windows 8.
* **Control Panel**: legacy but still powerful.
* Both accessible from Start Menu.
* Example: change adapter settings for network inside Control Panel.

---

### 9. Task Manager

* Access via right-click Taskbar or `Ctrl+Shift+Esc`.
* Shows resource usage (CPU, RAM, etc).
* Can kill or monitor processes.

---

### 10. Conclusion

* Room gives a high-level intro to Windows OS structure.
* Prepares the learner for deeper dives into Windows Defender, Registry, etc.

---

# 🧠 Takeaways

* Comfortable with navigating Windows GUI and filesystem.
* Understood difference between admin and standard user.
* Learned NTFS, permissions, ADS, and key system folders.
* Managed users and groups using built-in tools.
* Got familiar with Task Manager and Control Panel usage.

---

🚀 Next up: **Windows Fundamentals Part 2** — let’s continue mastering Windows internals!
