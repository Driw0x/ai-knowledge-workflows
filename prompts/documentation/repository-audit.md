# Repository Documentation Audit Prompt

Audit repository documentation for accuracy, completeness, and consistency.

## Compare

Compare documentation against:

- source code;
- configuration;
- CLI interfaces;
- tests;
- directory structure;
- current project status.

## Identify

- stale README sections;
- undocumented important modules;
- commands that no longer work;
- missing setup steps;
- duplicated documentation;
- roadmap items presented as implemented;
- inconsistent terminology;
- undocumented limitations;
- missing benchmark context;
- missing links between related docs.

## Prioritization

Classify findings as:

- **Critical**
- **Important**
- **Minor**

## Rules

- Do not rewrite documentation during the audit unless explicitly requested.
- Prefer correctness over completeness.
- Do not require documentation for trivial internal details.
- Focus on information that affects users, contributors, reproducibility, or project understanding.

## Output

Produce a table containing:

- issue;
- affected file;
- evidence;
- recommended change;
- priority.
