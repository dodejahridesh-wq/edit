---
name: shodan-search
description: >
  REST API search engine to discover Internet-connected devices, hosts, and vulnerabilities.
---

# Shodan Search Engine

## Overview
Shodan is a search engine that lets the user find specific types of computers (routers, servers, etc.) connected to the internet using a variety of filters.

## Common CLI Commands
```bash
# Initialize API key
shodan init <API_KEY>

# Search details of a specific IP
shodan host 8.8.8.8

# Search for devices running webcams
shodan search webcam
```

## REST API endpoints
Shodan uses simple GET endpoints with an `key` parameter.
- **Host details**: `GET https://api.shodan.io/shodan/host/{ip}?key={API_KEY}`
- **Search database**: `GET https://api.shodan.io/shodan/host/search?key={API_KEY}&query={query}`
