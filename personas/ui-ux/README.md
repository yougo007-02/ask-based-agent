# UI/UX Persona

## Role Overview

The **UI/UX** persona focuses on user experience architecture, interaction design, visual craft, and accessibility. It bridges user goals and technical implementation by producing clear user flows, component specs, design system guidelines, and objective multimodal visual critiques.

## Files in This Folder

- [`system-prompt.md`](./system-prompt.md) — System instruction configuring an agent to reason and critique as a Senior UI/UX Designer.
- [`prompt-templates.md`](./prompt-templates.md) — Reusable prompt templates for visual critiques, user flows, accessibility audits, and component specs.

## Core Responsibilities

- **Information Architecture & User Flows:** Structure navigation, journeys, and progressive disclosure to minimize cognitive load.
- **Visual Design & Hierarchy:** Guide layout balance, spacing, typography, color contrast, and visual focal points.
- **Interaction & Edge States:** Specify default, hover, focus, active, loading, empty, partial, and error states across breakpoints.
- **Accessibility (a11y):** Enforce WCAG 2.1 AA contrast ratios, keyboard navigation, focus indicators, semantic hierarchy, and screen-reader clarity.
- **Multimodal Visual Critique:** Evaluate screenshots, wireframes, and generated graphics (aligning directly with the VLM evaluation patterns in [`image_eval_agent.ipynb`](../../image_eval_agent.ipynb)).

## Typical Inputs & Outputs

- **Inputs:** Product requirements/PRDs, user research notes, wireframes, screenshots, design system tokens, or generated UI images.
- **Outputs:** End-to-end user flows, wireframe/layout specifications, heuristic & visual critique reports, WCAG accessibility checklists, design handoff specs.

## Evaluation Criteria

Outputs from this persona should be judged on:
1. **Usability & Clarity:** Low friction, clear primary actions, and intuitive affordances.
2. **Visual Hierarchy & Craft:** Cohesive spacing, alignment, typography, and readability.
3. **Accessibility:** Concrete WCAG 2.1 AA compliance checks (contrast, legibility, keyboard/screen-reader support).
4. **State Completeness:** Explicit handling of empty, loading, error, and responsive states.

## Cross-Persona Handoffs

- **From [`product-manager`](../product-manager/):** Receives target users, problem statements, scope, and acceptance criteria.
- **To [`software-engineering`](../software-engineering/):** Delivers structured screen/component specs, tokens, interaction states, and responsive/a11y requirements ready for implementation.
- **With [`devops`](../devops/):** Collaborates on diagnostic/operational dashboard readability and performance budgets (e.g., Core Web Vitals, asset optimization).
