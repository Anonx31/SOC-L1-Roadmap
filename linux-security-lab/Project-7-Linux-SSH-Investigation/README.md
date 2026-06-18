# Project 7 – Linux SSH Investigation

## Objective

Investigate the Secure Shell (SSH) configuration and status on a Kali Linux system from a SOC Analyst perspective.

The goal of this project is to determine whether the SSH service is running, inspect authentication settings, review login history, and identify potential indicators of unauthorized remote access.

---

## Tools Used

- Kali Linux
- systemctl
- ps
- ss
- grep
- journalctl
- last
- who

---

## Investigation Steps

- Checked SSH service status
- Examined running SSH-related processes
- Verified whether port 22 was listening
- Reviewed SSH authentication configuration
- Inspected the SSH daemon configuration
- Reviewed SSH-related system logs
- Examined historical login records
- Identified currently logged-in users

---

## Findings

- OpenSSH Server package is installed.
- SSH service (`sshd`) is currently **inactive (dead)**.
- SSH service is **disabled** and does not start automatically.
- No process is listening on TCP port 22.
- Only the local `ssh-agent` process is running.
- Root login remains commented out (default behavior).
- Password authentication is enabled in the configuration.
- No evidence of active remote SSH sessions was observed.
- Login history contains previous local user sessions.
- Current logged-in user is `anon`.

---

## Conclusion

No suspicious SSH activity was identified during this investigation. The SSH daemon is not running and the system is not accepting remote SSH connections. Current evidence indicates only local user activity.

---

## MITRE ATT&CK

- T1021.004 – SSH
- T1078 – Valid Accounts

---

## Screenshots

- ssh-service-status.png
- ssh-processes.png
- ssh-port-22.png
- ssh-config.png
- sshd-config-top.png
- ssh-journal.png
- login-history.png
- logged-in-users.png