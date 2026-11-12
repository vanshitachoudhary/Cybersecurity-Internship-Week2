# Cybersecurity Internship - Week 2: Penetration Testing & Footprinting Report
**Student Name:** Vanshita Choudhary  
**Institute:** Acropolis Institute of Technology & Research, Indore  
**Batch:** BT804C  
**Program:** Cybersecurity & Ethical Hacking Internship | Networkwalks  

---

## 📌 Executive Summary
This repository contains the complete practical implementation, configuration proofs, execution screenshots, and final structured documentation for **Week 2** of the Cybersecurity Internship. The project successfully covers **Modules 1 through 5** (Passive Reconnaissance, GHDB, Maltego, theHarvester, and Zenmap Local Network Scanning) alongside the comprehensive final report.

---

## 📁 Repository Structure & Modules

| Module / Directory | Topic / Focus Area | Key Tools & Utilities Used | Status |
| :--- | :--- | :--- | :--- |
| **`module 1`** | Reconnaissance & Information Gathering | Multiple Kali Linux CLI Tools | ✅ Completed |
| **`module 2`** | Google Hacking Database (GHDB) & Dorks | Advanced Search Operators | ✅ Completed |
| **`module 3`** | Footprinting with Maltego CE | Maltego Community Edition (Windows) | ✅ Completed |
| **`module 4`** | Microsoft Domain OSINT | `theHarvester` | ✅ Completed |
| **`module 5`** | Network Scanning & Discovery | Zenmap (Nmap GUI), `ipconfig` (`10.235.107.0/24`) | ✅ Completed |
| **`Final Report`** | Comprehensive Penetration Testing Report | Multi-phase documentation & evidence proofs | ✅ Completed |

---

## 🛠️ Summary of Activities Performed

### Phase 1: Reconnaissance, OSINT & Footprinting (Modules 1 - 4)
* **Modules 1 & 2:** Gathered domain registration data, performed DNS enumeration, inspected HTTP security headers, and leveraged Google Hacking Database (GHDB) advanced search operators.
* **Module 3 (Maltego):** Configured Maltego Community Edition on Windows, completed activation wizard steps, authenticated via browser login links, and initialized the graphical OSINT workspace.
* **Module 4 (theHarvester):** Executed target domain queries to harvest associated email addresses, employee names, and subdomains from public sources.

### Phase 2: Network Discovery & Scanning (Module 5 & Final Report)
* **Local Interface Identification:** Used Windows `ipconfig` to determine local network configuration (`IP: 10.235.107.1`, `Subnet: 10.235.107.0/24`).
* **Zenmap Ping Scan:** Executed subnet sweep (`nmap -sn 10.235.107.0/24`) to discover active live hosts (`10.235.107.1` and `10.235.107.219`).
* **Topological Mapping:** Generated, viewed, and exported the visual network topology graph as a PDF (`zenmap_topology.pdf`).

---

## 🛡️ Risk Analysis & Security Recommendations
* **Information Exposure:** Publicly visible CMS versions and footprinting data assist potential attackers in technology fingerprinting. Regular review and hardening of response headers are recommended.
* **Network Visibility:** Internal host discovery emphasizes the necessity of maintaining strict network asset inventories and investigating unknown connected devices.
* **Scope Adherence:** All reconnaissance, OSINT, and scanning activities were performed strictly within authorized educational lab scopes and personal network environments in accordance with standard cybersecurity ethics.

---
> *© 2026 Vanshita Choudhary | Acropolis Institute | Networkwalks Internship*
