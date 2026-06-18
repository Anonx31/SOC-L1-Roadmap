# Network Traffic Investigation Report

## Objective

The objective of this investigation was to capture and analyze network traffic using Wireshark in order to understand common protocols and identify network communication patterns.

---

# Tools Used

* Kali Linux
* Wireshark
* Ping Utility
* Web Browser

---

# Traffic Generation

The following activities were performed:

1. Pinged external hosts.
2. Visited websites.
3. Generated DNS lookups.
4. Captured network packets.

Traffic was recorded and saved in a PCAP file for analysis.

---

# DNS Analysis

## Filter Used

```text
dns
```

## Findings

* Multiple DNS queries were observed.
* Domain names were resolved into IP addresses.
* DNS responses provided destination IP information.

## Importance

DNS activity is valuable during investigations because malicious software often communicates using domain names before connecting to remote servers.

---

# ICMP Analysis

## Filter Used

```text
icmp
```

## Findings

* ICMP Echo Requests were identified.
* ICMP Echo Replies were successfully returned.
* Network connectivity was verified.

## Importance

ICMP traffic is commonly used for:

* Host discovery
* Connectivity testing
* Network troubleshooting

Attackers may also use ICMP during reconnaissance activities.

---

# TCP Analysis

## Filter Used

```text
tcp
```

## Findings

The TCP Three-Way Handshake was observed:

1. SYN
2. SYN-ACK
3. ACK

The connection was successfully established between client and server.

## Importance

TCP analysis helps identify:

* Network sessions
* Suspicious connections
* Unauthorized communications

---

# HTTP Analysis

## Filter Used

```text
http
```

## Findings

HTTP requests were captured and examined.

Observed:

* GET requests
* Host headers
* Server responses

## Importance

HTTP analysis can help identify:

* Malicious downloads
* Command-and-control traffic
* Suspicious web activity

---

# Investigation Summary

The packet capture successfully demonstrated the operation of several common network protocols including DNS, ICMP, TCP, and HTTP.

The captured traffic showed normal user activity and provided visibility into how systems communicate across a network.

No malicious activity was identified during this investigation.

---

# Skills Demonstrated

* Packet Analysis
* Protocol Identification
* Wireshark Investigation
* Traffic Monitoring
* Network Security Fundamentals

---

# Lessons Learned

This investigation improved my understanding of network communication and packet analysis. These skills are essential for SOC Analysts who investigate alerts, analyze network activity, and support incident response operations.

---

# Recommended Next Steps

* Analyze encrypted HTTPS traffic metadata.
* Investigate suspicious network behavior.
* Learn advanced Wireshark filters.
* Explore malware traffic analysis.
* Build SIEM-based network monitoring labs.
