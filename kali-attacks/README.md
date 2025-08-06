# 🐚 Kali Attacker VM – Simulation & Adversary Emulation

This Kali Linux virtual machine simulates attacker behavior targeting the Windows detection lab. It leverages preinstalled tools to perform reconnaissance, command execution, and payload delivery based on MITRE ATT&CK techniques.

---

## ⚙️ System Overview

- **OS:** Kali Linux (VirtualBox)
- **Networking:** Host-only / Internal (connected to Windows VM)
- **Role:** Red Team simulation and command delivery
- **Connectivity:** Verified via ping and TCP scan to Windows VM

---

## 🔧 Tools ()

| Tool            | Purpose                                |
|------------------|----------------------------------------|
| `nmap`           | Port scanning and service enumeration  |
| `hydra`     |  brute-force attacks to test login credentials on Windows machine     |
|          |     |
|       |    |
|   |    |
|   |        |

---

## 🧪 Simulated Attacks

✅ In Progress:
- Port scan against Windows (`T1046`)
- SMB enumeration (`T1071.001`)
- Encoded PowerShell command (`T1059.001`)
- Reverse shell generation with payload staging

🔜 Upcoming:
- Privilege escalation test (`T1068`)
- Registry modification simulation
- MITRE technique correlation documentation

---

## 📄 Logs & Notes (in `/logs/`) 

- `attack-event-correlations.md` – Mapping attack to detection events  
- `payload-history.md` – Stored PowerShell and shell command samples  

---

## 🧠 Skills Demonstrated

- Adversarial simulation aligned with MITRE ATT&CK
- Red team enumeration and payload staging
- Command obfuscation and delivery via CLI
- Detection awareness through cross-system validation
- Technical writeups and lab documentation


