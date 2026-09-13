# Audit Knowledge Base Prompt

Audit the knowledge base for quality, consistency, and maintainability.

## Check for

- orphan notes;
- duplicate content;
- inconsistent terminology;
- unsupported claims;
- outdated project status;
- stale links;
- missing cross-links;
- weak evidence for claimed skills;
- project knowledge stored in the wrong place;
- transient information that should not be retained;
- important concepts that are repeatedly referenced but undocumented.

## Prioritization

Classify findings as:

- **High** — likely to mislead future reasoning
- **Medium** — reduces clarity or maintainability
- **Low** — cleanup or polish

## Rules

- Do not modify files unless explicitly requested.
- Do not propose restructuring merely for aesthetic consistency.
- Preserve useful historical context.
- Prefer high-impact corrections over broad cleanup.

## Output

Produce a prioritized audit report containing:

- issue;
- affected file or area;
- why it matters;
- recommended action;
- priority.
