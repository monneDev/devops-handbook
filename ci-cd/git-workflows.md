# Git Workflows

## What It Is
Git workflows define branching, review, and merge practices for teams. A good workflow minimizes integration friction and preserves release traceability. Common approaches include trunk-based development and release branch models.

## Key Concepts
- Short-lived feature branches reduce merge conflicts.
- Protected main branch enforces review and checks.
- Commit message conventions improve history quality.
- Frequent sync with main lowers integration risk.

## Simple Example
```bash
git checkout -b feature/add-metrics
git commit -m "feat: add metrics endpoint"
git push origin feature/add-metrics
```

## Practical Commands
```bash
# Create branch from latest main
git checkout main
git pull origin main
git checkout -b feature/improve-logging

# Rebase before PR
git fetch origin
git rebase origin/main
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
