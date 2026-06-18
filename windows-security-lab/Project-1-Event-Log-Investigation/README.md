# Windows Security Lab - Project 1: Event Log Investigation

## Project Overview

This project focuses on analyzing Windows Security Event Logs using Event Viewer and PowerShell. The objective is to understand how Windows records authentication events, user account activity, and administrative actions that are commonly investigated by SOC Analysts.

## Objectives

* Create and manage Windows user accounts
* Generate authentication events
* Investigate successful logins
* Investigate failed login attempts
* Monitor account creation and deletion activities
* Use PowerShell to gather security information

## Lab Environment

### Operating System

* Windows 10 / Windows 11

### Virtualization Platform

* VirtualBox

### Tools Used

* Event Viewer
* Command Prompt
* PowerShell

## Event IDs Investigated

### Event ID 4624

**Description:** Successful Login

**Purpose:**
Records successful authentication activity.

**Information Collected:**

* Username
* Logon Type
* Time Generated

### Event ID 4625

**Description:** Failed Login Attempt

**Purpose:**
Records unsuccessful authentication attempts.

**Information Collected:**

* Username
* Failure Reason
* Time Generated

### Event ID 4720

**Description:** User Account Created

**Purpose:**
Records the creation of a local user account.

**Information Collected:**

* Account Name
* Creator Account
* Creation Time

### Event ID 4726

**Description:** User Account Deleted

**Purpose:**
Records the deletion of a local user account.

**Information Collected:**

* Deleted Account Name
* Responsible User
* Deletion Time

## PowerShell Investigation

### Commands Used

```powershell
Get-LocalUser

Get-WinEvent -LogName Security -MaxEvents 20
```

### Purpose

* Enumerate local users
* Review recent security events
* Understand PowerShell-based log analysis

## Screenshots

The screenshots folder contains:

* user_creation.png
* failed_login_4625.png
* successful_login_4624.png
* account_creation_4720.png
* account_deletion_4726.png
* powershell_localuser.png
* powershell_events.png

## Skills Demonstrated

* Windows Administration
* Event Log Analysis
* User Account Management
* Authentication Investigation
* PowerShell Fundamentals
* Security Monitoring

## SOC Relevance

Windows Security Logs are one of the primary sources of information used by SOC Analysts. Authentication events, account modifications, and administrative actions often provide critical evidence during security investigations.

## Lessons Learned

This project provided hands-on experience with Windows event logs and demonstrated how user activities generate security events. Understanding these logs is essential for incident investigation and threat detection.

## Future Improvements

* Account Lockout Analysis
* PowerShell Logging Investigation
* Windows Defender Monitoring
* Sysmon Integration
* Threat Hunting Using Event Logs
