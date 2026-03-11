# Terraform Basics

## What It Is
Terraform is a declarative IaC tool that provisions cloud and platform resources via providers. It calculates execution plans and applies only required changes to reach desired state. This supports consistent environment creation and predictable infrastructure evolution.

## Key Concepts
- Providers connect Terraform to target APIs.
- Resources represent managed infrastructure objects.
- Variables and outputs enable reusable modules.
- State is critical and must be protected.

## Simple Example
```bash
provider "aws" { region = "us-east-1" }
resource "aws_s3_bucket" "logs" { bucket = "example-logs" }
```

## Practical Commands
```bash
# Initialize and plan
terraform init
terraform plan

# Apply and inspect managed objects
terraform apply
terraform state list
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
