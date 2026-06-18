# Investigation Report – Linux Process & Service Analysis

## Incident ID
LAB-004

## Analyst
Anon31

## Date
16 June 2026

---

# Executive Summary

A manual inspection of system processes, services, user sessions, and network state was conducted to establish a baseline for the Linux host.

No evidence of malware, unauthorized users, suspicious services, or abnormal resource utilization was discovered.

---

# Evidence Collected

## Host Information

- OS: Kali Linux
- Kernel: 6.18.12-kali-amd64

---

## User Sessions

Command:
```bash
who
```

Result:
- One logged-in user (`anon`)
- Local graphical session only

Assessment:
Normal.

---

## CPU Analysis

Command:

```bash
ps aux --sort=-%cpu | head
```

Findings:
- qterminal
- Xorg
- Shell processes

Assessment:
No abnormal CPU consumption detected.

---

## Memory Analysis

Command:

```bash
ps aux --sort=-%mem | head
```

Findings:
- XFCE window manager
- Xorg
- qterminal
- Desktop helper processes

Assessment:
Expected desktop memory usage.

---

## Process Hierarchy

Command:

```bash
pstree
```

Findings:
Standard process tree rooted at `systemd` with XFCE components.

Assessment:
No suspicious child processes.

---

## Running Services

Command:

```bash
systemctl list-units --type=service --state=running
```

Observed:
- cron
- dbus
- NetworkManager
- polkit
- journald
- udisks2

Assessment:
Expected system services only.

---

## Cron Verification

Command:

```bash
systemctl status cron
```

Findings:
Cron service active and executing scheduled maintenance.

Assessment:
Healthy operation.

---

## SSH Review

Command:

```bash
ps aux | grep ssh
```

Findings:
Only `ssh-agent` process present.

Assessment:
No active remote SSH connections.

---

## Network Sockets

Command:

```bash
ss -tulnp
```

Findings:
No unexpected listening services.

Assessment:
Low attack surface.

---

# Risk Assessment

| Category | Status |
|-----------|--------|
| Suspicious Processes | None |
| Unauthorized Sessions | None |
| Suspicious Services | None |
| Active Backdoors | None |
| Network Exposure | Minimal |
| Overall Risk | Low |

---

# Final Verdict

This Linux host appears clean and consistent with a normal workstation baseline. No immediate security concerns or indicators of compromise were identified.