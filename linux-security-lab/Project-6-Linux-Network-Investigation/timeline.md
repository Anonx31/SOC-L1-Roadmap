# Investigation Timeline

| Step | Activity |
|------|----------|
| 1 | Collected network interface information using `ip a` |
| 2 | Examined routing table using `ip route` |
| 3 | Checked listening ports using `ss -tulnp` |
| 4 | Reviewed active network connections using `ss -tunp` |
| 5 | Verified routing information with `netstat -rn` |
| 6 | Retrieved host IP information using `hostname -i` |
| 7 | Inspected ARP cache using `arp -a` |
| 8 | Reviewed DNS configuration in `/etc/resolv.conf` |
| 9 | Tested IP connectivity with `ping 8.8.8.8` |
| 10 | Tested DNS resolution with `ping google.com` |
| 11 | Analyzed results and documented findings |