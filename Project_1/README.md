# Cibersegurança 🛡️

[cite_start]**Autor:** FMartinsCyberSec [cite: 11]

---

## 📑 Descrição do Projeto
Este projeto documenta a resolução de uma prova prática de cibersegurança ofensiva e defensiva, focada em:
1. **CTF & Criptoanálise:** Exploração de arquivos e quebra de hashes.
2. **Pentest Técnico:** Auditoria completa e análise de risco numa máquina virtual (Windows XP).

---

## 🛠️ Parte 1: Análise Forense e Cracking (try_open_me.zip)

[cite_start]Foi realizada a análise do repositório `hackTHEtask` para obter informações críticas de um arquivo ZIP protegido. [cite: 18, 25]

### Metodologia e Ferramentas:
- [cite_start]**Enumeração:** Listagem de ficheiros internos (Blackbeard, Captain Hook, Captain Kidd, etc). [cite: 49]
- [cite_start]**Zip2John:** Conversão do arquivo ZIP para formato hash. [cite: 54]
- [cite_start]**John the Ripper:** Quebra da password do arquivo ZIP utilizando a wordlist `rockyou.txt`. [cite: 63, 68]
  - [cite_start]**Password Encontrada:** `ilove2shop` [cite: 72]

### Hashes Desencriptados (Hashcat):
| Ficheiro | Algoritmo | Hash | Password |
| :--- | :--- | :--- | :--- |
| `Blackbeard.txt` | [cite_start]MD5 [cite: 98] | [cite_start]`ecbf92...a3d3` [cite: 87] | [cite_start]**maximillian** [cite: 142] |
| `Captain Kidd.txt` | [cite_start]SHA2-256 [cite: 147] | [cite_start]`f97598...2f85` [cite: 93] | [cite_start]**marquese** [cite: 185] |
| `Captain Hook.txt` | [cite_start]SHA2-512 [cite: 194] | [cite_start]`eabb2c...c11` [cite: 197] | [cite_start]**lilmisssunshine** [cite: 197] |
| `Wavebreaker.txt` | [cite_start]SHA1 [cite: 202] | [cite_start]`7005bc...4099` [cite: 96] | [cite_start]**me&him** [cite: 209] |
| `just_look_here.docx` | [cite_start]MS Office 2013 [cite: 229] | - | [cite_start]**briliant** [cite: 232] |

---

## 🛡️ Parte 2: Pentest Técnico (VM m00-dl3)

[cite_start]Auditoria técnica realizada numa máquina vulnerável para identificar falhas críticas de infraestrutura. [cite: 250, 253]

### 🔍 Fase de Reconhecimento:
- [cite_start]**Alvo:** 192.168.1.222 (VMware). [cite: 265, 300]
- [cite_start]**OS:** Windows XP SP2/SP3 (Sistema legado e altamente vulnerável). [cite: 304]
- [cite_start]**Serviços Críticos:** Apache 2.4.9, MySQL 5.x e SMB (portas 139/445). [cite: 272, 291, 297, 298]

### 💣 Vetores de Ataque Identificados:
1. [cite_start]**Misconfiguration SMB:** As partilhas `disknet` e `SharedDocs` permitiam acesso de leitura e escrita anónimo. [cite: 372, 373]
   - [cite_start]**PoC:** Foi realizado o upload de um ficheiro `malware.txt` com sucesso via `smbclient`. [cite: 387, 390]
2. [cite_start]**Brute Force:** Identificação de credenciais de utilizador root através da ferramenta Medusa. [cite: 405, 406]

### 💡 Recomendações de Mitigação:
- [cite_start]**Desativar SMBv1:** Bloqueio imediato das portas 139 e 445. [cite: 322, 323]
- [cite_start]**Isolamento (Air-Gap):** Colocar sistemas indispensáveis em VLANs isoladas. [cite: 334, 335]
- [cite_start]**Atualização de SO:** Migração para Windows 10/11 ou Linux LTS devido ao fim de suporte do XP. [cite: 333]

---

## 🔧 Ferramentas Utilizadas
- [cite_start]**Sistemas:** Kali Linux. [cite: 24, 32, 254]
- [cite_start]**Reconhecimento:** Nmap, Netdiscover. [cite: 258, 279]
- [cite_start]**Cracking:** John the Ripper, Hashcat, Medusa. [cite: 63, 101, 141, 406]
- [cite_start]**Análise:** ExifTool, LibreOffice. [cite: 220, 242]
