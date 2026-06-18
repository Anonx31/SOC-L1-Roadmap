# Linux Network Investigation Report

## Investigation Summary

A network investigation was performed on a Kali Linux virtual machine to collect information about interfaces, routes, active connections, DNS settings, and connectivity.

## Observations

### Network Interface

The `ip a` command showed the primary interface `eth0` with an IPv4 address assigned.

Result:
- Interface: eth0
- IPv4 Address: 10.0.2.15

---

### Routing Table

The routing table indicates that traffic is routed through the default gateway.

Result:
- Default Gateway: 10.0.2.2
- Network: 10.0.2.0/24

---

### Listening Ports

No significant listening TCP services were identified, reducing the attack surface.

---

### Active Connections

A UDP connection related to DHCP communication was observed.

No suspicious outbound or inbound sessions were detected.

---

### ARP Cache

The ARP table contained the gateway mapping for the local network.

---

### DNS Configuration

`/etc/resolv.conf` specifies a configured nameserver used for domain resolution.

DNS resolution is functioning correctly.

---

### Connectivity Tests

Ping to 8.8.8.8 completed successfully.

Ping to google.com also completed successfully, confirming both network and DNS functionality.

---

## Security Assessment

No suspicious services or abnormal network activity were identified during this investigation.

The host appears to be operating normally within a controlled virtual machine environment.

## Conclusion

The Linux system demonstrated healthy network connectivity with proper routing, DNS configuration, and minimal active network exposure.