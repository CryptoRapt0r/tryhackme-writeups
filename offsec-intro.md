# 🦖 Offensive Security Intro — TryHackMe Room Writeup  
**Author:** CryptoRapt0r  
**Platform:** [TryHackMe.com](https://tryhackme.com)  
**Room:** [Offensive Security Intro](https://tryhackme.com/room/offensivesecurityintro)  
**Difficulty:** 🟢 Easy  
**Type:** Walkthrough

---

## 🎯 Goal  
Hack into a simulated banking website, find a hidden endpoint, and perform a fake money transfer to capture the room flag.

---

## 🧰 Tools Used  
- Gobuster  
- wordlist.txt  
- Firefox (FakeBank UI)  
- TryHackMe VM

---

## 🛠️ Steps

### 1. Start Machine  
Target IP provided: `10.10.137.143`  
FakeBank site hosted on: `http://fakebank.thm`

---

### 2. Scan for Hidden Directories  
Using **Gobuster** to brute-force directory names:

```bash
gobuster -u http://fakebank.thm -w wordlist.txt dir
/images (301)
/bank-transfer (200)
```

###3. Access /bank-transfer
Visited http://fakebank.thm/bank-transfer
→ Opened the hidden money transfer page
→ Simulated transfer of $2000 to account 8881


🏁 Flag
Message displayed:

Congratulations - you hacked the bank!  
The answer is BANK-HACKED

✅ Submitted flag: BANK-HACKED

![image](https://github.com/user-attachments/assets/1ec5a3e3-7d4a-40b8-b5fc-4a395d36e063)

🧠 Takeaways
Recon is the most important step in offensive security

Gobuster = simple, powerful, fast

“Hidden” doesn’t mean “secure”

I just hacked my first fake machine 😎
