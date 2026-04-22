# 🛡️ Security-Labs

Welcome to my Cybersecurity laboratory. This repository centralizes my technical portfolio, documenting CTF challenges, network audits, and penetration testing projects.

---

## ⚖️ Disclaimer / Terms of Responsibility
**Attention:** This repository, including all its subdirectories and associated projects, is created and maintained strictly for **educational and academic purposes**.

* **Controlled Environment:** All activities and vulnerability demonstrations were conducted exclusively within **controlled laboratory environments**.
* **Ethical Use:** Any attempt to use these techniques for malicious purposes or without prior authorization is the **sole responsibility of the user**.
* **Liability:** The author assumes no responsibility for the misuse of the content presented herein.

---

## 📂 Portfolio Organization

Each directory below represents an isolated project and follows this structure:
1. `README.md`: Detailed documentation of methodology, tools, and results.
2. `screenshots/`: Screen captures providing technical proof (PoC).
3. `files/`: PDF reports or configuration files (where applicable).

---

### 🛠️ Tech Stack & Security Toolbox

The development of these labs involves an ecosystem of advanced tools, categorized according to the **Penetration Testing Execution Standard (PTES)** phases and modern security workflows:

#### 💻 Lab Infrastructure & OS
* **Offensive Platforms:** Kali Linux (Rolling Release), Parrot Security OS.
* **Target Environments:** Metasploitable 2/3, Windows Server Active Directory Labs, TryHackMe/HackTheBox instances, and Docker-based vulnerable microservices.
* **Virtualization & Hypervisors:** VMware Workstation Pro, VirtualBox, Proxmox VE.

#### 🔍 Information Gathering & Enumeration
* **Network Discovery:** `Nmap`, `Masscan`, `Netdiscover`, `Bettercap`.
* **Web Fingerprinting:** `WhatWeb`, `Wappalyzer (CLI)`, `BuiltWith`.
* **Directory & Asset Fuzzing:** `FFUF`, `Gobuster`, `Dirsearch`, `Dirb`.
* **OSINT:** `Shodan`, `TheHarvester`, `Maltego`, `SpiderFoot`.

#### 🏛️ Infrastructure & Directory Services (SMB/AD)
* **SMB/RPC Enumeration:** `Enum4linux`, `Enum4linux-ng`, `Smbclient`, `Smbmap`.
* **AD Assessment:** `CrackMapExec` (Swiss-army knife for AD), `BloodHound` (Path analysis), `Impacket Suite`.

#### 🛡️ Vulnerability Analysis & Web Auditing
* **Web Proxy/DAST:** `Burp Suite Professional`, `OWASP ZAP`.
* **Vulnerability Scanning:** `Nikto` (Web Misconfigurations), `Nuclei` (Template-based scanning), `Nessus`.
* **Database Auditing:** `SQLMap` (SQLi detection and exploitation).

#### 🚀 Exploitation & Post-Exploitation
* **Exploitation Frameworks:** `Metasploit Framework (MSF)`, `Searchsploit` (Exploit-DB).
* **Traffic Analysis & Sniffing:** `Wireshark`, `Tcpdump`, `Tshark`.
* **Privilege Escalation:** `LinPEAS`, `WinPEAS`, `BeRoot`, `PowerUp`.
* **Post-Exploitation Modules:** `Mimikatz` (In-memory credential dumping), `Rubeus` (Kerberos-based attacks).

#### 🔑 Credential Access & Identity
* **Offline Cracking:** `Hashcat` (GPU accelerated), `John the Ripper`.
* **Online Brute Force:** `Hydra`, `Medusa`, `Patator`.

#### 📂 Digital Forensics & Reverse Engineering (DFIR)
* **Static Analysis:** `Strings`, `ExifTool`, `Binwalk`.
* **Reverse Engineering:** `Ghidra`, `Radare2`, `IDA Free`.
* **Steganography:** `Steghide`, `Zsteg`, `StegSolve`.
