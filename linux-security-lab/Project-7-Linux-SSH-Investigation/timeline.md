# Investigation Timeline

| Step | Action |
|------|--------|
| 1 | Checked SSH service status using `systemctl status ssh` |
| 2 | Reviewed SSH-related processes with `ps aux \| grep ssh` |
| 3 | Verified port 22 exposure using `ss -tulpn \| grep :22` |
| 4 | Inspected SSH authentication settings in `sshd_config` |
| 5 | Reviewed beginning of SSH daemon configuration file |
| 6 | Examined SSH-related system logs using `journalctl` |
| 7 | Checked historical logins using `last` |
| 8 | Identified active users using `who` |
| 9 | Analyzed collected evidence |
| 10 | Concluded that SSH service is disabled and no remote SSH activity was present |