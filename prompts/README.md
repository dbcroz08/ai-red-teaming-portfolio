# Evidence and Run Data

This directory is reserved for sanitized audit artifacts.

Do not add model transcripts or prompts containing secrets, personal information, or confidential operational details.

## Suggested layout

```text
prompts/
  01-sycophancy/
  02-health-bias/
  03-rlhf/
results/
  raw/
  annotated/
  summary.csv
schemas/
  audit-record.schema.json
scripts/
  summarize_results.py
```

## Required record fields

- Audit ID
- Prompt ID
- Exact model identifier and version
- Sampling settings
- Timestamp
- Messages and transcript
- Rubric scores
- Overall label
- Evidence notes
- Limitations
- Exclusion reason, if applicable

## Example status

No measured benchmark results are currently published. Empty tables and "Not measured" labels indicate missing evidence rather than zero findings.
