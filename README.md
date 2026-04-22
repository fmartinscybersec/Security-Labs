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

## 🛠️ Tech Stack & Security Toolbox

The development of these labs involves an ecosystem of advanced tools, categorized according to the Penetration Testing Execution Standard (PTES) phases:

### 💻 Environments and Systems
* **Offensive Systems:** Kali Linux, Parrot Security OS.
* **Target Systems (Vulnerable Labs):** Metasploitable 2/3, Windows Server (2008/2012/2019), Windows XP/7/10 (Legacy), HTB, and TryHackMe machines.
* **Virtualization & Cloud:** VMware Workstation Pro, VirtualBox, Proxmox, and Docker (for vulnerable microservices).

### 🔍 Reconnaissance and Enumeration
* **Network Scanning:** `Nmap`, `Masscan`, `Netdiscover`.
* **Web Enumeration:** `Dirsearch`, `Gobuster`, `FFUF`, `Nikto`.
* **OSINT:** `TheHarvester`, `Maltego`, `Shodan`.
* **SMB/AD:** `Enum4linux`, `Smbmap`, `CrackMapExec`.

### 🛡️ Vulnerability Analysis and Exploitation
* **Web Proxy/DAST:** `Burp Suite Professional`, `OWASP ZAP`.
* **Exploitation Frameworks:** `Metasploit Framework (MSF)`, `Searchsploit`.
* **Database Hacking:** `SQLMap`.
* **Network Sniffing:** `Wireshark`, `Tcpdump`, `Bettercap`.

### 🔑 Credential Management and Cracking
* **Offline Cracking:** `Hashcat` (GPU accelerated), `John the Ripper`.
* **Online Brute Force:** `Medusa`, `Hydra`.
* **Post-Exploitation:** `Mimikatz`, `LinPEAS/WinPEAS` (Privilege Escalation scripts).

### 📂 Forensics and File Analysis
* **Metadata:** `ExifTool`.
* **Binary Analysis:** `Strings`, `Binwalk`, `Ghidra` (Reverse Engineering).
* **Steganography:** `Steghide`.
