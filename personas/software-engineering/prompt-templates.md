# Prompt Templates: Software Engineering

Use these ask-based templates with [`system-prompt.md`](./system-prompt.md). Replace bracketed placeholders (`[like this]`) with your context.

---

## 1. Technical Design Doc (RFC) & Implementation Plan

```text
Write a concise technical design (RFC) for [feature or system component].

Context:
- Requirements / acceptance criteria: [paste or summarize requirements]
- Tech stack & runtime: [languages, frameworks, cloud/SDKs, e.g., Python + google-genai + Pydantic]
- Non-functional targets: [latency, throughput, cost, data retention, security]
- Existing codebase constraints: [relevant modules or legacy constraints]

Deliverables:
1. High-level architecture & component responsibilities
2. Data models, schemas, and API/module interfaces
3. Error handling, retries, and edge-case strategy
4. Alternatives considered and key trade-offs
5. Phased implementation & testing plan
```

---

## 2. Code Review & Refactoring Audit

```text
Review the following [code / diff / notebook] for production readiness:
[paste code or reference file paths]

Context:
- Intended behavior: [what this change should accomplish]
- Focus areas: [e.g., correctness, typing/schemas, performance, security, readability]

Provide feedback grouped by severity (Blocker / Important / Nit), citing exact symbols or lines, explaining *why* each issue matters, and showing minimal, clean fixes.
```

---

## 3. Debugging & Root-Cause Analysis

```text
Help diagnose and fix the following issue:

Symptoms:
- Observed behavior: [error message, stack trace, or incorrect output]
- Expected behavior: [what should happen]
- Reproduction steps: [inputs, environment, frequency]
- Relevant code / logs: [snippet or file references]

Provide:
1. Most likely root cause(s) ranked by probability with evidence
2. Diagnostic checks to confirm the root cause
3. Minimal fix and any related edge cases to guard against
4. Regression test case to prevent recurrence
```

---

## 4. Test Strategy & Edge-Case Matrix

```text
Design a test plan for [module / agent / API endpoint].

Specification:
[describe inputs, outputs, external dependencies, and business rules]

Deliverables:
1. Unit test cases (happy paths, boundary values, malformed inputs, error paths)
2. Integration / contract test cases (including mocking external APIs or models)
3. Key failure-injection or regression scenarios
4. Recommended test assertions and coverage priorities
```
