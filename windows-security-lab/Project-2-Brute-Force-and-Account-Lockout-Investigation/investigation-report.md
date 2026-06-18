# Investigation Report

## Project 2 - Brute Force and Account Lockout Investigation

## Objective

The objective of this investigation was to analyze multiple failed login attempts against a Windows user account, determine whether an account lockout occurred, and document the sequence of events using Windows Security Logs.

---

# Incident Summary

A Windows user account named **targetuser** experienced multiple failed login attempts within a short period. The repeated authentication failures triggered the Windows account lockout policy. After administrative intervention, the account was unlocked and successfully accessed.

---

# Lab Environment

* Operating System: Windows 10
* Tools Used:

  * Event Viewer
  * Windows Security Logs
  * Command Prompt
* Target Account: targetuser

---

# Evidence Collected

## Event IDs Investigated

| Event ID | Description          |
| -------- | -------------------- |
| 4625     | Failed Login Attempt |
| 4740     | Account Locked Out   |
| 4624     | Successful Login     |

---

# Event ID 4625 Analysis

## Description

Event ID 4625 records failed authentication attempts.

## Findings

The following failed login attempts were identified:

* 11:50:01 PM
* 11:50:07 PM
* 11:50:10 PM
* 11:50:13 PM
* 11:50:17 PM
* 11:50:22 PM
* 11:51:02 PM
* 11:51:51 PM
* 11:53:18 PM

### Total Failed Attempts

9

### Target Account

targetuser

## Security Relevance

Repeated failed login attempts may indicate:

* Password guessing
* Brute-force attacks
* User authentication errors

---

# Event ID 4740 Analysis

## Description

Event ID 4740 indicates that an account has been locked due to security policy enforcement.

## Findings

Account Lockout Time:

* 11:53:18 PM

Affected Account:

* targetuser

## Security Relevance

Account lockouts are important indicators of:

* Brute-force activity
* Password spraying attempts
* Excessive authentication failures

---

# Event ID 4624 Analysis

## Description

Event ID 4624 records successful authentication activity.

## Findings

Successful Login Time:

* 12:06:48 AM (June 14, 2026)

Account:

* targetuser

## Security Relevance

Successful logins following lockout events should be reviewed to determine whether access was legitimate or potentially unauthorized.

---

# Timeline of Events

| Time        | Event                   |
| ----------- | ----------------------- |
| 11:50:01 PM | Failed Login Attempt    |
| 11:50:07 PM | Failed Login Attempt    |
| 11:50:10 PM | Failed Login Attempt    |
| 11:50:13 PM | Failed Login Attempt    |
| 11:50:17 PM | Failed Login Attempt    |
| 11:50:22 PM | Failed Login Attempt    |
| 11:51:02 PM | Failed Login Attempt    |
| 11:51:51 PM | Failed Login Attempt    |
| 11:53:18 PM | Failed Login Attempt    |
| 11:53:18 PM | Account Locked (4740)   |
| 12:06:48 AM | Successful Login (4624) |

---

# Findings

* Multiple failed login attempts targeted the account "targetuser".
* The Windows account lockout policy successfully prevented further login attempts.
* Administrative action was required to restore account access.
* A successful login occurred after the account was unlocked.

---

# Security Assessment

The activity observed during this investigation closely resembles a brute-force attack scenario. Multiple authentication failures were recorded before the account lockout policy was triggered.

No evidence of unauthorized access was identified. The successful login was performed as part of the controlled lab exercise after account recovery.

---

# Recommendations

1. Maintain account lockout policies to mitigate brute-force attacks.
2. Monitor repeated Event ID 4625 occurrences.
3. Investigate unusual authentication patterns.
4. Enforce strong password requirements.
5. Configure centralized log monitoring using a SIEM platform.

---

# Conclusion

This investigation demonstrated how Windows Security Logs can be used to detect and analyze brute-force activity. Event IDs 4625, 4740, and 4624 were used to reconstruct the incident timeline and understand the sequence of authentication events.

The exercise provided practical experience with account lockout investigations and reinforced fundamental SOC analyst skills related to authentication monitoring and incident analysis.
