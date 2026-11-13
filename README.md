# Footprinting & Reconnaissance with theHarvester (W2-PM4) & Zenmap Scanning (W2-PM5)

**Author:** Devangi  
**Program:** Cybersecurity & Ethical Hacking Program – Networkwalks  
**Week / Module:** Week 02 | W2-PM4 & W2-PM5  
**Date:** 12 November 2026  

---

## Overview
This repository documents Week 2 practical penetration testing exercises covering **Phase 1: Passive Reconnaissance & Footprinting** using `theHarvester` in Kali Linux and **Phase 2: Active Network Discovery** using `Zenmap (Nmap GUI)` on Windows 11.

> **Disclaimer:** All activities were performed strictly for educational and research purposes against public Open-Source Intelligence (OSINT) sources and an owned local lab environment (`192.168.79.0/24`).

---

## Tools Used
* **Kali Linux (VirtualBox):** Primary OS for passive OSINT footprinting.
* **theHarvester (v4.11.1):** Python-based OSINT tool for gathering emails, subdomains, hosts, and IPs from public search engines.
* **Zenmap (Nmap 7.993 GUI):** Network scanner used for ping sweeps (`nmap -sn`), MAC address identification, and topology mapping.

---

## Commands Executed

### 1. Passive Footprinting (`theHarvester`)
* **Task 1 – Single-Source Search (Baidu, limit 1000):**
  ```bash
  theHarvester -d microsoft.com -l 1000 -b baidu
  ```
* **Task 2 – Multi-Source Enumeration (All sources, limit 50):**

  ```bash
  theHarvester -d microsoft.com -l 50 -b all
  ```
2. Local Network Discovery (Zenmap)
Ping Scan across local subnet:

```
nmap -sn 192.168.79.0/24
```
Discovered Hosts: 192.168.79.1 (Local host) and 192.168.79.254 (MAC: 00:50:56:F8:22:17 – VMware).
