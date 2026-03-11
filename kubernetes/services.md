# Services

## What It Is
A Service provides stable networking for a dynamic set of Pods. Because Pod IPs change, Services expose consistent virtual IPs and DNS names. They are foundational for internal discovery and controlled traffic routing.

## Key Concepts
- ClusterIP is internal-only service access.
- NodePort opens access through node ports.
- LoadBalancer integrates cloud-native load balancers.
- Selectors map traffic to endpoints.

## Simple Example
```bash
apiVersion: v1
kind: Service
metadata:
  name: api-svc
spec:
  type: ClusterIP
  ports:
  - port: 80
```

## Practical Commands
```bash
# Create service
kubectl apply -f service.yaml
kubectl get svc

# Verify backend endpoints
kubectl get endpoints api-svc
kubectl describe svc api-svc
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
