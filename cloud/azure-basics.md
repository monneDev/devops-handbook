# Azure Basics

## What It Is
Azure provides cloud services for compute, storage, networking, and managed Kubernetes. Typical DevOps workflows combine Azure identity, resource groups, virtual networks, and monitoring tools. Automation with CLI and IaC keeps environment setup repeatable.

## Key Concepts
- Resource groups organize lifecycle and ownership.
- Role-based access control enforces least privilege.
- VNets and subnets segment workloads securely.
- Azure Monitor collects metrics and logs.

## Simple Example
```bash
az group list --output table
az vm list -d --output table
```

## Practical Commands
```bash
# Authenticate and select subscription
az login
az account show --output table

# Review resources
az group list --output table
az vm list -d --output table
```

## Why It Matters in DevOps
This concept matters because it improves delivery reliability, operational speed, and change safety across environments.
- Reduces deployment and rollback risk through repeatable workflows.
- Improves collaboration between developers and platform teams.
- Speeds troubleshooting with clear operational procedures.

## Common Pitfalls
- Applying commands manually without documenting process and ownership.
- Skipping pre-deployment validation and post-deployment verification.
- Ignoring security basics such as least privilege and secret handling.

## Quick Checklist
- Keep commands version-controlled with the related docs.
- Validate changes in a safe environment before production.
- Review and update procedures after incidents or platform changes.
