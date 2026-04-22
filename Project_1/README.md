**Author:** FMartinsCyberSec  

---

## 📑 Project Overview
This project documents the resolution of a practical cybersecurity assessment focused on two main pillars:
1. **CTF & Cryptanalysis:** File exploration, metadata analysis, and password cracking.
2. **Technical Pentest:** Full security audit and risk analysis on a vulnerable virtual machine (Windows XP).

---

## 🛠️ Part 1: Forensic Analysis & Cracking (`try_open_me.zip`)

An analysis was conducted on the `hackTHEtask` repository to extract critical information from a protected ZIP file.

### Methodology and Tools:
- **Enumeration:** Listed internal files (Blackbeard, Captain Hook, Captain Kidd, etc.) to identify potential targets.
- **Zip2John:** Converted the ZIP file encryption into a crackable hash format.
- **John the Ripper:** Executed a dictionary attack using the `rockyou.txt` wordlist.
  - **Password Found:** `ilove2shop`

### Decrypted Hashes (Hashcat):
| File | Algorithm | Hash Fragment | Decrypted Password |
| :--- | :--- | :--- | :--- |
| `Blackbeard.txt` | MD5 | `ecbf92...a3d3` | **maximillian** |
| `Captain Kidd.txt` | SHA2-256 | `f97598...2f85` | **marquese** |
| `Captain Hook.txt` | SHA2-512 | `eabb2c...c11` | **lilmisssunshine** |
| `Wavebreaker.txt` | SHA1 | `7005bc...4099` | **me&him** |
| `just_look_here.docx`| MS Office 2013 | - | **briliant** |

---

## 🛡️ Part 2: Technical Pentest (VM `m00-dl3`)

A technical audit was performed on a vulnerable machine to identify critical infrastructure flaws in a simulated network.

### 🔍 Reconnaissance Phase:
- **Target IP:** `192.168.1.222` (VMware environment).
- **OS:** Windows XP SP2/SP3 (Legacy and highly vulnerable system).
- **Critical Services:** Apache 2.4.9, MySQL 5.x, and SMB (ports 139/445).

### 💣 Identified Attack Vectors:
1. **SMB Misconfiguration:** The `disknet` and `SharedDocs` shares allowed anonymous Read/Write access.
   - **PoC (Proof of Concept):** Successfully uploaded a `malware.txt` file using `smbclient` without authentication.
2. **Brute Force:** Identified root user credentials using the **Medusa** tool.

### 💡 Mitigation Recommendations:
- **Disable SMBv1:** Immediate block of ports 139 and 445.
- **Isolation (Air-Gap):** Place legacy systems in isolated VLANs with strict firewall rules.
- **OS Upgrade:** Migrate to Windows 10/11 or a supported Linux LTS distribution due to the EOL (End of Life) status of Windows XP.

---

## 🔧 Tools Applied
* **Systems:** Kali Linux (Attacker machine).
* **Reconnaissance:** Nmap, Netdiscover.
* **Cracking:** John the Ripper, Hashcat, Medusa.
* **Analysis:** ExifTool, Smbclient, LibreOffice.

---
**Note:** Visual evidence for each step is available in the `screenshots/` directory of this project.
