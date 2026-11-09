# 🛡️ Networkwalks Cybersecurity Internship | Week 2: Module 1

[![Intern Name](https://img.shields.io/badge/Intern-Vanshita%20Choudhary-blue?style=flat-square)](https://github.com/vanshitachoudhary)
[![Module](https://img.shields.io/badge/Module-Footprinting%20%26%20Reconnaissance-orange?style=flat-square)]()
[![Target Scope](https://img.shields.io/badge/Target-networkwalks.com-success?style=flat-square)](https://networkwalks.com)
[![Status](https://img.shields.io/badge/Status-Completed%20%26%20Verified-brightgreen?style=flat-square)]()

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Authorized Scope](#-authorized-scope)
- [Tools & Commands Executed](#-tools--commands-executed)
- [Repository Artifacts](#-repository-artifacts)
- [Conclusion](#-conclusion)

---

## 🔍 Project Overview
This module documents the practical execution of **Footprinting and Reconnaissance Attacks** performed as part of the Networkwalks Cybersecurity Internship. The primary objective is to systematically gather open-source intelligence (OSINT), perform web server fingerprinting, resolve DNS records, and detect defensive security mechanisms (WAF) without violating ethical boundaries or triggering disruptive alerts.

---

## 🎯 Authorized Scope
All reconnaissance and information-gathering tasks were strictly restricted and executed against:
* **Target Domain:** `networkwalks.com`[cite: 1]
* **Environment:** Controlled Kali Linux Laboratory Environment (Batch B084)

---

## 🛠️ Tools & Commands Executed
During this lab session, six core Kali Linux utilities were deployed and analyzed:

| No. | Tool / Utility | Command Executed | Core Objective |
| :--- | :--- | :--- | :--- |
| **1** | **Whois** | `whois networkwalks.com` | Query domain registrar records, creation dates, and administrative contacts[cite: 1]. |
| **2** | **WhatWeb** | `whatweb networkwalks.com` | Identify web server software, CMS platforms, and backend technologies[cite: 1]. |
| **3** | **Nslookup** | `nslookup networkwalks.com` | Resolve domain names to target IP addresses (`192.232.216.135`)[cite: 1]. |
| **4** | **Curl** | `curl -I https://networkwalks.com` | Extract HTTP response headers, status codes, and security policies[cite: 1]. |
| **5** | **Wafw00f** | `wafw00f networkwalks.com` | Detect and fingerprint protective Web Application Firewall (WAF) implementations[cite: 1]. |
| **6** | **DNSRecon** | `dnsrecon -d networkwalks.com` | Enumerate complete DNS record sets (SOA, NS, MX, TXT, SRV)[cite: 1]. |

---

## 📂 Repository Artifacts
* **`Week 2 Project Module 1 - Footprinting & Reconnaissance Report.pdf`** — The comprehensive professional internship report containing detailed technical observations, step-by-step command analysis, and embedded execution screenshots.

---
*Verified & Submitted by **Vanshita Choudhary** for Networkwalks Cybersecurity Internship Evaluation.*
