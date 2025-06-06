# 🌐 Active Directory Basics — TryHackMe Room Writeup

**Author:** CryptoRapt0r
**Platform:** [TryHackMe.com](https://tryhackme.com)
**Room:** [Active Directory Basics](https://tryhackme.com/room/winadbasics)
**Difficulty:** 🟢 Easy
**Type:** Walkthrough

---

## 🎯 Goal

Learn Active Directory (AD) fundamentals, including users, groups, domains, policies, and authentication protocols.

---

## 🔧 Tools Used

* TryHackMe Browser Machine
* Windows Domain Controller
* PowerShell / RDP

---

## 🧭 Tasks Summary

### Task 1: Introduction

Brief overview of the AD room. No questions.

---

### Task 2: Windows Domains

* A domain is a central management system for users/computers.
* AD runs on Domain Controllers (DCs).
* Centralized identity + security policies.

✅ **Answers:**

* `Active Directory`
* `Domain Controller`

---

### Task 3: Active Directory

* Key components: Users, Machines, Security Groups.
* Users can represent humans or services.
* Machines join the domain and get their own accounts.
* Default groups: Domain Admins, Domain Users, etc.
* Organizational Units (OUs): Containers for users/devices.

✅ **Answers:**

* `Domain Admins`
* `TOM-PCS`
* `Organizational Units`

---

### Task 4: Managing Users in AD

* Used "Active Directory Users and Computers" tool.
* Deleted unused OU (had to disable accidental deletion).
* Delegated password reset rights for Phillip (IT) via `Delegate Control`.
* Reset password using PowerShell:

```powershell
Set-ADAccountPassword sophie -Reset -NewPassword (Read-Host -AsSecureString)
Set-ADUser -ChangePasswordAtLogon $true -Identity sophie
```

✅ **Answers:**

* `THM{thanks_for_contacting_support}`
* `delegation`

---

### Task 5: Managing Computers in AD

* Devices default to "Computers" container.
* Created separate OUs for `Workstations` and `Servers`.
* Moved computers accordingly.

✅ **Answers:**

* `7`
* `yay`

---

### Task 6: Group Policies

* Group Policy Objects (GPOs) define configuration rules.
* GPOs created under Group Policy Management.
* Linked to OUs to apply specific settings.
* Changed password length in default GPO.
* Created GPOs:

  * `Restrict Control Panel Access` (linked to non-IT OUs)
  * `Auto Lock Screen` (300 seconds inactivity, linked to root)
* Force policy sync with:

```powershell
gpupdate /force
```

✅ **Answers:**

* `sysvol`
* `yay`

---

### Task 7: Authentication Methods

* **Kerberos:** Default in modern Windows; uses tickets (TGT, TGS).
* **NetNTLM:** Legacy; uses challenge-response.

✅ **Answers:**

* `nay`
* `Ticket Granting Ticket`
* `nay`

---

### Task 8: Trees, Forests and Trusts

* Trees = Domains with shared namespace.
* Forest = Multiple trees with different namespaces.
* Trusts connect domains:

  * One-way or Two-way

✅ **Answers:**

* `Tree`
* `A Trust Relationship`

---

## 🏁 Final Flag

**Completion Trigger:** Room fully completed after finishing all tasks.

---

## 🧠 Key Takeaways

* Active Directory is the heart of Windows domain networks.
* Organizational Units (OUs) allow structure and control.
* GPOs help enforce security and configuration.
* Kerberos is a secure authentication protocol; NetNTLM is less secure.
* Trees/Forests and trust relationships scale AD across enterprises.

---

**Next up:** Dive deeper with **Attack Techniques in AD** 🔍
