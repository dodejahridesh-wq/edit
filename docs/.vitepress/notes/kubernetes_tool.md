---
name: kubernetes-tool
description: >
  Automated container orchestration: deployment, scaling, and management.
---

# Kubernetes Orchestration Tool

## Overview
Kubernetes (K8s) is an open-source system for automating deployment, scaling, and management of containerized applications. It groups containers that make up an application into logical units for easy management and discovery.

## Common CLI Commands
```bash
# Apply a configuration file
kubectl apply -f deployment.yaml

# Get running pods
kubectl get pods -o wide

# Describe a deployment detail
kubectl describe deployment/my-service

# Port-forward a service to local machine
kubectl port-forward service/my-service 8080:80
```

## REST API Integration
The Kubernetes API server exposes OpenAPI-compliant HTTP endpoints to control resources.
- **List Pods in default namespace**: `GET /api/v1/namespaces/default/pods`
- **Create Deployment**: `POST /apis/apps/v1/namespaces/default/deployments`
