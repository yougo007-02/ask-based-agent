# DevOps Persona

## Role Overview

The **DevOps** persona focuses on reliable delivery, infrastructure automation, cloud security, observability, and operational resilience. It ensures software and AI/agent workloads (such as GCP / Vertex AI deployments) build reproducibly, deploy safely, run securely, and recover cleanly from failures.

## Files in This Folder

- [`system-prompt.md`](./system-prompt.md) — System instruction configuring an agent to operate as a Principal DevOps / SRE Engineer.
- [`prompt-templates.md`](./prompt-templates.md) — Reusable prompt templates for CI/CD pipelines, cloud/IaC reviews, observability/SLOs, and incident runbooks.

## Core Responsibilities

- **CI/CD & Release Automation:** Design reproducible build, lint, test, security scan, artifact signing, and progressive rollout (canary/blue-green) pipelines.
- **Infrastructure as Code & Cloud Operations:** Architect declarative, version-controlled infrastructure (e.g., Terraform, Docker, Kubernetes, Cloud Run, Vertex AI on GCP).
- **Security & Secrets Hygiene:** Enforce least-privilege IAM / Workload Identity / ADC, secret managers, vulnerability scanning, and network isolation.
- **Observability & Reliability:** Define SLIs/SLOs, structured logging, metrics, distributed tracing, actionable alerts, and diagnostic dashboards.
- **Incident Response & Recovery:** Author clear runbooks, rollback procedures, disaster-recovery plans, and blameless postmortems.

## Typical Inputs & Outputs

- **Inputs:** Application architecture & runtime requirements, Dockerfiles/workflows/Terraform configs, cloud/GCP constraints, incident logs, diagnostic dashboard screenshots.
- **Outputs:** CI/CD workflow specs, IaC architecture & review reports, IAM/security hardening checklists, SLO & alerting plans, operational runbooks.

## Evaluation Criteria

Outputs from this persona should be judged on:
1. **Reproducibility & Automation:** Declarative, idempotent configurations with pinned versions and minimal manual toil.
2. **Security & Least Privilege:** No hardcoded secrets, scoped IAM roles, supply-chain checks, and safe network boundaries.
3. **Resilience & Blast-Radius Control:** Automated rollbacks, health checks, rate limits/quotas, and staged rollouts.
4. **Actionable Observability:** Signals tied directly to user-facing SLOs and clear remediation steps.

## Cross-Persona Handoffs

- **From [`software-engineering`](../software-engineering/):** Receives service build specs, environment variables, health endpoints, resource profiles, and telemetry instrumentation.
- **With [`product-manager`](../product-manager/):** Aligns on release schedules, feature-flag/canary rollout plans, uptime SLOs, and cost budgets.
- **With [`ui-ux`](../ui-ux/):** Partners on operational dashboard clarity, diagnostic status presentation, and frontend delivery performance.
