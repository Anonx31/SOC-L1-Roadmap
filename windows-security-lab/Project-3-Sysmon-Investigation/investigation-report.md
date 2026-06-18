# Investigation Report

## Project 3 - Sysmon Investigation

## Objective

To deploy Sysmon on a Windows system and investigate process creation events generated through normal system activity.

---

## Executive Summary

Sysmon was successfully installed and configured on a Windows 10 system. Event data was collected and reviewed using Event Viewer and PowerShell.

The investigation focused on Event ID 1 (Process Creation), which records detailed information about newly launched processes.

---

## Evidence Collected

### Sysmon Status

* Installed: Yes
* Version: 15.20
* Service Status: Running

### Log Source

Microsoft-Windows-Sysmon/Operational

---

## Event ID 1 Analysis

### Event Description

Event ID 1 records process creation activity.

### Observed Process

Process Name:

whoami.exe

Path:

C:\Windows\System32\whoami.exe

Command Line:

whoami

User:

DESKTOP-B7UMH2G\BOSS

Process ID:

4856

Timestamp:

2026-06-15 13:30:59.740 UTC

---

## Security Significance

The whoami command is commonly used to identify the current user context.

Attackers frequently execute commands such as:

* whoami
* hostname
* ipconfig
* net user

during the Discovery phase of an attack.

Monitoring process creation events allows defenders to identify potentially suspicious activity and reconstruct attacker behavior.

---

## Additional Telemetry Observed

### Event ID 22

DNS Query Activity

### Event ID 13

Registry Modification Activity

These events demonstrate Sysmon's ability to provide visibility beyond standard Windows Security Logs.

---

## Findings

* Sysmon was successfully deployed.
* Process creation telemetry was collected.
* Event ID 1 successfully captured command execution.
* Additional DNS and Registry events were observed.
* Sysmon provides enhanced visibility useful for SOC operations and threat hunting.

---

## Recommendations

1. Deploy Sysmon across monitored endpoints.
2. Forward Sysmon logs to a SIEM platform.
3. Monitor suspicious process execution.
4. Create alerts for PowerShell and command shell activity.
5. Correlate Sysmon events with MITRE ATT&CK techniques.

---

## Conclusion

This investigation demonstrated how Sysmon can be used to monitor endpoint activity and provide detailed visibility into process execution. Event ID 1 was analyzed to understand how commands are recorded and how defenders can use this telemetry during investigations.
