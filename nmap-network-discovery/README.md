# Lab Report: Host Discovery & Network Reconnaissance with Nmap

## 📋 Executive Summary
This laboratory exercise documents network reconnaissance and host discovery workflows executed within a controlled security testing environment. The primary objective is to map target systems, identify active listeners, and enumerate open services on a vulnerable virtualized machine (`Metasploitable 2`) using advanced `Nmap` command-line switches from a `Kali Linux` host.

---

## 🛠️ Lab Architecture & Environment
* **Attacker System:** Kali Linux (VirtualBox Host-Only Adapter)
* **Target System:** Metasploitable 2 (Vulnerable Virtual Machine)
* **Tooling:** Nmap (Network Mapper) v7.xx
* **Methodology:** Passive reconnaissance transitioning to active TCP SYN port scanning and service version detection.

---

## 🔍 Execution & Methodology

### Phase 1: Host Discovery (Ping Sweep)
To identify live hosts on the local subnet without triggering intensive firewall alerts, an ARP/ICMP sweep was initiated:
```bash
nmap -sn 192.168.56.0/24
