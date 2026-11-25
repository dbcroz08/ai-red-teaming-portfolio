# Model Safety Investigation Portfolio

**Brandyn Crosby** · Phoenix, AZ · Open to remote work

A practical portfolio focused on investigating unexpected AI model behavior: preserving evidence, reconstructing events from incomplete records, applying consistent labels, documenting uncertainty, and identifying when to escalate.

> **Important evidence note:** The included investigation exercise is explicitly synthetic. It demonstrates a workflow, not an actual incident, production-model evaluation, or claim about any provider. No measured model-safety benchmark is published here.

## Investigation capabilities demonstrated

- **Intake and triage:** identify the reported behavior, scope, urgency, evidence gaps, and possible duplicate signals.
- **Evidence reconstruction:** build a time-ordered account from available records while separating direct observations from assertions and inference.
- **Consistent review:** apply a defined severity and disposition rubric, recording rationale and uncertainty.
- **Case writing:** produce concise summaries that state what happened, what remains unknown, and the next action.
- **Escalation judgment:** define concrete triggers for urgent or specialist review.
- **Quality improvement:** use calibration questions and structured review fields to surface ambiguous guidance and recurring patterns.
- **Privacy-aware handling:** minimize sensitive content and use synthetic examples in this public portfolio.

## Start here

1. [Investigation workflow](./INVESTIGATION_WORKFLOW.md) — intake through closure and escalation.
2. [Synthetic case file](./examples/synthetic-case-001.md) — worked evidence review and decision rationale.
3. [Case record template](./templates/case-record.md) — reusable structured investigation form.
4. [Calibration exercise](./CALIBRATION.md) — short labeling exercise with answer key.
5. [Original case studies](#case-studies) — focused evaluations of conversational truthfulness, health-domain reasoning, and preference-data consistency.

## Case studies

| Study | Focus | Evidence status |
|---|---|---|
| [01 · Unsupported state claims](./01-sycophancy-hallucination-audit.md) | Truthfulness under user pressure | Methodology and illustrative progression; not a measured benchmark |
| [02 · Health-domain bias](./02-holistic-health-bias-audit.md) | Single-factor reasoning and uncertainty | Educational review protocol; not clinical validation |
| [03 · Preference-data validation](./03-rlhf-dataset-validation.md) | Cross-turn consistency and annotation quality | Proposed protocol; no preference dataset published |

## How to read this portfolio

The synthetic investigation shows the form and reasoning discipline I would use; it does not establish real-world model behavior. The case studies are hypotheses and evaluation plans unless backed by preserved, attributable run evidence. Every unknown is intentionally labeled unknown rather than filled with assumptions. See [Evidence standards](./METHOD.md), the [Data Card](./DATA_CARD.md), and [Disclaimer](./DISCLAIMER.md).

## Responsible review

- Use only authorized systems and approved tools.
- Preserve source records and access controls; publish only sanitized or synthetic examples.
- Distinguish reported content, verified evidence, inference, and unresolved questions.
- Do not infer root cause from a transcript alone.
- Follow applicable escalation procedures for urgent safety issues.
- Health-related content is not medical advice or clinical validation.

## Repository map

```text
.
├── INVESTIGATION_WORKFLOW.md
├── CALIBRATION.md
├── templates/case-record.md
├── examples/synthetic-case-001.md
├── metrics/README.md
├── METHOD.md
├── DATA_CARD.md
├── DISCLAIMER.md
└── 01–03 case studies
```

Documentation is licensed under the MIT License. See [LICENSE](./LICENSE) and [Contributing](./CONTRIBUTING.md).
