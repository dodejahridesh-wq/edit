---
name: terraform-tool
description: >
  Infrastructure as Code to provision and manage cloud infrastructure.
---

# Terraform IaC Tool

## Overview
Terraform is an open-source infrastructure as code software tool created by HashiCorp. Users define and provision data center infrastructure using a declarative configuration language known as HashiCorp Configuration Language (HCL).

## Common CLI Commands
```bash
# Initialize Terraform working directory
terraform init

# Generate and show an execution plan
terraform plan

# Build or change infrastructure
terraform apply

# Destroy Terraform-managed infrastructure
terraform destroy
```

## State & API
- **Local State**: Saved in `terraform.tfstate`.
- **HCP Terraform API**: Offers REST endpoints to trigger runs, manage variables, and upload configuration versions.
