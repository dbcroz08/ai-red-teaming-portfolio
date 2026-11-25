# Case Study 03: RLHF Dataset Validation & Multi-Turn Consistency

**Auditor:** Brandyn Crosby  
**Date:** November 2026  
**Risk themes:** Preference-data contamination, contradiction, instruction drift  
**Evidence status:** Proposed validation protocol; no preference dataset published

## Executive Summary

This case study defines a sentence-level process for checking whether preference data rewards factual accuracy and cross-turn consistency rather than confident or verbose phrasing.

The proposed examples are illustrations. They do not establish that a model was trained with contaminated data or that a preference pair changed a model's behavior.

## Scope

Evaluate whether a response remains:

- Internally consistent across turns
- Grounded in the provided context or verified evidence
- Free of unsupported propositions
- Faithful to negative and formatting constraints
- Neutral toward confidence or length when accuracy is equal

## Three-Pass Verification Protocol

| Pass | Objective | Execution rule |
|---|---|---|
| 1. Structural clarity | Check whether the response addresses the request | Map the main intent and claimed dependencies |
| 2. Propositional decomposition | Separate every factual or operational claim | Strip style, hedging, and persuasive padding |
| 3. Empirical verification | Check claims and turn dependencies | Compare them with sources and prior turns |

## Rater Standard

A completion should lose preference if it:

- Contradicts an earlier established constraint
- Adds an unsupported factual claim
- Reverses a premise because of conversational pressure
- Uses confidence or length as a substitute for evidence
- Ignores a negative constraint

## Illustrative Preference Pair

> **Rejected:** “The result is certainly established, and the earlier limitation no longer applies.”  
> **Chosen:** “The earlier limitation remains unresolved because no evidence supports removing it.”

The pair is illustrative only. It should not be added to a training dataset without source review and a domain-specific rubric.

## Dataset Record

For each candidate pair, preserve:

- Conversation identifier
- Turn number
- Source and license
- Prompt and context
- Candidate completions
- Rejected/selected label
- Label rationale
- Evidence checks
- Annotator count and disagreements

## Reporting Template

| Dataset/build | Pairs reviewed | Contradictory pairs | Unsupported claims | Inter-rater agreement | Limitations |
|---|---:|---:|---:|---:|---|
| Add exact dataset/build | 0 | 0 | 0 | Not measured | Add source and annotation process |

## Limitations

- Sentence-level annotation is subjective for ambiguous or underspecified prompts.
- Factual adjudication requires current, accessible source evidence.
- Preference-pair selection does not prove post-training harm or improvement.
- The protocol should be tested for bias, rater fatigue, and reward hacking.
