# Prompt Templates: DevOps

Use these ask-based templates with [`system-prompt.md`](./system-prompt.md). Replace bracketed placeholders (`[like this]`) with your context.

---

## 1. CI/CD Pipeline & Release Workflow Design

```text
Design a CI/CD pipeline for [service / repository name].

Context:
- Source & CI platform: [e.g., GitHub Actions, Cloud Build]
- Runtime & packaging: [e.g., Python 3.12, Docker, Cloud Run, Vertex AI]
- Environments: [dev / staging / prod]
- Quality & security gates: [linting, unit/integration tests, container scan, secret scan]

Deliverables:
1. Pipeline stages and triggers (PR checks vs. main branch vs. release tags)
2. Caching, dependency pinning, and build reproducibility practices
3. Secrets and identity handling (e.g., OIDC / Workload Identity Federation)
4. Progressive deployment and automated rollback strategy
```

---

## 2. Cloud Deployment & Infrastructure Review (GCP / IaC)

```text
Review the following deployment setup or IaC configuration for [workload description]:
[paste Terraform / Dockerfile / Cloud Run / Kubernetes manifest or describe architecture]

Evaluate and recommend improvements for:
1. IAM least privilege & credential hygiene (ADC / Workload Identity / Secret Manager)
2. Network boundaries, ingress/egress controls, and data security
3. Scaling, quotas, timeouts, and resilience (multi-zone, retries, circuit breakers)
4. Cost efficiency and resource right-sizing
```

---

## 3. Observability, Alerting & SLO Specification

```text
Define an observability and reliability plan for [service or AI agent workload].

Context:
- Critical user journeys / endpoints: [list key workflows]
- External dependencies: [e.g., Gemini / Vertex AI APIs, databases, queues]
- Traffic profile & latency expectations: [RPS, p95 target, batch vs. real-time]

Deliverables:
1. Core SLIs and recommended SLO targets (availability, latency, error rate)
2. Key structured log fields, metrics, and trace spans to emit
3. Actionable alert rules (paging vs. ticket severity) with low false-positive noise
4. Dashboard layout recommendations for rapid incident triage
```

---

## 4. Incident Triage & Operational Runbook

```text
Create an operational runbook for [service / alert / failure scenario].

Context:
- Triggering symptom or alert: [describe alert condition or failure mode]
- Architecture overview: [components, cloud services, dependencies]
- Available tooling: [CLI tools, dashboards, feature flags, rollback mechanism]

Include:
1. Immediate triage & impact assessment checks
2. Diagnostic commands / log queries to isolate root cause
3. Fast mitigation & rollback procedures
4. Escalation paths and post-incident verification checklist
```
