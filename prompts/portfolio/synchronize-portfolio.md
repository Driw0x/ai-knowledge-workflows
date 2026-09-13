# Portfolio Synchronization Prompt

Synchronize the public portfolio with the current verified knowledge base.

## Read before starting

1. `AGENTS.md`
2. Relevant project profiles
3. Relevant skill records
4. Career or target-role information
5. The current portfolio repository

## Source of truth

Treat the verified knowledge base as the source of truth for:

- project status;
- project descriptions;
- technologies;
- demonstrated skills;
- milestones;
- measurable results.

Treat the portfolio as the public presentation layer.

## Objective

Update the portfolio so that it reflects the current candidate profile without exposing unnecessary private or internal information.

Review:

- featured projects;
- project status;
- project descriptions;
- technologies;
- skills;
- project-to-skill relationships;
- links;
- current role positioning;
- outdated claims.

## Rules

- Do not invent portfolio claims.
- Do not add skills that are unsupported by the knowledge base.
- Do not expose private notes, internal evaluations, or application data.
- Preserve the existing portfolio structure unless a structural change is clearly justified.
- Prefer minimal diffs.
- Do not publish every internal milestone.
- Surface only information that is useful to an external reader such as a recruiter or technical reviewer.
- Keep project wording concise and evidence-based.
- Ensure project status matches the current source of truth.
- Preserve featured-project limits unless explicitly requested otherwise.
- Do not replace stronger project evidence with newer but weaker projects.
- Avoid duplicating the same competency across several descriptions when it adds no value.

## Synchronization checks

### Projects

For each portfolio project, verify:

- name;
- status;
- description;
- technologies;
- links;
- key evidence;
- whether it should still be featured.

### Skills

Verify that each displayed skill is supported by:

- projects;
- coursework;
- professional experience;
- other documented evidence.

### Positioning

Check that the portfolio still reflects the candidate's current target roles and strongest technical areas.

## Output

Provide:

1. files that should change;
2. exact information that is outdated;
3. proposed minimal updates;
4. information intentionally not exposed publicly;
5. any portfolio inconsistency that should be reviewed manually.

If file modification is requested, apply only the necessary changes.

Do not modify the private knowledge base during portfolio synchronization.
