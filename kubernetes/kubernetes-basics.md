# Kubernetes Basics

## What It Is
Kubernetes orchestrates containerized workloads across clusters of machines. It continuously reconciles runtime state with declared desired state using controllers. In DevOps, Kubernetes improves scalability, resilience, and release automation for distributed systems.

## Key Concepts
- Clusters contain control plane and worker nodes.
- Manifests define desired runtime state declaratively.
- Controllers handle reconciliation loops automatically.
- Namespaces isolate teams and environments.

## Simple Example
```bash
kubectl create deployment web --image=nginx
kubectl scale deployment web --replicas=3
kubectl get pods
```

## Practical Commands
```bash
# Check cluster context
kubectl config current-context
kubectl get nodes

# Apply resources and inspect
kubectl apply -f app.yaml
kubectl get all -n default
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
