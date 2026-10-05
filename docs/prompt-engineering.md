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

For repository work, current implementation and executable tests take
precedence over stale documentation. Documentation remains useful evidence, but
not when it contradicts observed behavior.

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

This repository includes:

- stable evaluation cases;
- a shared rubric;
- qualitative result reports;
- regression criteria for comparing prompt behavior.

The framework remains manual and lightweight. Model-to-model comparisons,
automated execution, and repeated-run consistency tests remain optional
extensions rather than v1 requirements.

## 11. Success criteria before execution

Before a substantive change, define:

- the observable result;
- behavior and files that must remain unchanged;
- the checks required before completion.

This prevents implementation from becoming the definition of success after the
fact.

## 12. Diagnose, fix, and verify

A reliable correction workflow is:

```text
reproduce or trace the failure
    ↓
identify the root cause
    ↓
apply a targeted fix
    ↓
run a regression check
    ↓
run broader relevant checks and a smoke test
```

Writing the change is only one step. A workflow should not report completion
until the relevant validation has run.

## 13. Grounded generation pipelines

When output contains claims about a person, project, or system, use an explicit
pipeline:

```text
source facts
    ↓
relevant evidence selection
    ↓
generation
    ↓
claim and output validation
```

The model may select, condense, organize, and reformulate evidence. It must not
create missing facts, metrics, experience, or results.

## 14. Human-in-the-loop boundaries

High-impact workflows should identify decisions that remain human actions.
Application workflows, for example, may discover, analyze, and prepare
materials, but the candidate reviews the final content and submits it manually.

```text
discovery
    ↓
analysis
    ↓
preparation
    ↓
human review
    ↓
manual action
    ↓
tracking
```

## 15. Reusable extraction across repository boundaries

A private source can inform a public derivative without being copied into it:

```text
private source evidence
    ↓
identify stable reusable rules
    ↓
remove personal and machine-specific context
    ↓
apply the smallest public change
    ↓
validate behavior, links, and privacy
```

The source remains authoritative. The derivative exposes only externally useful
information. Preserve unrelated local changes in both repositories and never
use the public derivative to overwrite private source facts.
