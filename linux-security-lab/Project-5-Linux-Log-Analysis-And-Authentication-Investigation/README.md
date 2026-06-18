# Linux Log Analysis & Authentication Investigation

## Overview

This project demonstrates basic Security Operations Center (SOC) Level 1 log analysis skills on a Kali Linux system. The investigation focuses on reviewing authentication events, user sessions, login history, sudo activity, kernel logs, and system journal entries to identify potentially suspicious behavior.

## Objectives

- Analyze Linux system logs using `journalctl`
- Review authentication and session activity
- Examine user login history
- Verify active users and account information
- Inspect sudo-related events
- Review kernel and system messages
- Document findings in a structured investigation report

## Tools Used

- Kali Linux
- journalctl
- last
- who
- id
- dmesg
- grep

## Commands Executed

```bash
journalctl -n 50
journalctl | grep -i "session"
last
who
id
dmesg | tail -20
journalctl | grep sudo
last reboot
```

## Key Findings

- Recent journal entries contained normal system service activity.
- Authentication sessions were successfully created and closed.
- Login history showed expected interactive logins with no obvious anomalies.
- The currently active user was `anon`.
- User identity and group memberships were verified successfully.
- Sudo logs indicated expected privilege escalation events.
- Kernel messages primarily contained VirtualBox-related information.
- No evidence of suspicious authentication attempts or unauthorized access was identified during this investigation.

## Skills Demonstrated

- Linux log analysis
- Authentication investigation
- Session monitoring
- User activity review
- Sudo event analysis
- Basic SOC investigation methodology
- Documentation and reporting

## Conclusion

The reviewed logs indicate expected system behavior with no immediately suspicious authentication or privilege escalation activity observed during the investigation.