---
name: pytorch-serve
description: >
  TorchServe model serving framework for deploying PyTorch models at scale.
---

# TorchServe PyTorch Model Serving

## Overview
TorchServe is a flexible and easy-to-use tool for serving PyTorch models. It supports multi-model serving, model versioning, logging, metrics reporting, and exposes REST APIs for inference and management.

## Common CLI Commands
```bash
# Start TorchServe loading config
torchserve --start --model-store model_store --models squeezenet1.1=squeezenet1.1.mar

# Stop TorchServe
torchserve --stop
```

## REST API Endpoints
- **Inference Port**: 8080 (endpoints like `POST /predictions/{model_name}`)
- **Management Port**: 8081 (endpoints like `GET /models` to view loaded models, `POST /models` to load new ones)
