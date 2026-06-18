# Investigation Report

## Case Information

- **Project:** Linux Scheduled Tasks & Persistence Investigation
- **Platform:** Kali Linux
- **Analyst:** Anon
- **Date:** 16 June 2026

---

## Executive Summary

A review of Linux scheduled tasks and persistence mechanisms was performed to identify unauthorized automation or malicious cron jobs. The investigation included inspection of user cron tables, root cron tables, system cron directories, cron service status, active processes, and systemd timers.

No suspicious persistence techniques were discovered.

---

## Investigation Steps

### 1. User Cron Jobs

Command executed:

```bash
crontab -l
```

Result:

```
no crontab for anon
```

No scheduled tasks existed for the current user.

---

### 2. Root Cron Jobs

Command executed:

```bash
sudo crontab -l
```

Result:

```
no crontab for root
```

No custom root cron jobs were configured.

---

### 3. System Cron Directories

The following directories were inspected:

- `/etc/cron.d`
- `/etc/cron.daily`
- `/etc/cron.hourly`
- `/etc/cron.weekly`
- `/etc/cron.monthly`

Observed entries consisted of standard maintenance scripts such as package updates, log rotation, system statistics collection, PHP session cleanup, and manual database updates.

No unauthorized scripts were identified.

---

### 4. System Crontab

`/etc/crontab` contained default scheduling entries responsible for hourly, daily, weekly, and monthly maintenance using `run-parts`.

No suspicious modifications were observed.

---

### 5. Cron Service

The cron daemon was active and running successfully.

Background scheduling functionality was operational without errors.

---

### 6. Running Processes

Process inspection confirmed a legitimate `/usr/sbin/cron` process executing under the root account.

No duplicate or suspicious cron-related processes were detected.

---

### 7. Systemd Timers

Several active timers were present for package management and system maintenance.

These timers appeared consistent with a standard Kali Linux installation.

---

## Security Assessment

| Check | Status |
|---------|--------|
| User cron jobs | No suspicious entries |
| Root cron jobs | No suspicious entries |
| `/etc/crontab` | Default configuration |
| Scheduled scripts | Legitimate |
| Cron service | Running normally |
| Running processes | Legitimate |
| systemd timers | Expected maintenance tasks |

---

## Final Verdict

No persistence mechanisms or malicious scheduled tasks were discovered during this investigation. The system's cron configuration appears secure and consistent with a standard Kali Linux environment.