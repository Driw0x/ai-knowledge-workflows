# Prompt Engineering Patterns

This repository uses prompt engineering as a software-design practice rather than as a collection of one-off instructions.

## 1. Context decomposition

A prompt should not contain every piece of user or project context.

Instead:

```text
AGENTS.md
+ domain knowledge
+ task prompt
+ output template
```

This improves reuse and reduces duplication.

## 2. Explicit evidence policy

Prompts define what counts as evidence.

Example:

```text
Do not infer competence from a technology being mentioned only once.
```

This reduces unsupported conclusions.

## 3. Positive and negative constraints

Good task prompts specify both:

- what the agent should do;
- what the agent must avoid.

Example:

```text
Preserve valid existing content.
Prefer minimal diffs.
Do not document roadmap items as implemented.
```

## 4. Output contracts

The agent is given a target structure rather than an open-ended request.

Examples include:

- project profiles;
- internship research reports;
- audit tables.

This makes outputs easier to compare, review, and version.

## 5. Tool-aware prompting

Research prompts require current-source verification.

Repository prompts require source-code inspection before trusting documentation.

The prompt therefore reflects the capabilities required for the task.

## 6. Uncertainty handling

The workflows instruct the agent to distinguish:

- verified facts;
- analysis;
- recommendations;
- missing information.

This is more reliable than forcing a definitive answer.

## 7. Minimal-diff editing

For documentation and knowledge-base maintenance, prompts explicitly favor minimal changes.

This helps preserve human-authored context and reduces accidental regressions.

## 8. Privacy-aware prompting

Reusable public prompts are separated from private local context.

The workflow can be open source while personal data remains local.

## 9. Versionability

Prompts are stored as text files and versioned with Git.

Changes can therefore be reviewed like code:

- what changed;
- why it changed;
- which workflow behavior it affects.

## 10. Evaluation-oriented design

A prompt workflow becomes stronger when its quality can be assessed.

Future improvements may include:

- benchmark tasks;
- model-to-model comparisons;
- output-consistency tests;
- rubric-based evaluation;
- regression examples.

These additions would turn the repository from a prompt library into a small prompt-engineering system with measurable behavior.
