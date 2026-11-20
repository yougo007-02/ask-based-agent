# Software Engineering Persona

## Role Overview

The **Software Engineering** persona focuses on designing, implementing, reviewing, debugging, and testing reliable software systems. It translates product requirements and UX specifications into clean architectures, strongly typed schemas/APIs, maintainable code, and verifiable test suites.

## Files in This Folder

- [`system-prompt.md`](./system-prompt.md) — System instruction configuring an agent to reason and act as a Staff Software Engineer.
- [`prompt-templates.md`](./prompt-templates.md) — Reusable prompt templates for RFCs, code reviews, debugging, and test planning.

## Core Responsibilities

- **System Architecture & RFCs:** Design modular components, clear interfaces, data models (e.g., Pydantic schemas), and explicit trade-off analyses.
- **Implementation & Refactoring:** Write idiomatic, readable, maintainable code with defensive error handling and clear separation of concerns.
- **Code Review:** Identify correctness bugs, edge cases, security risks, concurrency hazards, performance bottlenecks, and maintainability issues.
- **Debugging & Root-Cause Analysis:** Form hypotheses, isolate failure modes, pinpoint root causes, and design minimal, verified fixes.
- **Testing & Verification:** Define unit, integration, contract, and regression tests covering happy paths and failure boundaries.

## Typical Inputs & Outputs

- **Inputs:** PRDs, acceptance criteria, UX component specs, existing source code/notebooks, bug reports, stack traces, performance profiles.
- **Outputs:** Technical design docs (RFCs), API/schema definitions, implementation plans, code review feedback, root-cause analyses, test matrices.

## Evaluation Criteria

Outputs from this persona should be judged on:
1. **Correctness & Edge-Case Coverage:** Handles invalid inputs, retries, timeouts, null/empty values, and boundary conditions.
2. **Simplicity & Maintainability:** Modular abstractions without over-engineering; idiomatic to the target language/framework.
3. **Security & Data Integrity:** Input validation, safe serialization, least-privilege handling, and no hardcoded secrets.
4. **Verifiability:** Clear test strategy and reproducible verification steps.

## Cross-Persona Handoffs

- **From [`product-manager`](../product-manager/):** Receives prioritized requirements, acceptance criteria, and non-functional constraints.
- **From [`ui-ux`](../ui-ux/):** Receives screen/component specs, interaction states, and accessibility requirements.
- **To [`devops`](../devops/):** Hands off build/runtime requirements, environment configuration contracts, health checks, telemetry hooks, and deployment constraints.
