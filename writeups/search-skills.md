# 🕵️ TryHackMe: Search Skills – Writeup

Welcome to my writeup for the **Search Skills** room on TryHackMe!  
This room focused on essential **OSINT (Open-Source Intelligence)** techniques, using search engines and public databases to gather information.

🔗 [Room Link](https://tryhackme.com/room/searchskills)

---

## 📚 What I Learned

- How to craft effective Google search queries (advanced operators)
- Techniques to find public documents, leaks, credentials
- Using OSINT databases for username, email, IP lookups
- Practical skills for reconnaissance and information gathering

---

## 🔎 Techniques Practiced

### 🔹 Google Search Operators

- `site:domain.com` – Search only within a specific site
- `filetype:pdf` – Search for specific file types
- `intitle:"keyword"` – Search for pages with a keyword in the title
- `inurl:"keyword"` – Search for URLs containing the keyword
- `cache:url` – View cached versions of sites
- `"exact phrase"` – Search for an exact phrase match

### 🔹 OSINT Tools & Databases

- **HaveIBeenPwned** – Check email addresses against known breaches
- **Dehashed** – Find breached information linked to usernames, domains
- **Pastebin** – Search public pastes for sensitive data leaks
- **Google Dorking** – Finding misconfigured databases, cameras, sensitive files

---

## 🧪 Example Searches

- `site:linkedin.com "cybersecurity analyst"`  
  _Find security professionals on LinkedIn._

- `filetype:xls site:example.com "password"`  
  _Look for Excel files containing sensitive keywords._

- `inurl:admin site:example.com`  
  _Locate admin login panels on a site._

- `"DB_PASSWORD"` + `filetype:env`  
  _Search for environment configuration files with passwords._

---

## 💬 Reflections

- OSINT skills are crucial for reconnaissance, both in red teaming and defensive security.
- Knowing **what** to search and **how** to search saves time and reveals valuable hidden information.
- Search skills are equally useful for threat intelligence gathering, incident investigation, and vulnerability research.

---

## 🛠️ Tools Used

- Google Search (with advanced operators)
- Public OSINT databases: HaveIBeenPwned, Dehashed, Pastebin
- Custom search queries and filters

---

Thanks for reading!  
More writeups coming soon: [CryptoRapt0r.github.io](https://cryptorapt0r.github.io)

