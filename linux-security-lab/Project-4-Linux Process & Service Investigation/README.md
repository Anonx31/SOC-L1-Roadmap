# Linux Security Lab 4 – Process & Service Investigation

## Objective
Perform a baseline investigation of running processes, system services, user sessions, network sockets, and system uptime on a Linux host from the perspective of a SOC Level 1 analyst.

## Environment

- OS: Kali Linux
- Kernel: 6.18.12-kali-amd64
- Virtual Machine: Oracle VirtualBox
- Analyst User: anon

## Commands Used

```bash
uname -a
uptime
who
ps aux --sort=-%cpu | head
ps aux --sort=-%mem | head
pstree
systemctl list-units --type=service --state=running
systemctl status cron
ps aux | grep ssh
ss -tulnp
```

## Investigation Summary

### System Information
- Host running Kali Linux.
- Kernel version successfully identified.
- System uptime approximately 17 minutes during investigation.

### Logged-in Users
- One interactive user session detected.
- User: `anon`

### CPU Usage
Top resource consumers were desktop environment components:
- qterminal
- Xorg
- shell processes
- XFCE-related services

No suspicious CPU-intensive process observed.

### Memory Usage
Highest memory consumers included:
- xfwm4
- Xorg
- qterminal
- Python-based desktop utilities

Memory usage appeared normal for a GUI desktop environment.

### Process Tree
The process hierarchy was consistent with a standard XFCE desktop:
- systemd
- lightdm
- Xorg
- xfce-session
- xfwm4
- xfce-panel

No unexpected child processes or malicious persistence mechanisms detected.

### Running Services
Observed active services included:
- cron
- dbus
- NetworkManager
- systemd-journald
- polkit
- udisks2
- VirtualBox guest utilities

All services appeared legitimate.

### Cron Service
The cron daemon was active and running normally.
Recent logs showed scheduled system maintenance tasks.

### SSH Processes
Only helper (`ssh-agent`) process observed.
No active SSH server sessions or suspicious remote logins detected.

### Listening Ports
`ss -tulnp` returned no listening TCP/UDP services for the current user context.

## Conclusion

No indicators of compromise were identified during this baseline investigation.
The host exhibited expected behavior for a freshly started Kali Linux virtual machine running an XFCE desktop environment.

## Skills Practiced

- Process analysis
- Service enumeration
- Session monitoring
- Baseline system auditing
- Linux command-line investigation
- SOC L1 documentation