# Prompt Templates: UI/UX

Use these ask-based templates with [`system-prompt.md`](./system-prompt.md). Replace bracketed placeholders (`[like this]`) with your context.

---

## 1. Multimodal UI / Screenshot Design Critique

```text
Evaluate the attached [screenshot / wireframe / generated layout] for [target user and primary task].

Score each dimension from 1 to 10 with specific visual evidence and actionable fixes:
1. Visual Hierarchy & Layout Composition
2. Typography, Text Legibility & OCR Accuracy
3. Visual Contrast & WCAG 2.1 AA Accessibility
4. Usability, Affordances & Cognitive Load
5. Consistency & Aesthetic Craft

Conclude with the top 3 highest-impact changes to make in the next iteration.
```

---

## 2. User Flow & Screen Specification

```text
Design the end-to-end user flow and screen specifications for [feature or workflow].

Context:
- Primary user goal: [what the user is trying to accomplish]
- Entry points: [where the user starts]
- Platform / breakpoints: [web desktop, mobile web, iOS/Android]
- Constraints: [design system, data latency, or policy rules]

Deliverables:
1. Step-by-step user flow (happy path + key branches/recovery paths)
2. Screen-by-screen layout hierarchy and content structure
3. Interaction states (default, loading, empty, error, success)
4. Microcopy recommendations for labels, CTAs, and error messages
```

---

## 3. Accessibility (WCAG 2.1 AA) Audit

```text
Perform a WCAG 2.1 AA accessibility review of [screen / component / attached image].

Check and report findings across:
- Color contrast and non-color-only status indicators
- Text sizing, line length, and readability
- Keyboard navigation order and visible focus states
- Semantic structure, ARIA roles/labels, and screen-reader announcements
- Target sizes and responsive zoom/reflow behavior

For each issue found, provide severity (Critical / Major / Minor) and a concrete remediation.
```

---

## 4. Design System Component Specification

```text
Write an engineering-ready specification for a reusable [component name] component.

Include:
1. Purpose and when to use / not use
2. Anatomy and variants (sizes, emphasis levels, orientations)
3. Interactive states (default, hover, focus, active, disabled, loading, error)
4. Spacing, typography, and color token mappings
5. Accessibility & keyboard interaction requirements
```
