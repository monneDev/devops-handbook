# Pods

## What It Is
A Pod is the smallest deployable unit in Kubernetes. Most workloads run one container per Pod, while sidecars add capabilities like proxies or log shipping. Pods are ephemeral and should be managed by higher-level controllers for production reliability.

## Key Concepts
- All containers in a Pod share one network namespace.
- Pod IP changes when Pod is recreated.
- Readiness and liveness probes control traffic and restarts.
- Standalone Pods are usually for testing only.

## Simple Example
```bash
apiVersion: v1
kind: Pod
metadata:
  name: demo-pod
spec:
  containers:
  - name: app
    image: busybox
```

## Practical Commands
```bash
# Create pod and watch status
kubectl apply -f pod.yaml
kubectl get pod demo-pod -w

# Debug startup issues
kubectl describe pod demo-pod
kubectl logs demo-pod
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
