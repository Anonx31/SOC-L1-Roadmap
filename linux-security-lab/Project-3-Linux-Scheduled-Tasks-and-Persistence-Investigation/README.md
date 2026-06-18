# Linux Scheduled Tasks & Persistence Investigation

## Overview

This project documents a security-focused investigation of scheduled tasks and persistence mechanisms on a Kali Linux system. The objective was to inspect cron jobs, system-wide scheduling configurations, and active timers to identify any unauthorized or suspicious persistence techniques.

## Objectives

- Examine user and root cron jobs
- Review system-wide cron configuration
- Inspect scheduled task directories
- Verify cron service status
- Identify running cron processes
- Enumerate active systemd timers
- Assess the system for persistence mechanisms

## Environment

- OS: Kali Linux
- Hostname: `kali`
- User: `anon`
- Investigation Date: 16 June 2026 (IST)

## Tools Used

- `crontab`
- `systemctl`
- `ps`
- `cat`
- `ls`
- `systemd timers`

## Screenshots

| Screenshot | Description |
|------------|-------------|
| `user-crontab.png` | User cron jobs |
| `root-crontab.png` | Root cron jobs |
| `cron-d-directory.png` | `/etc/cron.d` contents |
| `cron-daily-directory.png` | `/etc/cron.daily` contents |
| `cron-hourly-directory.png` | `/etc/cron.hourly` contents |
| `cron-weekly-directory.png` | `/etc/cron.weekly` contents |
| `cron-monthly-directory.png` | `/etc/cron.monthly` contents |
| `system-crontab.png` | `/etc/crontab` configuration |
| `cron-service-status.png` | Cron daemon status |
| `cron-process.png` | Running cron process |
| `systemd-timers.png` | Active systemd timers |

## Findings

- No user-specific cron jobs were configured.
- No root user cron jobs were present.
- Standard system scheduling directories contained expected maintenance scripts.
- The cron daemon was active and running normally.
- System-wide scheduling was configured through `/etc/crontab`.
- Active systemd timers were limited to legitimate maintenance and package management tasks.
- No evidence of malicious persistence or unauthorized scheduled tasks was identified.

## Conclusion

The investigation found only legitimate operating system scheduled tasks. No suspicious cron entries or persistence mechanisms were detected, indicating a clean scheduling configuration.