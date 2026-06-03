---
name: nmap-scanning
description: >
  Network discovery and vulnerability scanning tool.
---

# Nmap Network Scanner

## Overview
Nmap (Network Mapper) is a free and open-source utility for network discovery and security auditing. It scans hosts and ports to identify services running on a network.

## Common CLI Commands
```bash
# Simple ping scan to find active hosts
nmap -sn 192.168.1.0/24

# Service version detection and OS fingerprinting
nmap -A -T4 192.168.1.50

# Scan specific ports
nmap -p 22,80,443 192.168.1.50

# Run vulnerability assessment script
nmap --script vuln 192.168.1.50
```

## Integration
Nmap is a CLI-only tool. Programmatic integrations typically execute Nmap via subprocesses and parse JSON/XML outputs (`-oX` flags) using libraries like `python-nmap`.
