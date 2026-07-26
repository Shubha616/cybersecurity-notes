## Topics Covered
- Introduction to Nmap
- Host Discovery
- ARP Scan
- ICMP Host Discovery
- Reverse DNS (rDNS)

## Key Concepts
Tcp Syn-"PS"
TCP Ack-"PA"
UDP-"PU"

### What is Nmap?
Nmap (Network Mapper) is a network scanning tool used to discover live hosts, open ports, running services, and operating systems.

### Host Discovery
Host discovery identifies which systems on a network are online before performing port scanning.

### ARP Scan
- Used only on the local network (same subnet).
- Maps an IP address to a MAC address.
- Fast and reliable for discovering live hosts.
- Command:
```bash
nmap -PR -sn 192.168.1.0/24
```

[[### ICMP Host Discovery
- `-PE` → ICMP Echo Request (Ping)
- `-PP` → ICMP Timestamp Request
- `-PM` → ICMP Address Mask Request]]
- 

### DNS Resolution
- `-n` → Disable DNS lookups (faster scan).
- `-R` → Force Reverse DNS lookups for all hosts.

## Useful Commands

```bash
# Scan a single host
nmap 192.168.1.1

# Scan multiple hosts
nmap 192.168.1.1 192.168.1.2

# Scan an entire subnet
nmap 192.168.1.0/24

# ARP Host Discovery
nmap -PR -sn 192.168.1.0/24

# ICMP Echo Host Discovery
nmap -PE -sn 192.168.1.0/24

# Disable DNS Resolution
nmap -n 192.168.1.1

# Force Reverse DNS Lookup
nmap -R 192.168.1.1
```

## Summary
Today I learned the fundamentals of Nmap, including host discovery techniques using ARP and ICMP, the difference between DNS resolution and Reverse DNS, and basic Nmap scanning commands. I also understood when to use `-n`, `-R`, `-PR`, `-PE`, `-PP`, and `-PM` during network reconnaissance.
