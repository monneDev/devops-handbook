# Observability

## What It Is
Observability is the capability to understand internal system behavior through metrics, logs, and traces. It extends monitoring by supporting investigation of unknown or emergent failures. In DevOps, observability is key for operating complex microservice systems.

## Key Concepts
- Metrics show trend and capacity behavior.
- Logs provide event-level execution context.
- Traces reveal request paths across services.
- Correlation IDs connect telemetry signals.

## Simple Example
```bash
Application -> OpenTelemetry SDK -> Collector -> Backend
```

## Practical Commands
```bash
# Query recent traces (example Jaeger API)
curl "http://jaeger.example/api/traces?service=payments-api&limit=5"

# Correlate trace id in logs
grep "abc123" app.log
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
