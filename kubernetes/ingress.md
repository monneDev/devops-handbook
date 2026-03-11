# Ingress

## What It Is
Ingress is a foundational DevOps concept used in day-to-day platform and delivery workflows. Kubernetes topics focus on orchestrating containerized workloads with declarative configuration, self-healing controllers, and scalable operations. For this topic specifically, teams should focus on clear standards, repeatable execution, and practical operational feedback loops. Treat this as a building block that connects code changes, runtime behavior, and production reliability.

## Key Concepts
- Define desired state using manifests.
- Use health probes to protect availability.
- Set resource requests and limits.
- Use namespaces and RBAC for isolation.

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
# Apply ingress rule and inspect
kubectl apply -f ingress.yaml
kubectl get ingress
kubectl describe ingress app-ingress

# Validate DNS + host routing locally
curl -H "Host: app.example.com" http://<ingress-ip>/
```

## Why It Matters in DevOps
This topic matters because DevOps is about reliable software delivery, not just tooling. Strong practices in ingress create consistent environments, faster troubleshooting, and safer changes across the release lifecycle.
- Reduces deployment risk through predictable operational patterns.
- Improves collaboration between development and operations teams.
- Increases delivery speed while maintaining service reliability.

## Common Pitfalls
- Treating tooling as a one-time setup instead of a maintained capability.
- Skipping documentation for conventions and operational decisions.
- Ignoring observability and rollback planning during implementation.

## Quick Checklist
- Define naming standards and ownership for this area.
- Automate checks in CI where possible.
- Review outcomes regularly and refine based on incidents.
