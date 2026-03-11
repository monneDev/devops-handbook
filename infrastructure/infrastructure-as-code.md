# Infrastructure As Code

## What It Is
Infrastructure as Code manages infrastructure with versioned configuration files instead of manual console changes. This improves repeatability, reviewability, and change auditing across environments. IaC is a foundational DevOps practice for scalable platform operations.

## Key Concepts
- Infrastructure changes go through pull request review.
- State tracking maps config to real resources.
- Modules reduce repetition and standardize patterns.
- Policy checks enforce governance automatically.

## Simple Example
```bash
terraform fmt
terraform validate
terraform plan
terraform apply
```

## Practical Commands
```bash
# Standard change flow
terraform fmt -recursive
terraform validate
terraform plan -out=tfplan
terraform apply tfplan
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
