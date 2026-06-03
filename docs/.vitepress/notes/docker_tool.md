---
name: docker-tool
description: >
  Build, ship, and run containers; the industry-standard container runtime.
---

# Docker Container Tool

## Overview
Docker enables developers to package applications into containers—standardized executable components combining application source code with the operating system libraries and dependencies required to run that code in any environment.

## Common CLI Commands
```bash
# Build an image
docker build -t my-app .

# Run a container in detached mode mapping port 8080
docker run -d -p 8080:80 my-app

# List active containers
docker ps

# Stream logs of a container
docker logs -f <container_id>
```

## REST API Integration
The Docker Engine API exposes RESTful endpoints over a Unix socket (`/var/run/docker.sock`) or TCP.
- **Get container list**: `GET /containers/json`
- **Inspect container**: `GET /containers/{id}/json`
- **Start container**: `POST /containers/{id}/start`
