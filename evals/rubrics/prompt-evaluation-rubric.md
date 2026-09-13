# Prompt Evaluation Rubric

Use this rubric to evaluate outputs produced by repository workflows.

Each criterion is scored from **1 to 5**.

## 1. Grounding

Measures whether claims are supported by the provided evidence.

### Score

- **5** — all important claims are grounded in available evidence
- **4** — mostly grounded, with only minor unsupported interpretation
- **3** — some unsupported or weakly grounded claims
- **2** — several important claims lack evidence
- **1** — output relies heavily on invented or unsupported information

## 2. Instruction following

Measures compliance with explicit task constraints.

Examples:

- read required files;
- preserve existing content;
- avoid unrelated modifications;
- use requested classifications;
- respect privacy rules.

### Score

- **5** — follows all important instructions
- **4** — one minor instruction missed
- **3** — partially follows instructions
- **2** — misses several important constraints
- **1** — largely ignores the task instructions

## 3. Output structure

Measures whether the output respects the requested format.

### Score

- **5** — complete and correctly structured
- **4** — structure is correct with minor omissions
- **3** — recognizable structure but inconsistent
- **2** — major requested sections are missing
- **1** — output does not follow the requested structure

## 4. Unsupported claims

Measures hallucination avoidance.

A higher score means fewer unsupported claims.

### Score

- **5** — no unsupported claims
- **4** — one minor unsupported statement
- **3** — several weak assumptions
- **2** — important unsupported claims
- **1** — substantial hallucination or fabrication

## 5. Minimal-diff behavior

Measures whether the workflow preserves valid existing content when editing tasks require minimal changes.

### Score

- **5** — only necessary changes are made
- **4** — small unnecessary edits, no important loss
- **3** — noticeable unnecessary rewriting
- **2** — large rewrite despite limited requested changes
- **1** — destructive or inappropriate rewrite

For non-editing tasks, mark this criterion as **N/A**.

## 6. Completeness

Measures whether the response covers all important parts of the task.

### Score

- **5** — all important requirements addressed
- **4** — one minor omission
- **3** — useful but incomplete
- **2** — several important omissions
- **1** — major parts of the task are absent

## Scoring

Maximum standard score:

```text
30
```

If `Minimal-diff behavior` is not applicable, calculate the result out of:

```text
25
```

## Interpretation

For a 30-point evaluation:

- **27–30** — excellent
- **23–26** — strong
- **18–22** — acceptable but should be improved
- **12–17** — weak
- **6–11** — failed evaluation

Do not rely only on the total score.

A critical grounding or hallucination failure may invalidate an otherwise high-scoring result.

## Regression rule

A new prompt version should be reviewed if:

- total score decreases materially;
- grounding decreases;
- unsupported claims increase;
- an explicit constraint previously respected is now ignored;
- minimal-diff behavior becomes worse.

Critical regressions should block the new prompt version until reviewed.
