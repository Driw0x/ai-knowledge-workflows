# Extract Knowledge Prompt

Inspect the supplied source material and extract durable knowledge that is useful for future reasoning.

## Possible sources

- repository code;
- documentation;
- research notes;
- technical reports;
- experiment logs;
- project discussions;
- external references.

## Extract

Identify:

- concepts;
- methods;
- algorithms;
- tools;
- architectural patterns;
- implementation lessons;
- reusable constraints;
- project-specific knowledge;
- demonstrated competencies.

## Rules

- Extract only information supported by the source.
- Do not copy transient debugging history unless it teaches a reusable lesson.
- Do not duplicate information already present in the knowledge base.
- Prefer concise, durable statements.
- Preserve important technical nuance.
- Separate general knowledge from project-specific facts.
- Prefer one responsible canonical note for each reusable concept. Keep detailed results and project history in their source records.
- Preserve provenance when it affects interpretation or evidence strength.
- Add links to related existing notes when appropriate.

## Output

Propose:

- new notes to create;
- existing notes to update;
- links to add;
- information that should not be stored.

For each candidate, name the supporting source, responsible note, maximum
evidence level, and whether to create, consolidate, defer, or ignore it.

Do not modify files unless explicitly requested.
