# Deployments

## What It Is
Deployments manage stateless Pods through ReplicaSets and rolling updates. They provide version history, rollback support, and declarative scaling. This makes Deployments the default pattern for many web APIs and backend services.

## Key Concepts
- Replica count defines desired Pod instances.
- Rolling strategy controls update pace and disruption.
- Selectors bind Deployment to matching Pods.
- Revision history enables rollback.

## Simple Example
```bash
apiVersion: apps/v1
kind: Deployment
metadata:
  name: api
spec:
  replicas: 3
```

## Practical Commands
```bash
# Apply deployment
kubectl apply -f deployment.yaml

# Update image and watch rollout
kubectl set image deployment/api api=myorg/api:1.6.0
kubectl rollout status deployment/api

# Rollback if needed
kubectl rollout undo deployment/api
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
