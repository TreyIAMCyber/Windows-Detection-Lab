# 🛡️ Windows Detection Lab – Offensive Simulation & Defensive Logging
A self-contained cybersecurity lab simulating real-world attacker behavior against a Windows 10 virtual machine, with live telemetry and detection mechanisms configured to monitor malicious activity. Built using Kali Linux and VirtualBox, this project demonstrates practical blue team visibility aligned with MITRE ATT&CK techniques.

# 🚀 Objective
Design and deploy a local detection lab that allows experimentation with attacker techniques, visibility tooling, and security event logging—without relying on enterprise infrastructure or cloud-based solutions.

# 🧱 Lab Architecture
| Component      | Role                         | Key Capabilities                               |
|----------------|------------------------------|------------------------------------------------|
| Windows VM     | Target system                | Sysmon, Defender, PowerShell logging           |
| Kali Linux VM  | Attacker / simulation box    | Recon tools (`nmap`, `enum4linux`, `base64`)   |
| VirtualBox     | VM orchestration layer       | Hosts both machines with internal networking   |

Windows Configuration:

1. Non-admin test user (labuser)
2. Sysmon (64-bit) installed with advanced config
3. PowerShell ScriptBlock + Module Logging via Registry
4. Defender active and updated
5. Verified logs in Event Viewer (4103, 4104)

Kali Linux:
1. Tools used: nmap, enum4linux, base64, msfconsole
2. Internal networking (host-only) for VM interaction

# 🔍 Detection Capabilities

✅ Logged:
1. Encoded PowerShell commands
2. Module invocation events
3. ScriptBlock executions
4. Defender threat alerts
5. Sysmon process and network telemetry

🔜 Upcoming Simulations:
1. MITRE Techniques: T1059, T1047, T1086
2. Reverse shell payloads
3. Port scans and Windows service enumeration

# 📸 Documentation Highlights
| Screenshot                | Description                        |
|---------------------------|------------------------------------|
| sysmon-installed.png      | Sysmon installed via CMD           |
| registry-logging-setup.png| Registry keys for PowerShell logs |
| powershell-eventviewer.png| Captured ScriptBlock execution     |
| nmap-scan-results.png     | Kali scan showing open ports       |



### 🧠 Skills Demonstrated
- Detection Engineering: Built Sysmon and PowerShell logging stack  
- Threat Simulation: Emulated MITRE ATT&CK techniques  
- Event Log Analysis: Investigated Windows Event Viewer alerts  
- Windows Hardening: Configured registry for logging enhancements  
- Command-Line Tooling: Used `nmap`, `enum4linux`, `base64`, etc  
- Blue Team Visibility: Correlated attack behavior with detection signals  
- Virtual Lab Deployment: Deployed VMs with isolated networking  
- Technical Documentation: Wrote clear GitHub README and structure


### 📁 Repository Structure

- `/windows-harden/`
  - `README.md` – Windows logging setup
  - `images/` – Screenshots of configuration & logs
  - `config/` – Sysmon XML config

- `/kali-attacks/`
  - `README.md` – Simulated attacker behavior
  - `screenshots/` – Kali terminal output & scans
  - `logs/` – Correlated logs from Event Viewer

- `/` *(root directory)*
  - `README.md` – Overview of the project

# 📌 Why This Matters
This lab simulates real-world detection workflows and empowers defenders to understand attacker behavior from both sides of the wire. It serves as a practical portfolio piece to showcase your capabilities in building, analyzing, and documenting a complete security detection environment.
