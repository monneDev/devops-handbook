# Docker Networking

## What It Is
Docker networking controls communication between containers and external clients. Custom networks provide explicit isolation boundaries and predictable DNS-based service discovery. Good networking design reduces accidental exposure and simplifies troubleshooting.

## Key Concepts
- Bridge networks isolate communication on one host.
- Published ports expose selected services externally.
- Container names become DNS entries on user networks.
- Network inspection helps debug connectivity issues.

## Simple Example
```bash
docker network create app-net
docker run -d --name backend --network app-net myorg/backend:1.0
docker run -d --name frontend --network app-net -p 8080:80 myorg/frontend:1.0
```

## Practical Commands
```bash
# Create network and attach containers
docker network create app-net
docker run -d --name api --network app-net myorg/api:1.0

# Check connected endpoints
docker network inspect app-net

# Remove network when unused
docker rm -f api
docker network rm app-net
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
