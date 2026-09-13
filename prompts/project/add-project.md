# Add Project Prompt

Inspect the target repository and create a structured project entry using only verifiable information.

## Read before starting

1. `AGENTS.md`
2. `templates/project-profile.md`
3. Relevant repository files
4. Existing knowledge-base conventions, if available

## Objective

Create a concise but useful project record that captures:

- project objective;
- problem being solved;
- current status;
- technologies actually used;
- important architecture or methods;
- demonstrated skills;
- verified milestones;
- measurable results;
- limitations;
- next relevant milestone.

## Rules

- Inspect implementation before relying on README claims.
- Do not infer technologies that are not used in the repository.
- Do not claim skills without concrete evidence.
- Distinguish implemented functionality from planned work.
- Distinguish active approaches from abandoned experiments.
- Preserve repository terminology when it is clear and accurate.
- Avoid copying large README sections verbatim.
- Prefer durable information over transient debugging details.

## Output

Use `templates/project-profile.md`.

If the knowledge base has a project directory convention, place the new entry there.

Do not modify unrelated project files.
