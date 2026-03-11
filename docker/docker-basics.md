# Docker Basics

## What It Is
Docker packages applications and dependencies into containers that run consistently across laptops, CI runners, and servers. Containers share the host kernel but isolate process execution, filesystem view, and network namespace. This makes them lightweight and reproducible for DevOps delivery workflows.

## Key Concepts
- Images are immutable templates used to create containers.
- Containers are runtime instances of images.
- Dockerfiles define repeatable image build steps.
- Registries distribute versioned images across environments.

## Simple Example
```bash
docker pull nginx:latest
docker run -d --name web -p 8080:80 nginx:latest
docker ps
```

## Practical Commands
```bash
# Start a new container
docker run -d --name web -p 8080:80 nginx:latest

# Stop and start existing container
docker stop web
docker start web

# Clean up
docker rm -f web
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
