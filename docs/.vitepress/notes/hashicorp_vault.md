---
name: hashicorp-vault
description: >
  Secrets management engine to store credentials and encrypt keys.
---

# HashiCorp Vault Secrets Manager

## Overview
Vault is an identity-based secrets and encryption management system. It provides security shielding for sensitive application configuration data like API keys, database credentials, and certificates.

## Common CLI Commands
```bash
# Start Vault in dev mode
vault server -dev

# Write a key-value secret
vault kv put secret/my-app db_password="supersecretpassword"

# Retrieve the secret
vault kv get secret/my-app
```

## REST API Integration
Vault has a primary REST HTTP API covering all actions.
- **Read Secrets**: `GET /v1/secret/data/my-app` (Header: `X-Vault-Token`)
- **Rotate keys**: `POST /v1/transit/keys/my-key/rotate`
