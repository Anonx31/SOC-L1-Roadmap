# Investigation Timeline

**Project:** Linux User, Login & Privilege Investigation  
**Date:** 16 June 2026  
**Time Zone:** Indian Standard Time (IST)

| Time (IST) | Activity |
|------------|----------|
| 07:24 PM | Collected system identification using `whoami`, `hostname`, `uname -a`, and `id`. |
| 07:25 PM | Reviewed active user sessions using `who`. |
| 07:26 PM | Examined logged-in user details and system load using `w`. |
| 07:26 PM | Verified sudo privileges using `sudo -l`. |
| 07:27 PM | Reviewed historical login records using `last`. |
| 07:28 PM | Enumerated local user accounts from `/etc/passwd`. |
| 07:29 PM | Checked group memberships using `groups`. |
| 07:30 PM | Recorded findings and completed the investigation. |

## Summary

The investigation confirmed that the active user (`anon`) was logged into the Kali Linux system, possessed administrative (`sudo`) privileges, and belonged to several system groups. Historical login records and local account enumeration were successfully reviewed, with no suspicious activity identified during this assessment.