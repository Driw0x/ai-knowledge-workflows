# Adapt Resume Prompt

Choose and prepare the most suitable resume for one job posting using only
verified candidate evidence.

## Read before starting

1. `AGENTS.md`
2. The complete job posting
3. Verified candidate evidence
4. Existing resume variants and their actual content
5. Resume format and length constraints

## Decision

Choose exactly one action:

- **REUSE** — an existing resume already fits sufficiently without substantive
  changes.
- **ADAPT** — an existing resume is a suitable base, but emphasis, ordering, or
  wording should change.
- **CREATE** — no existing resume provides a sufficiently appropriate basis.

Prefer `REUSE`, then `ADAPT`, when they represent the evidence accurately.
Do not create a new variant merely because the wording could be different.

## Rules

- Compare job responsibilities and requirements with resume content, not file
  names or variant labels alone.
- Do not invent a skill, experience, project role, result, date, or metric.
- Do not convert related experience into exact experience.
- Preserve factual meaning when shortening or reframing evidence.
- Prioritize relevant evidence and remove only lower-value content needed to
  respect format constraints.
- Keep wording readable by a recruiter and specific enough to verify.
- Record important unsupported requirements rather than inserting them into the
  resume.
- Preserve the source resume or template. Write adapted output to a separate
  target when modification is requested.

## Output

Provide:

1. `REUSE`, `ADAPT`, or `CREATE`;
2. selected base resume, if any;
3. evidence-based rationale;
4. content to emphasize, reorder, rewrite, or omit;
5. important gaps that must not be claimed;
6. target file, when a new document is requested;
7. checks performed on factual accuracy, format, and readability.

The candidate reviews the final resume before use.
