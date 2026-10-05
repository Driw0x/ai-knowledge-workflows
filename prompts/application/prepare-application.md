# Prepare Application Prompt

Prepare application materials for one explicitly selected opportunity without
submitting the application.

## Read before starting

1. `AGENTS.md`
2. The complete job posting and its canonical source
3. Verified candidate profile, project, skill, and experience records
4. Existing application materials and resume variants, when supplied
5. `prompts/application/adapt-resume.md` when a resume decision is required

## Objective

Produce a grounded preparation package that helps the candidate review and
submit a strong application manually.

## Analysis

1. Extract actual responsibilities, required qualifications, preferred
   qualifications, location, timing, and application constraints.
2. Separate verified posting facts from interpretation and missing information.
3. Map each important requirement to candidate evidence.
4. Classify candidate evidence as supported, partial, not documented,
   significant gap, or potentially blocking prerequisite.
5. Select only the strongest relevant projects and experiences.
6. Record important gaps instead of hiding them with broader wording.
7. If needed, apply the `REUSE`, `ADAPT`, or `CREATE` decision from
   `adapt-resume.md`.

## Grounding rules

- Do not invent skills, experience, metrics, results, responsibilities,
  language level, availability, or motivation.
- Do not infer candidate evidence from the job posting.
- Preserve the meaning and limits of source evidence.
- Keep internal file paths and private notes out of candidate-facing documents.
- Treat company facts as current only when supported by a reliable source.
- Distinguish facts from recommendations and proposed wording.

## Optional cover letter

Create a cover letter only when requested. Ground every candidate claim in the
supplied evidence. Connect the strongest evidence to the actual role, state
important learning areas honestly, and avoid generic praise or technology
lists. Keep identity and contact fields separate from generated prose when a
document template supplies them.

## Human review

The candidate must review all claims, wording, dates, contact details, and
attachments before submission. Do not submit forms, send messages, or perform
mass applications.

## Output

Provide:

1. verified opportunity summary and source;
2. requirement-to-evidence analysis;
3. strongest evidence to emphasize;
4. gaps and unsupported requirements;
5. resume decision and rationale, when applicable;
6. proposed application materials requested by the user;
7. facts or wording requiring human review;
8. manual next actions.

Modify only the explicitly requested application files. Preserve existing
source profiles, project records, resumes, and templates.
