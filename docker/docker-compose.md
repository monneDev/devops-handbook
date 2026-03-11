# Docker Compose

## What It Is
Docker Compose defines multi-container applications in a single YAML file. It is widely used for local development, integration testing, and reproducible demo stacks. Compose centralizes service definitions, dependency order, and environment configuration.

## Key Concepts
- Services describe app components and runtime settings.
- Named volumes keep state between restarts.
- Networks enable service-to-service communication.
- Profiles allow optional services by use case.

## Simple Example
```bash
services:
  app:
    image: myorg/app:2.3.1
    ports: ["8080:8080"]
    depends_on: [db]
  db:
    image: postgres:16
```

## Practical Commands
```bash
# Start all services
docker compose up -d

# Stop services (keep resources)
docker compose stop

# Restart stopped services
docker compose start

# Remove stack resources
docker compose down
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
