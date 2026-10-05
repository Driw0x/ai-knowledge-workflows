# Evaluation Result — Application Preparation

## Configuration

- **Date:** 2026-10-06
- **Case:** `evals/cases/application-preparation.md`
- **Workflows:** `prompts/application/prepare-application.md` and `prompts/application/adapt-resume.md`
- **Rubric:** `evals/rubrics/prompt-evaluation-rubric.md`
- **Method:** manual walkthrough against the fixed synthetic case
- **Model:** not applicable; no model run is claimed

## Rubric results

| Criterion | Result | Observation |
|---|---|---|
| Grounding | Pass | Forecasting, evaluation, and API claims map directly to supplied project evidence. |
| Instruction following | Pass | Unsupported requirements remain gaps and submission stays manual. |
| Output structure | Pass | The workflows request requirement mapping, resume decision, review items, and next actions. |
| Unsupported claims | Pass | Kubernetes, deployment, production operations, and public speaking are not added. |
| Minimal-diff behavior | Pass | Resume A is reused or narrowly adapted; a new resume requires a material reason. |
| Completeness | Pass | Required and preferred qualifications, evidence, gaps, resume choice, and human review are covered. |

## Observed result

Applying the workflows selects Resume A as the closest evidence-based base.
Project Alpha supports forecasting and evaluation. Project Beta supports a
tested API, not deployment. Kubernetes and production operations remain not
documented. The candidate reviews all wording and submits manually.

## Gaps and limitations

- This is a deterministic manual walkthrough, not a measured model benchmark.
- It does not test document rendering or a complex resume portfolio.
- No repeated runs or model comparison were performed.

## Conclusion

The workflows pass this qualitative case. They preserve grounding, minimal
resume change, explicit gaps, and human control without claiming measured model
performance.
