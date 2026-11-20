# Prompt Templates: Product Manager

Use these ask-based templates with [`system-prompt.md`](./system-prompt.md). Replace bracketed placeholders (`[like this]`) with your context.

---

## 1. Feature PRD / One-Pager

```text
Draft a concise PRD for [feature or initiative name].

Context:
- Target users: [user segment / persona]
- Problem statement: [core user pain point or business opportunity]
- Constraints: [timeline, platform, budget, compliance, or technical limits]
- Existing product context: [current workflow or baseline]

Deliverables:
1. Executive summary & problem framing
2. Goals, non-goals, and MVP scope
3. Functional requirements & key edge cases
4. Primary success metrics and guardrail metrics
5. Rollout plan, risks, and open questions
```

---

## 2. User Stories & Acceptance Criteria

```text
Break down [epic or feature description] into vertical, independently shippable user stories.

For each story, include:
- Story statement ("As a ..., I want ..., so that ...")
- Priority (P0 / P1 / P2)
- Testable acceptance criteria in Given / When / Then format
- Key edge cases and error states
- Dependencies on UI/UX, Software Engineering, or DevOps
```

---

## 3. Prioritization & Trade-off Analysis

```text
Evaluate and prioritize the following candidate initiatives for [quarter / milestone]:
[list candidate features with brief descriptions]

Decision context:
- Primary objective: [e.g., activation, retention, reliability, revenue]
- Team capacity / constraints: [team size, deadline, dependencies]

Provide:
1. A structured scoring matrix (e.g., RICE or Impact vs. Effort with rationale)
2. Recommended execution order (Now / Next / Later)
3. Key trade-offs and what we are explicitly choosing NOT to do
```

---

## 4. Product Review of a Mockup or Visual Artifact

```text
Review the attached [mockup / screenshot / generated visual] against our product goal: [describe goal and target user].

Evaluate:
1. Value proposition & messaging clarity (score 1–10 with reasoning)
2. Alignment with user intent and core workflow (score 1–10 with reasoning)
3. Missing functional states or requirement gaps
4. Actionable revisions needed before handing off to engineering
```
