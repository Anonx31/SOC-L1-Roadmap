# Linux Security Audit Report

## Project 1 - Linux Security Audit

## Objective

The objective of this project was to perform a basic security audit of a Linux system by collecting system information, reviewing user accounts, inspecting running processes, examining network configuration, and identifying potential security-relevant observations.

---

## Lab Environment

* **Operating System:** Kali Linux
* **Platform:** VirtualBox
* **Audit Type:** Local Host Security Review

---

## Scope of Assessment

The following areas were reviewed:

* System Information
* Current User and Host Details
* User Accounts
* Running Processes
* Active Network Configuration
* Open Ports and Listening Services
* Disk Usage
* File Permissions
* Environment Variables

---

## Commands Executed

| Category              | Command           |
| --------------------- | ----------------- |
| Current User          | `whoami`          |
| Hostname              | `hostname`        |
| System Information    | `uname -a`        |
| Current Sessions      | `who`             |
| User Accounts         | `cat /etc/passwd` |
| Running Processes     | `ps aux`          |
| Network Interfaces    | `ip a`            |
| Routing Information   | `ip route`        |
| Open Connections      | `ss -tulnp`       |
| Disk Usage            | `df -h`           |
| Memory Usage          | `free -h`         |
| Environment Variables | `env`             |

---

## Findings

### 1. System Information

The Linux system information was successfully collected, confirming the operating system version and kernel details.

**Status:** Reviewed

---

### 2. User Context

The currently logged-in user and hostname were verified using standard Linux commands.

**Status:** Verified

---

### 3. User Accounts

Local user accounts were enumerated through `/etc/passwd` for awareness of available accounts on the system.

**Status:** Reviewed

---

### 4. Running Processes

Active processes were inspected to understand which applications and services were running during the audit.

No obviously suspicious processes were identified during the review.

**Status:** Normal

---

### 5. Network Configuration

Network interfaces and routing information were examined to verify connectivity and understand the host configuration.

**Status:** Reviewed

---

### 6. Listening Services

Open ports and listening services were checked using socket inspection commands.

Only expected services should be exposed on production systems, and any unnecessary services should be disabled.

**Status:** Reviewed

---

### 7. Disk and Memory Utilization

Basic storage and memory usage were reviewed to ensure the system was operating within expected limits.

**Status:** Reviewed

---

## Security Observations

* System information can provide valuable reconnaissance data if exposed to attackers.
* Running processes should be periodically reviewed for unauthorized applications.
* Open network ports should be minimized according to the principle of least privilege.
* Regular audits of user accounts help detect unauthorized access or stale accounts.
* Monitoring system resources can help identify unusual activity or compromise.

---

## Recommendations

1. Regularly review running processes and active services.
2. Minimize unnecessary open ports.
3. Periodically audit local user accounts.
4. Keep the operating system updated with security patches.
5. Monitor authentication and system logs for suspicious activity.
6. Implement centralized logging and SIEM integration for continuous monitoring.

---

## Skills Demonstrated

* Linux System Enumeration
* User and Process Investigation
* Network Inspection
* Security Auditing
* Basic Threat Hunting
* Command-Line Proficiency
* Documentation and Reporting

---

## Conclusion

This project provided hands-on experience performing a foundational Linux security audit using native command-line tools. The collected information demonstrates how defenders can assess a system's security posture, establish a baseline for normal activity, and identify areas requiring further investigation.

These techniques form an essential part of Security Operations Center (SOC) workflows and incident response activities.
