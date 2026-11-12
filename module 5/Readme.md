# Week 2 - Project Module 5: Network Scanning with Zenmap

This module covers local area network reconnaissance, live host discovery, and network topology mapping using **Zenmap** (the official GUI frontend for Nmap) on Windows[cite: 38].

---

## 🛠️ Tasks Performed & Subnet Details
* **Task 1:** Downloaded and installed Zenmap and Nmap components on Windows[cite: 38, 39, 40].
* **Task 2:** Identified local network configuration using `ipconfig` (Subnet: `10.235.107.0/24`).
* **Task 3 & 4:** Executed a Ping Scan (`nmap -sn 10.235.107.0/24`) to discover active hosts on the subnet[cite: 38].
* **Task 5 & 6:** Extracted live IP addresses (`10.235.107.1`, `10.235.107.219`) and associated MAC addresses.
* **Task 7:** Generated, viewed, and exported the visual network topology graph as a PDF (`zenmap_topology.pdf`)[cite: 38].

---

## 📸 Execution Proof & Screenshots

### Task 3 & 4: Ping Scan Output & Live Hosts
> *Description: Nmap output showing the executed ping scan command and discovered live hosts on the local subnet.*
![Zenmap Scan Output](Screenshot%202026-11-12%20200103.png)

### Task 7: Network Topology Map
> *Description: Visual node representation of connected localhost and active subnet IPs in Zenmap topology view.*
![Zenmap Topology View](Screenshot%202026-11-12%20200749.png)

---

## 📌 Key Learnings
* **Subnet Discovery:** Using ICMP ping sweeps (`-sn`) to quickly identify online devices within a local network range without intrusive port scans.
* **Topological Mapping:** Leveraging Zenmap graphical features to visualize network nodes and export reports for documentation[cite: 38].
