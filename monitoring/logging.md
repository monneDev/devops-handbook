# Logging

## What It Is
Logging captures event records from applications and infrastructure for debugging, auditing, and incident analysis. Structured logs improve searchability and correlation across distributed services. Centralized logging is essential for scalable DevOps operations.

## Key Concepts
- Use structured JSON logs when possible.
- Include request or trace identifiers consistently.
- Redact secrets and sensitive payload fields.
- Set retention and indexing policies deliberately.

## Simple Example
```bash
{"level":"ERROR","service":"api","trace_id":"abc123","message":"database timeout"}
```

## Practical Commands
```bash
# Stream logs from deployment
kubectl logs -f deploy/api

# Filter JSON logs locally
cat app.log | jq 'select(.level=="ERROR") | {timestamp,service,message,trace_id}'
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
