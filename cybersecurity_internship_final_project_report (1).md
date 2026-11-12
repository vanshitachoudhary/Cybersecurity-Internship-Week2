# PENETRATION TESTING REPORT
## FOOTPRINTING & NETWORK SCANNING PHASES
**W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS**

| Detail | Information |
| :--- | :--- |
| **Pentester Name** | Vanshita Choudhary (Cybersecurity Professional) |
| **Program/Batch** | BT804C - Networkwalks |
| **Date** | 12 November 2026 |
| **Modules Completed** | W2-PM1 (Kali Tools), W2-PM2 (GHDB), W2-PM3 (Maltego), W2-PM4 (theHarvester), W2-PM5 (Zenmap Scanning) |
| **Client/Target** | 1. Networkwalks (secured written permission already)<br>2. My own local LAN Network (`10.235.107.0/24`) |
| **Permission Secured?** | Yes |
| **Phases Covered** | Phase 1: Reconnaissance & Footprinting (Modules 1 - 4)<br>Phase 2: Scanning & Network Discovery (Module 5) |

---

## 1. Liability Disclaimer
I have performed these activities only on the systems & devices where I had secured written permission or the devices/systems that I own myself. All these materials are for education and research purpose only. Do not use anything from here to break the law. The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge. Every action you take is your own responsibility. Misuse can lead to criminal charges, heavy fines, loss of your job and a permanent record. In most countries unauthorised access is a crime even when nothing is damaged.

---

## 2. Introduction
This report covers footprinting the `networkwalks.com` domain using multiple Kali Linux tools, Google Hacking Database dorks, Maltego, and theHarvester (Modules 1 to 4), followed by scanning my own local network subnet (`10.235.107.0/24`) with Zenmap (Module 5). Together, these modules illustrate how a security professional transitions from passive OSINT intelligence gathering to active host discovery on a local network. It forms the complete Week 2 project deliverable of my ongoing internship program at Networkwalks (Batch BT804C).

All commands were run in Kali Linux (footprinting) and on a Windows PC with Zenmap installed (scanning). Every step includes the exact command used, observed results, screenshot evidence, and a brief note on why the finding matters from an attacker's perspective.

---

## 3. Tools Used
| Tool | Purpose |
| :--- | :--- |
| **Kali Linux & Windows** | Operating systems used for reconnaissance and scanning activities |
| **WHOIS** | Find domain registration details (owner, dates, name servers) |
| **WhatWeb** | Fingerprint web technologies (server, CMS, plugins, IP) |
| **nslookup** | Resolve the domain name to its IP address using DNS |
| **curl -I** | Read the HTTP response headers of the website |
| **wafw00f** | Detect whether a Web Application Firewall protects the site |
| **Google Dorks (GHDB)** | Leverage advanced search operators for targeted information leakage discovery |
| **Maltego CE** | Initialize graphical OSINT investigation workspaces on Windows |
| **theHarvester** | Harvest public email addresses, employee names, and subdomains |
| **Zenmap (Nmap GUI)** | Scan local subnet (`10.235.107.0/24`) to find live hosts, IPs, and MAC addresses |
| **Windows CMD (`ipconfig`)** | Local interface IP and subnet identification |

---

## 4. Activities Performed

### 4.1 Footprinting & Reconnaissance (Modules 1 - 4)
I performed comprehensive reconnaissance across all assigned modules against `networkwalks.com` and target investigation scopes:
* **Modules 1 & 2 (CLI & GHDB):** Utilized Kali Linux command-line utilities (`whois`, `whatweb`, `nslookup`, `curl -I`, `wafw00f`) and Google Dorks to extract domain registration data, server IP (`192.232.216.135`), WordPress CMS versions (7.0.4), and ModSecurity WAF protection.
* **Module 3 (Maltego CE):** Downloaded, installed, and configured Maltego Community Edition on Windows, completed activation wizard steps, authenticated via browser login links, and initialized the graphical OSINT investigation workspace.
* **Module 4 (theHarvester):** Configured the execution environment and ran target domain queries to harvest associated digital footprints, email structures, and subdomains from public intelligence sources.

### 4.2 Network Scanning with Zenmap (Module 5)
For the active network discovery phase:
* Used Windows `ipconfig` to determine local network interface configuration: **Local Gateway / IP:** `10.235.107.1` | **Subnet:** `10.235.107.0/24`.
* Entered the target subnet into Zenmap and executed a **Ping Scan** (`nmap -sn 10.235.107.0/24`).
* **Discovered Live Hosts (2 hosts up):**
  1. `10.235.107.1` (Host is up)
  2. `10.235.107.219` (Host is up with MAC Address `D6:BD:8A:E2:1A:A8`)
* Opened the Topology section in Zenmap, enabled the legend, and exported the network topology map in PDF format (`zenmap_topology.pdf`).

---

## 5. Risk Analysis / Impact
| # | Risk / Finding | Evidence / Observation | Potential Impact | Risk Level |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Web technology information exposed | WhatWeb identified WordPress and WP Download Manager | Attackers may use exposed software version info to identify components requiring security review | ● Medium |
| 2 | Server IP address identifiable | Nslookup resolved domain to `192.232.216.135` | Provides information about the physical/cloud network location of the web service | ● Low |
| 3 | HTTP technical information exposed | Curl returned HTTP response headers and exposed `/wp-json/` | May assist technology fingerprinting and endpoint enumeration | ● Low |
| 4 | WAF technology identifiable | Wafw00f identified ModSecurity (SpiderLabs) | Reveals information about the web application’s security defensive architecture | ● Low |
| 5 | Active live hosts visible on local network | Zenmap identified active hosts in subnet `10.235.107.0/24` | Unknown or unauthorized devices present on a local network can broaden attack surface | ● Medium |

*Risk level key: ● Critical ● Medium ● Low*  
*(Note: The risks above are observations from reconnaissance exercises, not confirmed vulnerabilities.)*

---

## 6. Recommendations
* **Review Public Technology Exposure:** Regularly review what information about web technologies, CMS, and plugins is publicly visible.
* **Keep Software Updated:** CMS platforms, plugins, and web dependencies should be updated regularly against security advisories.
* **Harden HTTP Headers:** Inspect and minimize HTTP response headers to prevent unnecessary server information leakage.
* **Perform Internal Discovery:** Periodically scan internal networks to identify active devices and investigate unexpected connections.
* **Maintain Documentation:** Network topology diagrams and asset inventories should be documented and updated regularly.
* **Strict Authorization:** Reconnaissance and scanning must only be performed against systems and networks where explicit prior authorization has been provided.

---

## 7. Conclusion
During Week 2 of my Cybersecurity & Ethical Hacking internship (Batch BT804C), I successfully completed all practical modules covering passive reconnaissance, GHDB search techniques, Maltego workspace setup, theHarvester OSINT domain footprinting, and active local network discovery using Zenmap. These exercises demonstrated that structured information gathering and meticulous technical documentation are vital foundational pillars of professional cybersecurity assessments.

---

## 8. Evidences Collected

### Module 1 & 2: Kali Linux CLI & GHDB Footprinting
* **WHOIS Domain Lookup:** `whois networkwalks.com` output verifying registrar details.
* **WhatWeb Fingerprinting:** Identifying Apache, WordPress 7.0.4, and WP Download Manager.
* **Nslookup & Curl Headers:** Resolving `192.232.216.135` and inspecting `/wp-json/` endpoints.
* **Wafw00f Detection:** Verifying ModSecurity (SpiderLabs) WAF protection.

### Module 3: Maltego Workspace Initialization
* **Maltego Activation Setup:** `Screenshot 2026-11-12 183415_2.jpg`
* **Login Link Authentication:** `Screenshot 2026-11-12 183639_2.png`
* **Main Graph Workspace Ready:** `Screenshot 2026-11-12 201909.jpg`

### Module 4: theHarvester Microsoft Reconnaissance
* **Environment Setup:** `module 4 task 1 (2).jpeg`
* **First Half Recon Output:** `module 4 task2 first half.jpeg`
* **Final Harvested Results:** `module 4 task2 final half.jpeg`

### Module 5: Zenmap Network Scanning & Topology
* **Ping Scan Output (`10.235.107.0/24`):** `Screenshot 2026-11-12 200103.png`
* **Network Topology Map & Legend:** `Screenshot 2026-11-12 200749.png` & `zenmap_topology.pdf`

---
-End-  
👤 **Author:** Vanshita Choudhary (Batch: BT804C)  
📌 **Program:** Cybersecurity Internship | Networkwalks | Week 2