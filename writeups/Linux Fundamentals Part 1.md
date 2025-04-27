# 🐉 Linux Fundamentals Part 1 — TryHackMe Room Writeup

**Author:** CryptoRapt0r\
**Platform:** [TryHackMe.com](https://tryhackme.com)\
**Room:** [Linux Fundamentals Part 1](https://tryhackme.com/room/linuxfundamentalspart1)\
**Difficulty:** 🟢 Easy\
**Type:** Walkthrough

---

## 🌟 Goal

Get familiar with Linux basics: navigation, searching, file manipulation, and understanding shell operators.

---

## 🛠️ Tools Used

- TryHackMe Browser VM
- Linux Terminal

---

## 🛠️ Steps

### 1. Introduction

- Overview of Linux OS and its importance.
- Linux powers smart cars, servers, android devices, etc.
- Goal: Start interacting with Linux from the ground up.

---

### 2. A Bit of Background on Linux

- Linux is lightweight compared to Windows.
- Popular distributions: Ubuntu, Debian.
- First Linux OS release: **1991**

---

### 3. Interacting with Your First Linux Machine

- Deployed a TryHackMe Ubuntu machine in-browser.
- IP address assigned, 2 hours expiry timer.

---

### 4. Running Your First Few Commands

Basic Commands:

- `echo Hello` — outputs "Hello" to terminal.
- `whoami` — shows current logged-in user.

Examples:

```bash
echo "TryHackMe"
whoami
```

---

### 5. Interacting With the Filesystem

Filesystem Navigation:

- `ls` — list files and directories.
- `cd` — change directories.
- `cat` — output file contents.
- `pwd` — print working directory (shows where you are).

Example:

```bash
ls
cd Documents
pwd
```

---

### 6. Searching for Files

Using `find`:

- Search by name:

```bash
find -name passwords.txt
```

- Search all `.txt` files:

```bash
find -name *.txt
```

Using `grep`:

- Search inside files:

```bash
grep "THM" access.log
```

- Found Flag: **THM{ACCESS}**

---

### 7. Shell Operators

Operators:

- `&` — run process in background.
- `&&` — run second command only if first succeeds.
- `>` — redirect output (overwrites file).
- `>>` — append output to file.

Examples:

```bash
echo hey > welcome
cat welcome
echo hello >> welcome
cat welcome
```

---

## 🏁 Flag

**Found Flag:** `THM{ACCESS}`

---

# 🧠 Takeaways

- Linux navigation basics mastered (ls, cd, pwd).
- Learned `find`, `grep`, and shell operators for file interaction.
- Feeling more confident in CLI environments!

---

Next stop: **Linux Fundamentals Part 2!** 🚀

