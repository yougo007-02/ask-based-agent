# Agent Personas

This directory organizes role-specific agent personas for the `ask-based-agent` repository. Each persona provides standardized role documentation, a ready-to-use system instruction (`system-prompt.md`), and reusable ask-based prompt templates (`prompt-templates.md`).

## Available Personas

| Persona | Folder | Primary Focus |
| :--- | :--- | :--- |
| **Product Manager** | [`product-manager/`](./product-manager/) | Problem framing, PRDs, prioritization, acceptance criteria, and KPIs |
| **UI/UX** | [`ui-ux/`](./ui-ux/) | User flows, visual hierarchy, accessibility (WCAG), design systems, and multimodal UI critique |
| **Software Engineering** | [`software-engineering/`](./software-engineering/) | Architecture (RFCs), schemas & APIs, implementation, code reviews, and testing |
| **DevOps** | [`devops/`](./devops/) | CI/CD, IaC, cloud/GCP operations, IAM security, observability, and incident response |

## Folder Structure

Every persona subfolder follows the same layout:

```text
personas/<persona-name>/
├── README.md            # Role scope, inputs/outputs, evaluation criteria, and handoffs
├── system-prompt.md     # System instruction for LLM/agent configuration
└── prompt-templates.md  # Reusable ask-based prompt templates for common tasks
```

## Collaboration Workflow

```text
Product Manager (What & Why)
        │
        ▼
UI/UX (Experience & Interface)
        │
        ▼
Software Engineering (Architecture & Code)
        │
        ▼
DevOps (Delivery, Security & Reliability)
        │
        └──── Telemetry & User Feedback ────► Product Manager
```

## Using a Persona with `google-genai`

You can load any persona's `system-prompt.md` directly as a `system_instruction` when invoking Gemini models (matching the pattern used in [`image_eval_agent.ipynb`](../image_eval_agent.ipynb)):

```python
from pathlib import Path
from google import genai
from google.genai import types

persona_prompt = Path("personas/ui-ux/system-prompt.md").read_text(encoding="utf-8")

client = genai.Client(enterprise=True)
response = client.models.generate_content(
    model="gemini-3.5-flash",
    contents="Review our checkout screen layout for visual hierarchy and contrast issues.",
    config=types.GenerateContentConfig(
        system_instruction=persona_prompt,
        temperature=0.2,
    ),
)
print(response.text)
```
