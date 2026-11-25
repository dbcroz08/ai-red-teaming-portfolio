# Model Safety Investigation Workflow

This workflow is a portfolio demonstration, not a substitute for an employer's policies, access controls, or incident-response procedures. Follow the authorized playbook for any real case.

## 1. Intake and scope

Capture the minimum information needed to identify the report and understand the concern:

- Case ID and received time
- Reporter’s description, clearly marked as a report (not verified fact)
- Product surface, feature, and approximate event time, if known
- Potentially affected user or system scope, without unnecessary identifiers
- Immediate safety, privacy, or ongoing-harm concern
- Available artifacts and their source

Do not collect sensitive content merely because it may be interesting. Use approved access controls and storage.

## 2. Duplicate and related-case check

Search using approved case identifiers and relevant behavior signatures. Record:

- Candidate related case IDs
- Why each appears related
- Whether evidence actually overlaps
- Link, merge, or keep-separate decision and rationale

Similarity is a lead, not proof of a shared incident or root cause.

## 3. Preserve and assess evidence

Keep original artifacts in the authorized system. In a review note, identify source, collection time, and any transformations. Distinguish:

| Evidence class | Example | How to write it |
|---|---|---|
| Direct artifact | A supplied transcript or event record | “The supplied transcript shows…” |
| Reporter statement | User’s description of what occurred | “The reporter states…” |
| Corroborated fact | Independently verified across sources | Name the sources and agreement |
| Inference | Plausible interpretation | Label it as a hypothesis and state alternatives |
| Unknown | Missing log, version, or context | State what is missing and why it matters |

Do not claim that a log is complete unless its coverage is known. A transcript alone generally cannot establish internal model state, tool execution, or root cause.

## 4. Reconstruct the event

Build a concise timeline with timestamps and sources. Note gaps, time-zone assumptions, version identifiers, tool results, retries, and relevant policy or configuration context when available. Do not silently normalize conflicting records; document the conflict.

## 5. Apply labels and severity

First select a behavior label based on observed evidence. Then assess severity using the rubric below. Keep confidence separate from severity: a potentially severe report can have low confidence and still warrant escalation.

### Severity rubric (illustrative)

| Level | Suggested interpretation | Typical handling |
|---|---|---|
| S0 — No issue substantiated | Available evidence does not show the reported behavior, or it is expected behavior | Document evidence and close or request missing information |
| S1 — Limited | Low-impact, isolated behavior with no credible ongoing harm | Queue for routine review and track patterns |
| S2 — Significant | Plausible user impact, repeatability, sensitive context, or material policy concern | Prioritized investigation and reviewer/lead consultation |
| S3 — Urgent | Credible imminent or ongoing serious harm, broad exposure, or sensitive data incident | Escalate promptly through the authorized urgent channel |

This generic rubric is not a company policy. Apply the relevant organization-specific definitions where provided. Never lower urgency solely because evidence is incomplete.

### Confidence

- **High:** key facts are supported by complete, consistent primary evidence.
- **Medium:** material facts are supported, but some context is missing or sources disagree.
- **Low:** report is plausible but key evidence is absent, unverified, or indirect.

## 6. Decide disposition and escalation

Possible dispositions: close with rationale, request additional evidence, continue investigation, link to related case, or escalate. Record the decision owner, timestamp, and next action.

Escalate immediately under the authorized process when the report suggests imminent serious harm, ongoing exposure, sensitive-data disclosure, a potentially systemic issue, or uncertainty that exceeds the reviewer’s authority. These examples do not override local policy.

## 7. Write a defendable case summary

Use this order:

1. **Issue:** one sentence describing the reported or observed behavior.
2. **Evidence:** what was reviewed and what it shows.
3. **Finding:** what is substantiated, with label and severity.
4. **Uncertainty:** missing or conflicting evidence; plausible alternatives.
5. **Action:** disposition, escalation path, owner, and next step.

Prefer short, neutral statements. Avoid attributing intent, model internals, or root cause without evidence.

## 8. Quality review and closure

Before closure, verify source attribution, timeline, label rationale, privacy minimization, duplicate handling, and follow-up ownership. Record reviewer feedback and calibration disagreements. Feed recurring ambiguities into guidance updates rather than resolving them through undocumented individual judgment.

## 9. Operational metrics

Track denominators and definitions alongside counts. Suggested measures include intake volume, duplicate rate, handling time by complexity band, escalation rate, reopened cases, reviewer agreement, and evidence-completeness rate. Do not optimize speed in isolation: pair throughput measures with quality and rework measures. See [metrics/README.md](./metrics/README.md).
