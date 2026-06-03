---
name: owasp-zap-scan
description: >
  Dynamic Application Security Testing (DAST) vulnerability scanner.
---

# OWASP ZAP Vulnerability Scanner

## Overview
ZAP (Zed Attack Proxy) is an open-source web application security scanner. It acts as a proxy, intercepting and analyzing traffic to discover vulnerabilities in web applications and REST APIs.

## Common CLI Commands
```bash
# Start ZAP in headless/daemon mode
zap.sh -daemon -port 8090 -config api.key=12345

# Trigger a baseline scan using Python wrapper
zap-baseline.py -t https://example.com -g gen.conf -r report.html
```

## REST API Integration
When running in daemon mode, ZAP exposes an interactive API on the configured port.
- **Access API UI**: `http://localhost:8090/UI`
- **API endpoints**: For crawling (`/JSON/spider/action/scan/`), scanning (`/JSON/ascan/action/scan/`), and reports.
