# MITRE ATT&CK Mapping

## Project 3 - Sysmon Investigation

| Activity                 | Sysmon Event | MITRE Technique | Description                            |
| ------------------------ | ------------ | --------------- | -------------------------------------- |
| whoami.exe Execution     | Event ID 1   | T1033           | System Owner/User Discovery            |
| cmd.exe Execution        | Event ID 1   | T1059.003       | Windows Command Shell                  |
| powershell.exe Execution | Event ID 1   | T1059.001       | PowerShell                             |
| DNS Queries              | Event ID 22  | T1016           | System Network Configuration Discovery |
| Registry Modifications   | Event ID 13  | T1112           | Modify Registry                        |

---

## Why MITRE Mapping Matters

MITRE ATT&CK provides a common language for describing attacker behavior.

By mapping Sysmon events to ATT&CK techniques, SOC analysts can:

* Identify attacker objectives
* Create detection rules
* Improve threat hunting
* Build SIEM alerts
* Support incident response investigations

---

## Key Observation

The execution of whoami.exe was successfully captured by Sysmon Event ID 1 and mapped to:

T1033 - System Owner/User Discovery

This technique is commonly observed during the Discovery phase of an attack lifecycle.
