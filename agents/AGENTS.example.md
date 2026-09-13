# Agent Instructions

This file defines reusable operating rules for AI agents using this repository.

Copy it to `AGENTS.md` before adapting it to your own environment.

## Core rules

1. Read the relevant source files before acting.
2. Treat supplied knowledge files as the source of truth for user-specific information.
3. Do not invent skills, experience, project results, implementation details, or preferences.
4. Distinguish clearly between:
   - verified facts;
   - analysis;
   - recommendations;
   - missing information.
5. Prefer primary sources when researching current information.
6. Preserve source links or references for time-sensitive claims.
7. Do not modify stable knowledge files unless the task explicitly requires it.
8. Keep generated reports separate from source-of-truth files.
9. Preserve useful existing content when updating documentation.
10. Prefer minimal diffs over broad rewrites.
11. Never expose secrets or private information in public outputs.
12. When a claim cannot be verified, state the limitation instead of guessing.

## Evidence policy

A skill, feature, or result is considered supported only when there is concrete evidence such as:

- source code;
- repository documentation;
- tests;
- benchmark output;
- project reports;
- coursework;
- professional experience;
- reproducible commands;
- externally verifiable sources.

A technology name appearing in a file is not enough by itself to prove competence.

## File safety

The following locations are private by default:

```text
AGENTS.md
local/
private/
```

Do not move content from those locations into public files unless explicitly requested and reviewed for anonymization.

## Career workflow

Before career research, read:

```text
local/career-profile.md
```

For each opportunity:

- verify that it is currently accessible;
- verify that it matches the requested contract type;
- verify geographic compatibility;
- verify expected academic level;
- extract important technical and non-technical requirements;
- compare requirements only against supported candidate evidence;
- identify strongest supporting projects;
- identify missing or weak evidence;
- avoid including weak matches merely to increase the number of results.

Use:

```text
templates/internship-research-report.md
```

for the output structure.

## Project workflow

When analyzing a project:

- inspect implementation before relying on documentation;
- distinguish current implementation from roadmap items;
- distinguish active approaches from abandoned experiments;
- do not attribute technologies that are not actually used;
- keep project status evidence-based;
- prefer repository evidence over marketing wording.

## Knowledge workflow

When updating a knowledge base:

- extract durable knowledge;
- avoid storing transient debugging noise unless it teaches something reusable;
- reduce duplication;
- preserve useful technical detail;
- create links between related concepts when appropriate;
- do not manufacture certainty.

## Documentation workflow

When updating documentation:

- preserve correct existing content;
- make the smallest useful change;
- prefer additions over unnecessary rewrites;
- ensure documented behavior matches current implementation;
- keep future work clearly separated from current functionality.
