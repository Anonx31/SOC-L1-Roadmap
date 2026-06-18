# Linux Security Lab

## Project Overview

This project demonstrates fundamental Linux administration and security concepts that are commonly used in Security Operations Center (SOC) environments. The lab focuses on user management, group management, file permissions, and log investigation.

## Objectives

* Create and manage Linux users
* Create and manage security groups
* Configure file and directory permissions
* Investigate authentication logs
* Understand Linux security fundamentals relevant to SOC operations

## Lab Environment

* Operating System: Kali Linux
* Virtualization Platform: VirtualBox

## User Management

### Users Created

* analyst1
* analyst2

### Commands Used

```bash
sudo useradd analyst1
sudo useradd analyst2

sudo passwd analyst1
sudo passwd analyst2

cat /etc/passwd | grep analyst
```

### Outcome

Successfully created two analyst accounts and verified their existence within the system.

## Group Management

### Group Created

* socteam

### Commands Used

```bash
sudo groupadd socteam

sudo usermod -aG socteam analyst1
sudo usermod -aG socteam analyst2

groups analyst1
groups analyst2
```

### Outcome

Both analyst accounts were successfully added to the SOC team group.

## Directory Permission Management

### Commands Used

```bash
mkdir confidential_logs

ls -ld confidential_logs

chmod 700 confidential_logs

ls -ld confidential_logs
```

### Outcome

Access to the confidential_logs directory was restricted to the owner only.

## File Permission Management

### Commands Used

```bash
touch incident_report.txt

ls -l incident_report.txt

chmod 600 incident_report.txt

ls -l incident_report.txt
```

### Outcome

The incident report file was secured so that only the owner could read and modify it.

## Log Investigation

### Commands Used

```bash
sudo cat /var/log/auth.log | tail -20
```

Alternative:

```bash
sudo journalctl -xe
```

### Activities Performed

* Reviewed authentication events
* Examined login attempts
* Investigated sudo activity
* Observed user-related system events

## Screenshots

The screenshots folder contains evidence of:

* User creation
* Group creation
* Directory permissions
* File permissions
* Authentication log analysis

## Skills Demonstrated

* Linux Administration
* User and Group Management
* Permission Management
* Security Monitoring
* Log Analysis
* System Investigation

## Lessons Learned

This lab provided practical experience with Linux security fundamentals that are essential for SOC Analysts. Understanding users, permissions, and logs is critical for investigating security incidents and monitoring system activity.

## Future Improvements

* Advanced log analysis
* Linux hardening techniques
* Bash automation scripts
* Security monitoring tools
* Syslog server integration
