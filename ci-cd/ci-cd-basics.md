# CI CD Basics

## What It Is
CI/CD combines automated integration checks with automated delivery workflows. The goal is to move changes from commit to production safely and quickly. Strong pipelines provide fast feedback, consistent quality gates, and auditable deployments.

## Key Concepts
- CI runs build, lint, and tests on each change.
- CD promotes immutable artifacts across environments.
- Pipeline stages should be deterministic and observable.
- Rollback paths are part of release design.

## Simple Example
```bash
build -> unit-tests -> integration-tests -> deploy-staging -> deploy-prod
```

## Practical Commands
```bash
# Common pre-push checks
npm ci
npm run lint
npm test

# Build deployable artifact
npm run build
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
