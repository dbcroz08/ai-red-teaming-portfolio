# AI Red-Teaming & Safeguard Validation Portfolio

**Brandyn Crosby** — AI Red-Team Specialist & Adversarial Logic Auditor

Phoenix, AZ · Open to remote work · LLM sycophancy, misinformation, bias, and RLHF evaluation

## Overview

This portfolio documents structured adversarial evaluations of Large Language Models (LLMs). The work emphasizes:

- Multi-turn conversational pressure testing
- Conversational sycophancy and unsupported state claims
- Health-domain heuristic and stereotype analysis
- RLHF preference-data consistency checks
- Evidence-preserving, reproducible audit artifacts

> **Evidence status:** This repository documents methodologies and case-study findings. It does not claim independent scientific validation unless a model, version, sample size, rubric, and raw evidence are published alongside the result.

## Case Studies

| # | Case Study | Focus | Material in this repository |
|---|---|---|---|
| 01 | [Conversational Sycophancy & Feature-Access Hallucinations](./01-sycophancy-hallucination-audit.md) | Truthfulness under user pressure | Baseline probe, pressure progression, mitigation draft |
| 02 | [Adversarial Testing & Bias Decoupling in Health Models](./02-holistic-health-bias-audit.md) | Single-factor and stereotype bias | Multi-factor rubric, counter-example stress test |
| 03 | [RLHF Dataset Validation](./03-rlhf-dataset-validation.md) | Multi-turn consistency and dataset quality | Three-pass verification method and preference-pair template |

## Evaluation Evidence Standard

Each case study should publish, or clearly identify as missing:

- Model provider and exact model identifier
- Model version, deployment date, and sampling parameters
- Test prompt set and randomized or fixed ordering
- Number of trials and successful/failing outcomes
- Adjudication rules and disagreements
- Sanitized raw evidence, or a documented reason for withholding it
- Known limitations and likely confounders

The repository's [methodology](./METHOD.md) defines the baseline audit process. Placeholder metrics must not be interpreted as measured performance.

## Responsible Use

- Conduct evaluations only in authorized environments.
- Avoid harmful, personally identifying, or confidential data.
- Use synthetic or redacted examples when production context is sensitive.
- Do not present a portfolio finding as universal or established model behavior.
- Health findings are educational and are not medical advice or clinical validation.
- Preference pairs shown in this repository are illustrative unless accompanied by source and annotation evidence.

## Repository Structure

```text
.
├── 01-sycophancy-hallucination-audit.md
├── 02-holistic-health-bias-audit.md
├── 03-rlhf-dataset-validation.md
├── METHOD.md
├── DATA_CARD.md
├── DISCLAIMER.md
├── CONTRIBUTING.md
├── LICENSE
└── prompts/                 # Synthetic prompts and intended audit outcomes
```

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md). Contributions should preserve evidence provenance and avoid falsely attributing findings to a specific model or result set.

## License and Disclaimer

Documentation is licensed under the MIT License. See [LICENSE](./LICENSE) and [DISCLAIMER.md](./DISCLAIMER.md).
