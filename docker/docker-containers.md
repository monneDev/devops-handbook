# Docker Containers

## What It Is
A Docker container is a running process created from an image. Containers are designed to be replaceable and short-lived, which supports immutable infrastructure patterns. DevOps teams rely on container lifecycle commands for controlled deployments, troubleshooting, and rapid recovery.

## Key Concepts
- Containers should remain stateless when possible.
- Volumes persist data beyond container lifecycle.
- Resource limits prevent host contention.
- Logs and health checks improve operability.

## Simple Example
```bash
docker run -d --name api -p 5000:5000 myorg/api:1.0.0
docker logs -f api
docker stop api
```

## Practical Commands
```bash
# Create and start
docker run -d --name api -p 5000:5000 myorg/api:1.0.0

# Stop and start later
docker stop api
docker start api

# Inspect status and logs
docker ps -a
docker logs --tail 50 api
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
