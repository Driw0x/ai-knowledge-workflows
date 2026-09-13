# Internship Research Prompt

Perform a current search for final-year internship opportunities matching the candidate profile.

## Read before starting

1. `AGENTS.md`
2. `local/career-profile.md`
3. `templates/internship-research-report.md`
4. Previous files in `local/research/` only when useful for duplicate detection or change tracking

## Objective

Find currently accessible internship opportunities that genuinely match the candidate's profile and constraints.

For the selected offers, determine:

- why each offer is relevant;
- the main requested skills and technologies;
- which requirements are already supported by candidate evidence;
- which requirements are weakly demonstrated;
- which requirements are missing;
- which existing projects provide the strongest evidence;
- which skill gaps recur across multiple offers;
- which opportunities should be prioritized;
- what the candidate should strengthen next.

## Research rules

- Search the web for current offers.
- Respect geographic, role, education-level, duration, and timing constraints from the candidate profile.
- Prefer original employer career pages when available.
- Do not treat inaccessible or clearly expired offers as active.
- Deduplicate identical offers published on multiple platforms.
- Do not infer candidate skills that are not supported by the supplied files.
- Do not include weakly related offers simply to increase the result count.
- Preserve source URLs or references needed to verify selected offers.
- Separate facts from analysis.
- State uncertainty explicitly.

## Fit evaluation

Use qualitative levels:

- **Strong**
- **Good**
- **Partial**
- **Weak**

Avoid artificial numerical precision unless a scoring method has been explicitly defined.

## Output

Use:

```text
templates/internship-research-report.md
```

Save the personal report to:

```text
local/research/YYYY-MM-DD-internships.md
```

Do not modify the candidate profile or public templates unless explicitly requested.
