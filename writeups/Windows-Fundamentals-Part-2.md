# 🪟 Windows Fundamentals Part 2 — TryHackMe Room Writeup

**Author:** CryptoRapt0r  
**Platform:** [TryHackMe.com](https://tryhackme.com)  
**Room:** [Windows Fundamentals 2](https://tryhackme.com/room/windowsfundamentals2)  
**Difficulty:** 🟢 Easy  
**Type:** Walkthrough

---

## 🌟 Goal

Continue learning Windows OS fundamentals with a focus on system tools and user account management through graphical and command-line utilities.

---

## 🛠️ Tools Used

* TryHackMe Browser VM  
* RDP / Windows Server 2019  
* Windows Built-in Tools: `msconfig`, `lusrmgr.msc`, `regedit`, `cmd`, `resmon`, etc.

---

## 🧭 Steps

### 1. User Accounts and Permissions

* Two main user types:
  * **Administrator** - full system control.
  * **Standard User** - limited to user-level changes.
* Managed via:
  * `Settings > Accounts > Other Users`
  * `lusrmgr.msc` for advanced group/user management.
* Example account: `tryhackmebilly`, member of `Remote Desktop Users` and `Users`.

---

### 2. User Account Control (UAC)

* UAC prompts for admin privileges when needed.
* Prevents unauthorized elevation of privileges.
* Standard users must input admin credentials to run privileged operations.
* Visual cue: shield icon on executable.

---

### 3. Settings vs. Control Panel

* **Settings**: modern interface for basic system changes.
* **Control Panel**: legacy interface for deeper options.
* Some features start in Settings and redirect to Control Panel (e.g., Network Adapter Options).

---

### 4. Task Manager

* Shortcut: `Ctrl+Shift+Esc`
* Shows running processes, resource usage (CPU/RAM).
* "More details" expands to show advanced tabs like Performance, Services, Users.

---

### 5. System Configuration (`msconfig`)

* Used for troubleshooting and diagnostic boot options.
* Tabs:
  * **General** - Selective startup options.
  * **Boot** - Safe boot, no GUI, base video, etc.
  * **Services** - Enable/disable services.
  * **Startup** - Redirects to Task Manager.
  * **Tools** - Shortcuts to other Windows admin utilities.

---

### 6. Change UAC Settings

* Via `UserAccountControlSettings.exe`
* Adjust notification level using slider.
* Microsoft recommends keeping UAC enabled for security.

---

### 7. Computer Management

* Launched via `compmgmt.msc`
* Contains:
  * **System Tools** - Event Viewer, Task Scheduler, Shared Folders.
  * **Storage** - Disk Management.
  * **Services and Applications** - View and control background services.

---

### 8. Disk Management

* View partitions, volumes, free space.
* Manage storage: shrink/expand volumes, change drive letters.

---

### 9. Performance Monitor

* Launched via `perfmon`
* Monitors real-time and logged system performance data.

---

### 10. System Information (`msinfo32`)

* Displays:
  * **System Summary** - OS version, manufacturer, etc.
  * **Hardware Resources** - IRQs, memory, etc.
  * **Components** - Drivers and installed devices.
  * **Software Environment** - Drivers, tasks, variables, etc.

---

### 11. Resource Monitor (`resmon`)

* Visual real-time monitoring of:
  * **CPU**, **Disk**, **Network**, and **Memory**.
* Allows filtering, inspecting process handles, and module usage.

---

### 12. Command Prompt Basics

* Common commands:
  * `hostname`, `whoami`, `ipconfig`, `netstat`, `net`
* `net` subcommands: `net user`, `net session`, `net share`, etc.
* Help commands:
  * `<command> /?` or `net help <subcommand>`

---

### 13. Registry Editor

* Launched with `regedit.exe`
* Hierarchical database storing system/user/application configs.
* Root keys:
  * `HKEY_LOCAL_MACHINE`, `HKEY_CURRENT_USER`, etc.
* Advanced feature; improper use can destabilize system.

---

## 🧠 Takeaways

* Gained control over user/group permissions and profiles.
* Learned to use `msconfig` for diagnostic troubleshooting.
* Explored Event Viewer, Task Scheduler, Shared Folders.
* Used `resmon`, `msinfo32`, `perfmon` for deep system introspection.
* Practiced Command Prompt for system/network commands.

---

🚀 Next up: **Windows Fundamentals Part 3** — Dive deeper into Windows logging, security tools, and PowerShell!