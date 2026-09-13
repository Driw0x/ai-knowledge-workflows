# Prompt Evaluation Benchmarks

This directory defines lightweight evaluation cases for the prompt workflows in this repository.

The goal is to make prompt changes reviewable and measurable instead of relying only on subjective impressions.

## Evaluation flow

```text
Prompt
  ↓
Evaluation case
  ↓
Agent / model output
  ↓
Evaluation rubric
  ↓
Evaluation report
  ↓
Comparison with previous prompt version
```

## What can be evaluated?

Examples include:

- project update prompts;
- skill evaluation prompts;
- documentation update prompts;
- career research prompts;
- knowledge-base maintenance prompts.

## Directory structure

```text
evals/
├── README.md
├── rubrics/
│   └── prompt-evaluation-rubric.md
├── templates/
│   └── evaluation-report.md
└── cases/
    ├── project-update.md
    ├── skill-evaluation.md
    └── documentation-update.md
```

## Evaluation principles

### Use representative tasks

Evaluation cases should reflect real workflow failures or recurring tasks.

Do not create artificial tests that are easier than actual usage.

### Keep evaluation inputs stable

When comparing prompt versions, use the same case whenever possible.

Changing both the prompt and the test case at the same time makes comparison less useful.

### Separate prompt quality from model capability

Record the model used for each run.

A better result from a stronger model does not necessarily prove that the prompt improved.

### Penalize unsupported claims

A fluent answer is not a good answer if it invents information.

Grounding is a core criterion.

### Prefer behavioral evaluation

Evaluate what the output actually does:

- does it follow constraints?
- does it preserve correct content?
- does it avoid unsupported claims?
- does it produce the requested structure?

## Running an evaluation

1. Choose a prompt to evaluate.
2. Choose the matching case under `evals/cases/`.
3. Run the prompt using the case inputs.
4. Score the output with `evals/rubrics/prompt-evaluation-rubric.md`.
5. Record the result with `evals/templates/evaluation-report.md`.
6. Compare the result with previous versions when available.

## Comparing prompt versions

A prompt change should ideally improve one or more dimensions without causing a regression elsewhere.

Examples:

```text
Prompt v1
vs
Prompt v2
```

or:

```text
with AGENTS.md
vs
without AGENTS.md
```

or:

```text
Model A
vs
Model B
```

## Regression

A regression occurs when a new prompt version performs materially worse on an existing evaluation case.

Examples:

- introduces unsupported claims;
- ignores a previously respected constraint;
- rewrites files unnecessarily;
- loses required output structure;
- misses important evidence.

## Current benchmark scope

The initial benchmark set focuses on:

- project updates;
- skill evaluation;
- documentation updates.

Future benchmark cases can cover:

- internship research;
- knowledge extraction;
- portfolio synchronization;
- cross-project competency analysis.

## Future automation

The initial framework is intentionally manual and lightweight.

Possible future additions:

```text
evals/
├── scripts/
├── results/
└── datasets/
```

Automation should be added only after the evaluation criteria and cases prove useful in repeated manual runs.
