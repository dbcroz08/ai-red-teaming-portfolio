# Data Card

## Intended Use

The data described in this repository is for understanding red-team methodologies and reviewing representative, synthetic audit records.

## Data Contents

The repository may include:

- Synthetic prompts
- Sanitized model transcripts
- Rubric labels
- Annotator decisions
- Aggregate summaries

It should not contain real credentials, personal records, confidential medical records, protected operational data, or undisclosed proprietary material.

## Collection and Provenance

A data record must identify:

- Source model or environment
- Collection date
- Prompt creator and prompt source
- Dataset split or test condition
- Sampling settings
- Whether the response was generated, edited, or simulated
- Any permitted transformations

A missing field must be marked unknown rather than inferred.

## Annotation

Each test item should include a written pass/fail rule and the reviewer’s rationale. If labels are subjective, record reviewer count and agreement.

## Known Limitations

- A small prompt set may not represent real-world deployment behavior.
- Synthetic prompts may differ from naturalistic user behavior.
- Model behavior can change by build, configuration, and system prompt.
- Averages can conceal rare but severe failures.
- LLM-generated labels may introduce automation bias.

## Privacy and Safety

Authors must remove direct identifiers and replace sensitive examples with synthetic substitutes. Redaction decisions should not remove evidence needed to understand a finding.
