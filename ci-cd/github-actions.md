# GitHub Actions

## What It Is
GitHub Actions is a workflow automation system integrated directly into GitHub repositories. It runs jobs on events like pushes, pull requests, tags, and schedules. It is commonly used for tests, security scans, image builds, and deployments.

## Key Concepts
- Workflows are YAML files in .github/workflows.
- Jobs run on hosted or self-hosted runners.
- Reusable actions reduce repeated pipeline logic.
- Secrets and environments protect sensitive data.

## Simple Example
```bash
name: ci
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm test
```

## Practical Commands
```bash
# Add workflow and push
git add .github/workflows/ci.yml
git commit -m "ci: add test workflow"
git push origin feature/ci-workflow

# Optional run inspection
gh run list --limit 5
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
