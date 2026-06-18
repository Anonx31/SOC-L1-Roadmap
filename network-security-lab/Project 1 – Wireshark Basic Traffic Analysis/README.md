# Network Security Lab

## Project Overview

This project focuses on network traffic analysis using Wireshark. The objective is to understand how common network protocols operate and how packet analysis supports Security Operations Center (SOC) investigations.

## Objectives

* Capture live network traffic
* Analyze common network protocols
* Investigate DNS queries
* Examine ICMP traffic
* Understand TCP communication
* Review HTTP requests and responses
* Develop packet analysis skills

## Lab Environment

### Operating System

* Kali Linux

### Virtualization Platform

* VirtualBox

### Tools Used

* Wireshark
* Ping
* Web Browser

## Protocols Analyzed

* DNS
* ICMP
* TCP
* HTTP
* HTTPS
* UDP
* DHCP

## Activities Performed

### Traffic Capture

Generated network traffic by:

* Visiting websites
* Performing DNS lookups
* Sending ICMP requests using ping

### DNS Analysis

Examined:

* Domain name queries
* DNS responses
* Name resolution process

### ICMP Analysis

Observed:

* Echo Requests
* Echo Replies
* Host connectivity verification

### TCP Analysis

Investigated:

* TCP Three-Way Handshake
* Connection establishment
* Session communication

### HTTP Analysis

Reviewed:

* GET requests
* HTTP headers
* Server responses

## Repository Structure

```text
network-security-lab
│
├── README.md
│
├── screenshots
│   ├── wireshark_capture.png
│   ├── dns_analysis.png
│   ├── icmp_analysis.png
│   ├── tcp_handshake.png
│   ├── http_request.png
│   └── packet_details.png
│
├── notes
│   └── network-protocols.md
│
├── reports
│   └── network-traffic-investigation.md
│
└── pcaps
    └── basic-traffic-analysis.pcapng
```

## Skills Demonstrated

* Network Fundamentals
* Packet Analysis
* Wireshark Usage
* Protocol Identification
* Traffic Investigation
* Security Monitoring

## SOC Relevance

Network traffic analysis is a core responsibility of SOC Analysts. Understanding protocols and packet captures helps identify suspicious communications, investigate alerts, and support incident response activities.

## Lessons Learned

This project provided practical experience analyzing network traffic and understanding how communication occurs between systems. The skills gained are directly applicable to SOC monitoring and investigation tasks.

## Future Improvements

* Analyze malware traffic samples
* Investigate suspicious DNS activity
* Create protocol-based detection rules
* Perform threat hunting using packet captures
