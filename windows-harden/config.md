## 🔍 Sysmon Configuration

This project uses [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon) with the [SwiftOnSecurity Sysmon configuration](https://github.com/SwiftOnSecurity/sysmon-config/blob/master/sysmonconfig-export.xml) to monitor system-level activity during attack simulations.

### Purpose

The `sysmonconfig-export.xml` is designed to:
- Capture high-value security events with minimal noise
- Support threat detection and forensic analysis
- Provide visibility into attacker behavior without requiring a full SIEM stack

### Logged Events Include
- Process creation and command-line usage (Event ID 1)
- Network connections made by executables (Event ID 3)
- File and registry modifications
- Driver and image loading events
- DNS queries and named pipe activity (optional/noisy)

### Usage

Sysmon was installed on the Windows VM with the following configuration:

```bash
sysmon.exe -accepteula -i sysmonconfig-export.xml

