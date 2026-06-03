---
name: prometheus-metrics
description: >
  Prometheus HTTP API query endpoints and PromQL metrics query wrappers.
---

# Prometheus Metrics Tool

## Overview
Prometheus is an open-source systems monitoring and alerting toolkit. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts if certain conditions are observed.

## PromQL Queries
```promql
# Instant Query: Get CPU usage rate
sum(rate(node_cpu_seconds_total{mode="system"}[5m])) by (instance)

# Range Query: Memory usage percentage
(node_memory_MemTotal_bytes - node_memory_MemAvailable_bytes) / node_memory_MemTotal_bytes * 100
```

## REST API Endpoints
Prometheus exposes HTTP endpoints on port 9090.
- **Instant Query**: `GET /api/v1/query?query=<expression>&time=<timestamp>`
- **Range Query**: `GET /api/v1/query_range?query=<expression>&start=<start>&end=<end>&step=<step>`
