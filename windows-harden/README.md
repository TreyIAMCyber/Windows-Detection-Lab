# Windows Detection Lab – Hardened Logging & Visibility
This Windows VM is configured to simulate a realistic enterprise workstation with enhanced logging and visibility. It serves as the primary target system for attacker simulations originating from a Kali VM.

# ⚙️ System Overview
OS: Windows 10 (virtualized in VirtualBox)

User Account: labuser (non-admin)

### Security Tools:

- Microsoft Defender (enabled + updated)
- Sys

# 🛡️ Microsoft Defender
Role: Antivirus + Real-time protection

What It Does: Actively blocks known threats, malware, and suspicious behavior

Visibility: Generates alerts and quarantines based on signatures and heuristics

Detection Style: Preventive and reactive

# 🧠 Sysmon (System Monitor)
Role: Deep system logging tool

What It Does: Captures detailed telemetry like:

Process creation (Event ID 1)

Network connections (Event ID 3)

File modifications

Registry changes

Driver loading

Visibility: Logs raw data for correlation — doesn’t block, just reports

Detection Style: Passive visibility for analysis and hunting
