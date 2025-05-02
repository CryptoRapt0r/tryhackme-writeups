# 🐧 Linux Fundamentals Part 2 — TryHackMe Room Writeup

**Author:** CryptoRapt0r  
**Platform:** [TryHackMe.com](https://tryhackme.com)  
**Room:** [Linux Fundamentals Part 2](https://tryhackme.com/room/linuxfundamentalspart2)  
**Difficulty:** 🟢 Easy  
**Type:** Walkthrough

---

## 🌟 Goal

Learn how to access Linux remotely via SSH, interact with the filesystem using more advanced commands, understand file permissions, and navigate important root directories.

---

## 🛠️ Tools Used

- TryHackMe AttackBox  
- Remote Linux Machine  
- SSH client  
- Terminal

---

## 🧭 Steps

### 1. Introduction  
- Applies Part 1 knowledge in a deeper, more practical way.  
- Focus on flags, switches, scripts, and remote machine interaction.  

---

### 2. Access via SSH  
Connected using:

```bash
ssh tryhackme@<IP_ADDRESS>
# Password: tryhackme
```

> Note: No feedback shown when typing passwords — just press enter.

---

### 3. Flags & Switches  
- Use `ls -a` to show hidden files.  
- Use `ls --help` or `man ls` for command documentation.  

Example:

```bash
ls -lh  # Detailed view of directory with human-readable sizes
```

---

### 4. Filesystem Interaction Continued  
Commands practiced:  

- `touch` — create empty file  
- `mkdir` — create folder  
- `rm` — remove file/folder (`-R` for recursive)  
- `cp` — copy files  
- `mv` — move or rename files  
- `file` — check file type

Example:

```bash
touch note
mkdir myfolder
mv note myfolder/
```

🟢 Flag Found: **THM{FILESYSTEM}**

---

### 5. Permissions 101  
- Checked permissions using `ls -lh`  
- Owner and group permissions explained (`rwx` logic)  
- Switched users with `su`:

```bash
su -l user2
# Password: user2
```

🟢 Flag Found: **THM{SU_USER2}**

---

### 6. Common Directories  

- `/etc` — config files (e.g. `passwd`, `shadow`, `sudoers`)  
- `/var` — logs, runtime data (`/var/log`)  
- `/root` — home of root user  
- `/tmp` — volatile storage (clears on reboot)

---

## 🏁 Flags

- `THM{FILESYSTEM}`  
- `THM{SU_USER2}`  

---

# 🧠 Takeaways

- Learned how to connect to a remote Linux box using SSH  
- Mastered use of flags and command documentation  
- Practiced creating, moving, and deleting files  
- Understood Linux permissions and switching between users  
- Explored key system directories and their use in real-world systems

---

🚀 Next up: **Linux Fundamentals Part 3** — deeper scripting, user management, and more.  
Let’s keep going!
