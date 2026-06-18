# Investigation Report

## Project 2 - Linux User, Login & Privilege Investigation

## Objective

To perform a security-focused review of user accounts, login activity, and privilege assignments on a Linux system.

---

## Executive Summary

A Linux workstation was examined to identify active users, review login history, inspect privilege assignments, and enumerate local accounts. Standard Linux utilities were used to gather evidence and assess the system from a defender's perspective.

---

## Investigation Performed

### 1. System Identification

The current user, hostname, operating system information, and user identity were collected using native Linux commands.

### 2. Active Sessions

Current login sessions were reviewed using `who` and `w` to identify interactive users connected to the system.

### 3. Login History

Historical login information was reviewed using `last`. Any absence of historical records was documented as expected for a controlled lab environment.

### 4. Privilege Analysis

User identity and group memberships were verified using `id` and `groups`. Where available, `sudo -l` was used to inspect elevated privileges.

### 5. Local User Enumeration

Local accounts were reviewed using `/etc/passwd` to distinguish system accounts from regular user accounts.

---

## Security Observations

* No suspicious login activity was identified during testing.
* The investigation established a baseline for normal user activity.
* User and privilege enumeration techniques can assist in detecting unauthorized access and privilege abuse.

---

## Recommendations

1. Periodically review user accounts and group memberships.
2. Monitor login activity for unusual access patterns.
3. Apply the principle of least privilege.
4. Audit privileged accounts regularly.
5. Forward authentication logs to a centralized SIEM when available.

---

## Conclusion

The investigation successfully demonstrated Linux user and privilege analysis techniques that are directly applicable to SOC operations, incident response, and security monitoring.
