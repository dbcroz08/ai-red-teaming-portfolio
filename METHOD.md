# Audit Methodology

## Purpose

This methodology is intended to make adversarial testing understandable, repeatable, and suitable for review. It does not guarantee that any result generalizes across models, prompts, or deployments.

## 1. Pre-register the Scope

For every evaluation record:

- Name the model provider and exact model/build identifier.
- Record the evaluation date and model configuration.
- Record temperature, top-p, maximum tokens, and other relevant sampling settings.
- Separate system, developer, and user messages.
- Define whether tool access or retrieval is enabled.
- Identify the threat, protected domain, and stop conditions.

## 2. Create a Test Matrix

Use a fixed set of probes plus a clearly identified exploratory set. Record:

- Prompt identifier
- Prompt category
- Desired behavior
- Allowed sources or context
- Negative constraints
- Number of trials
- Randomization or run order

## 3. Capture Evidence

Preserve an audit record containing:

```json
{
  "audit_id": "A-001",
  "prompt_id": "P-001",
  "model": "provider/model-name",
  "model_version": "exact-build-if-known",
  "timestamp": "2026-11-25T00:00:00Z",
  "sampling": {},
  "messages": [],
  "response": "",
  "rubric_scores": {},
  "overall_label": "pass|fail|needs_review",
  "evidence_notes": "",
  "limitations": ""
}
```

Sanitize user-specific identifiers and sensitive operational details before publication.

## 4. Apply the Rubric

A finding requires a label, supporting evidence, and a documented rule. Typical labels are:

- **Pass:** Response follows the defined rule.
- **Fail:** Response violates a clearly stated rule.
- **Needs review:** Evidence is ambiguous or adjudication is required.

Do not convert exploratory observations into measured rates without a sufficient fixed test set and complete recording of attempts.

## 5. Independent Review

When practical:

1. Two reviewers label each response independently.
2. Reviewers discuss disagreements against the written rubric.
3. The final label and reviewer status are recorded.
4. Any disputed case remains labeled `needs_review` in aggregate summaries.

## 6. Report Results

A measured result should report:

- Numerator and denominator
- Baseline and adversarial conditions
- Absolute difference and, when appropriate, confidence interval
- Model and configuration
- Missing or excluded cases
- Limitations and possible confounders

No numeric result should be fabricated or treated as a benchmark until the underlying run data exists.

## 7. Reproduction

Published prompts and scripts should be runnable without access to private credentials. Where proprietary APIs are used, document the service and model version, and preserve a sanitized local transcript where permitted.
