# AWS Basics

## What It Is
AWS offers a broad set of cloud services for compute, storage, networking, identity, and observability. DevOps teams commonly combine IAM, EC2, EKS/ECS, VPC, S3, and CloudWatch. Automation through CLI and IaC keeps AWS environments reproducible and auditable.

## Key Concepts
- IAM controls access via users, roles, and policies.
- VPC defines network boundaries and routing.
- S3 is a core durable storage service.
- CloudWatch provides metrics and alarms.

## Simple Example
```bash
aws s3 ls
aws ec2 describe-instances --max-results 5
```

## Practical Commands
```bash
# Confirm account and region
aws sts get-caller-identity
aws configure get region

# Inspect core resources
aws ec2 describe-instances --max-results 5
aws s3 ls
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
