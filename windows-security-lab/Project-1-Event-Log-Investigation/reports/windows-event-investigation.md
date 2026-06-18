# Windows Event Investigation Report

## Objective

The objective of this investigation was to generate and analyze Windows Security Events associated with user authentication and account management activities.

## Tools Used

* Event Viewer
* Command Prompt
* PowerShell
* Windows Security Logs

---

# Event ID 4625 Analysis

## Event Description

Failed Login Attempt

## Activity Performed

A local user account was created and multiple login attempts were made using an incorrect password.

## Findings

* Multiple failed authentication attempts were recorded.
* The target username was successfully identified.
* Event timestamps confirmed when the attempts occurred.

## Security Relevance

Repeated Event ID 4625 entries may indicate:

* Password guessing attacks
* Brute-force attempts
* User authentication issues

---

# Event ID 4624 Analysis

## Event Description

Successful Login

## Activity Performed

The user successfully authenticated using valid credentials.

## Findings

* Successful authentication event recorded.
* User account activity was confirmed.
* Logon details were available for investigation.

## Security Relevance

Successful logins help analysts:

* Verify user activity
* Investigate account usage
* Build incident timelines

---

# Event ID 4720 Analysis

## Event Description

User Account Created

## Activity Performed

A temporary user account was created using administrative privileges.

## Findings

* User creation activity was recorded.
* The newly created account was identified.
* The creator account was logged.

## Security Relevance

Unexpected account creation events may indicate:

* Unauthorized access
* Persistence attempts
* Insider activity

---

# Event ID 4726 Analysis

## Event Description

User Account Deleted

## Activity Performed

The temporary account was removed from the system.

## Findings

* Account deletion event successfully recorded.
* Account name and timestamp were available.

## Security Relevance

Account deletion events may be associated with:

* Administrative cleanup
* Insider threats
* Attempts to remove evidence

---

# PowerShell Investigation

## Commands Executed

```powershell
Get-LocalUser

Get-WinEvent -LogName Security -MaxEvents 20
```

## Findings

* Local users were successfully enumerated.
* Recent security events were reviewed.
* PowerShell provided an alternative method for event investigation.

## Security Relevance

PowerShell is frequently used by administrators and attackers. Understanding PowerShell activity is essential for modern SOC investigations.

---

# Investigation Summary

The investigation successfully generated and analyzed Windows authentication and account management events. Multiple security-relevant Event IDs were reviewed using Event Viewer and PowerShell.

No malicious activity was identified during testing. All events were intentionally generated in a controlled lab environment.

---

# Key Event IDs Covered

| Event ID | Description          |
| -------- | -------------------- |
| 4624     | Successful Login     |
| 4625     | Failed Login         |
| 4720     | User Account Created |
| 4726     | User Account Deleted |

---

# Skills Demonstrated

* Event Viewer Analysis
* Windows Security Monitoring
* Authentication Investigation
* User Account Monitoring
* PowerShell Fundamentals
* SOC Investigation Workflow

---

# Lessons Learned

This investigation improved my understanding of Windows Security Logs and demonstrated how authentication and account management activities are recorded. These skills form an important foundation for SOC Analyst responsibilities involving log analysis and incident investigation.
