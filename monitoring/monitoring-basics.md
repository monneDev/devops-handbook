# Monitoring Basics

## What It Is
Monitoring collects and evaluates system health signals such as latency, error rate, throughput, and saturation. Effective monitoring combines dashboards, alerting, and incident response workflows. In DevOps, this feedback loop protects reliability during fast delivery.

## Key Concepts
- Golden signals reveal user-impacting issues quickly.
- Actionable alerts should link to runbooks.
- Dashboards support incident triage and planning.
- SLOs align reliability targets with business needs.

## Simple Example
```bash
Alert when 5xx error rate > 2% for 10 minutes
```

## Practical Commands
```bash
# Conceptual Prometheus query examples
# rate(http_requests_total[5m])
# histogram_quantile(0.95, sum(rate(http_request_duration_seconds_bucket[5m])) by (le))

# Trigger test alert in Alertmanager
curl -XPOST http://alertmanager.example/api/v2/alerts
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
