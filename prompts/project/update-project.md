# Update Project Prompt

Inspect the current project repository and compare it with the existing knowledge-base entry.

## Objective

Update only information that has materially changed.

Before editing, define the expected update, what valid content must remain, and
the checks needed to verify the result.

Review:

- project status;
- milestones;
- implemented features;
- architecture or methods;
- technologies;
- demonstrated skills;
- benchmark or evaluation results;
- limitations;
- abandoned approaches;
- next steps.

## Rules

- Preserve existing valid information.
- Prefer minimal diffs.
- Prefer additions over unnecessary rewrites.
- Remove or correct claims that are no longer true.
- Do not document roadmap items as implemented.
- Do not infer skills or technologies.
- Use repository evidence as the primary source.
- Inspect the current branch and `HEAD`. Distinguish current implementation from remote state, normal Git history, and abandoned local or checkpoint work when relevant.
- Treat tests and benchmarks as evidence only within their actual scope. State whether results were reproduced during the update or only documented.
- Distinguish implemented, tested, validated, experimental, planned, abandoned, and replaced work.
- Preserve whether an important result was reproduced, only documented, historical, or superseded.
- Keep historical information only when it provides useful project context.
- Clearly label paused, abandoned, experimental, or completed work when relevant.
- Report repository cleanliness when local changes can affect the observed state.

## Output

Update the existing project record in place.

At the end, provide a short summary of:

- what changed;
- what was intentionally preserved;
- any uncertainty that remains.
