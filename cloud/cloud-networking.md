# Cloud Networking

## What It Is
Cloud networking includes virtual networks, routing, DNS, firewalls, and load balancing. It is software-defined and API-driven, which enables automated and repeatable topology management. Strong network segmentation reduces blast radius and improves security.

## Key Concepts
- Subnets separate tiers and trust zones.
- Security groups/firewalls define allowed flows.
- Route tables control traffic paths.
- Load balancers distribute traffic across healthy targets.

## Simple Example
```bash
Public subnet: load balancer
Private subnet: app services
Data subnet: databases
```

## Practical Commands
```bash
# Kubernetes-based network checks
kubectl get svc
kubectl get ingress

# Verify service connectivity
kubectl exec -it deploy/api -- curl -s http://backend:8080/health
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
