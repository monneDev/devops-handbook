# Ingress

## What It Is
Ingress defines HTTP and HTTPS routing rules to services inside Kubernetes. It requires an Ingress Controller to enforce routes, TLS, and edge behavior. Teams use Ingress to centralize external access policy and domain-based routing.

## Key Concepts
- Host and path rules route traffic to services.
- TLS secrets terminate HTTPS traffic.
- Controller-specific annotations tune behavior.
- Ingress is typically environment entry point.

## Simple Example
```bash
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: app-ingress
spec:
  rules:
  - host: app.example.com
```

## Practical Commands
```bash
# Apply ingress and inspect
kubectl apply -f ingress.yaml
kubectl get ingress
kubectl describe ingress app-ingress

# Test host routing
curl -H "Host: app.example.com" http://<ingress-ip>/
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
