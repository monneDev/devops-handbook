# Configuration Management

## What It Is
Configuration management keeps server and platform settings consistent over time. Tools such as Ansible apply declarative, idempotent changes across many hosts. This reduces drift and supports reliable patching and operational standards.

## Key Concepts
- Idempotency avoids repeated side effects.
- Inventories define target hosts and groups.
- Templating supports environment-specific values.
- Secrets should be externalized and encrypted.

## Simple Example
```bash
- hosts: web
  tasks:
    - name: Ensure Nginx is installed
      apt:
        name: nginx
        state: present
```

## Practical Commands
```bash
# Dry-run changes
ansible-playbook -i inventory.ini site.yml --check

# Apply and validate
ansible-playbook -i inventory.ini site.yml
ansible web -i inventory.ini -m ping
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
