# Project 3 - Sysmon Investigation

## Overview

This project demonstrates the installation, configuration, and investigation of Sysmon (System Monitor) on Windows. Sysmon provides enhanced visibility into process creation, DNS queries, registry modifications, and other security-relevant activities.

The objective was to install Sysmon, generate activity, analyze Sysmon events, and map findings to MITRE ATT&CK techniques.

---

## Lab Environment

### Operating System

* Windows 10

### Tools Used

* Sysmon v15.20
* Event Viewer
* PowerShell

---

## Investigation Objectives

* Install Sysmon
* Verify Sysmon event collection
* Generate process creation events
* Analyze Event ID 1
* Review additional Sysmon telemetry
* Perform MITRE ATT&CK mapping

---

## Events Investigated

### Event ID 1

Process Creation

Example Processes:

* whoami.exe
* cmd.exe
* powershell.exe

### Additional Events Observed

* Event ID 13 - Registry Value Set
* Event ID 22 - DNS Query

---

## Skills Demonstrated

* Sysmon Deployment
* Process Monitoring
* Windows Log Analysis
* Event Investigation
* MITRE ATT&CK Mapping
* Threat Hunting Fundamentals

---

## Screenshots

* sysmon-installed.png
* sysmon-log.png
* event1_processcreation.png
* event1_details.png

---

## Key Takeaways

Sysmon provides significantly greater visibility than standard Windows Security Logs. Process creation events can be used to identify suspicious activity, investigate incidents, and support threat hunting operations.
