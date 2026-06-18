# Project 6 – Linux Network Investigation

## Overview

This project demonstrates basic Linux network investigation techniques using built-in command-line tools. The objective was to inspect network interfaces, routing information, active connections, DNS configuration, ARP cache, and connectivity.

## Objectives

- Identify network interfaces and IP addresses
- Review the routing table
- Check listening ports and active connections
- Inspect ARP cache entries
- Verify DNS configuration
- Test network connectivity
- Document findings from a security perspective

## Tools Used

- ip
- ss
- netstat
- arp
- hostname
- ping
- cat

## Commands Executed

```bash
ip a
ip route
ss -tulnp
ss -tunp
netstat -rn
hostname -i
arp -a
cat /etc/resolv.conf
ping -c 4 8.8.8.8
ping -c 4 google.com
```

## Screenshots

- network-interfaces.png
- routing-table.png
- listening-ports.png
- active-network-connections.png
- netstat-routing-table.png
- host-ip-address.png
- arp-cache.png
- dns-configuration.png
- ping-google-dns.png
- ping-google-domain.png

## Key Findings

- Active interface: `eth0`
- Assigned IPv4 address: `10.0.2.15`
- Default gateway: `10.0.2.2`
- DNS resolution functioning correctly
- Internet connectivity verified successfully
- ARP cache contains the local gateway entry
- Very few active network connections, indicating a clean lab environment

## Skills Demonstrated

- Linux networking fundamentals
- Network diagnostics
- Routing analysis
- DNS verification
- Connectivity testing
- Security investigation methodology