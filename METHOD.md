# Audit Methodology

## Purpose and evidence discipline

This method is for structured portfolio exercises and authorized evaluations. It does not replace an organization's investigation playbook or establish that a finding generalizes to other models or deployments.

## 1. Define scope

Record the model/provider/build if known, evaluation date, configuration, tools or retrieval enabled, test scope, expected behavior, and stop/escalation conditions. Mark unknown fields explicitly; do not infer them from output alone.

## 2. Separate investigation from experiment

An **incident investigation** reconstructs a reported event using available records. A **behavioral evaluation** tests a defined prompt set under controlled conditions. These are different activities: a synthetic prompt exercise is not an incident, and a single report is not a benchmark.

## 3. Build a test or evidence matrix

For evaluations, define prompt ID, category, expected behavior, constraints, trial count, and run order. For investigations, capture report, source artifact, timestamps, coverage, conflicts, and missing evidence. Keep exploratory cases separate from fixed test cases.

## 4. Preserve provenance

Preserve original artifacts only in authorized systems. Record source, collection time, access restrictions, transformations, and known incompleteness. Sanitize only for public examples and label any synthetic or edited content conspicuously.

## 5. Assess observations and uncertainty

Use separate fields for:

- **Observed:** directly present in a reviewed artifact.
- **Reported:** stated by a reporter but not independently verified.
- **Corroborated:** supported by independent sources.
- **Inference:** an interpretation with alternatives noted.
- **Unknown:** necessary information not available.

Do not treat model statements as proof that an external action occurred. A transcript alone does not generally establish system state, tool execution, or root cause.

## 6. Apply labels and severity consistently

Use the applicable policy taxonomy. Record label definition, evidence for and against, confidence, severity rationale, and escalation/disposition. Keep confidence distinct from severity. If no approved taxonomy is available, mark a label as provisional and do not present it as organizational policy.

## 7. Review and calibrate

When practical, reviewers independently label the same cases, discuss disagreements using documented definitions, and record adjudication. Track ambiguous guidance and update examples. Do not let reviewer consensus substitute for source evidence.

## 8. Report metrics responsibly

For any rate, publish numerator, denominator, time window, exclusions, case mix, and definition. For experiments, report model/build, settings, prompt set, trial count, missing runs, and limitations. Do not fabricate numbers or imply a benchmark without underlying data.

## 9. Privacy and safety

Use approved environments and access controls. Minimize personal and sensitive information. Public artifacts must be synthetic or appropriately de-identified and must not expose credentials, private records, or operationally sensitive details.

## 10. Reproduction

A published evaluation should include a sanitized prompt set, run configuration, transcripts where permitted, rubric, and summary procedure. An investigation case should include enough source provenance to audit the reasoning while retaining sensitive originals only in authorized storage.
