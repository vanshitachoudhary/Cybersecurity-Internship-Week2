# Networkwalks Cybersecurity Internship - Week 2: Module 1
**Intern Name:** Vanshita Choudhary  
**Module:** Footprinting & Reconnaissance Attacks  
**Target Authorized Scope:** `networkwalks.com` & local network  

---

## 📌 Executive Summary
This module focuses on passive and active footprinting techniques performed against the authorized target `networkwalks.com`. The goal is to gather publicly available information, identify web server characteristics, analyze DNS configurations, and detect defensive security controls without triggering disruptive alarms.

---

## 🛠️ Tools & Commands Executed
During this lab exercise, six core Kali Linux utilities were utilized:

1. **Whois Lookup (`whois`):**
   * *Command:* `whois networkwalks.com`
   * *Purpose:* To query domain registration records, administrative contacts, and registrar status.

2. **Web Server Fingerprinting (`whatweb`):**
   * *Command:* `whatweb networkwalks.com`
   * *Purpose:* To identify technologies running on the target web server (CMS, Apache, WordPress plugins, etc.).

3. **DNS Name Resolution (`nslookup`):**
   * *Command:* `nslookup networkwalks.com`
   * *Purpose:* To resolve the domain name to its corresponding IP address (`192.232.216.135`).

4. **HTTP Header Analysis (`curl`):**
   * *Command:* `curl -I https://networkwalks.com`
   * *Purpose:* To inspect HTTP response headers, server types, security policies, and cookies.

5. **Web Application Firewall Detection (`wafw00f`):**
   * *Command:* `wafw00f networkwalks.com`
   * *Purpose:* To detect and fingerprint any WAF protecting the web application (identified behind ModSecurity/SpiderLabs WAF).

6. **DNS Enumeration (`dnsrecon`):**
   * *Command:* `dnsrecon -d networkwalks.com`
   * *Purpose:* To perform comprehensive DNS record enumeration, finding SOA, NS, MX, TXT, and SRV records.

---

## 📂 Repository Contents
* `week2_module1_reconnaissance_report.pdf` — Complete professional internship report containing all technical observations and security analysis.
* `screenshots/` — Folder containing terminal execution screenshots for all 6 performed tasks.

---
*Authorized & Verified as part of the Networkwalks Internship Curriculum.*
