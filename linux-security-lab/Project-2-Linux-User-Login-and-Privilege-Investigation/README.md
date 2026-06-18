# Project 2 - Linux User, Login & Privilege Investigation

## Overview

This project focuses on investigating user accounts, login activity, and privilege information on a Linux system from a Security Operations Center (SOC) perspective.

The objective was to understand how to enumerate users, inspect active sessions, review login history, and verify privilege assignments using native Linux commands.

---

## Lab Environment

* Operating System: Kali Linux
* Platform: VirtualBox
* Investigation Type: Local Host User & Privilege Review

---

## Objectives

* Identify the current user and system information
* Review active login sessions
* Analyze historical login records
* Verify user and group memberships
* Check privilege information
* Enumerate local user accounts

---

## Commands Used

```bash
whoami
hostname
uname -a
id
who
w
last
groups
sudo -l
cat /etc/passwd
```

---

## Skills Demonstrated

* Linux User Enumeration
* Login Session Analysis
* Privilege Investigation
* Group Membership Analysis
* Basic Threat Hunting
* Security Documentation

---

## Key Observations

* System identity was successfully verified.
* Active user sessions were reviewed.
* Login history was examined using available system utilities.
* User privileges and group memberships were inspected.
* Local accounts were enumerated for security awareness.

---

## Conclusion

This project demonstrates foundational Linux investigation techniques commonly used by SOC analysts during incident response, account reviews, and privilege investigations. Understanding user activity and permissions is essential for detecting unauthorized access and maintaining system security.
