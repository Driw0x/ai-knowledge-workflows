# Generalize Repository Prompt

Extract a reusable public repository from a private or local source while
preserving working behavior and private boundaries.

## Define before acting

- intended public purpose and audience;
- components required for that purpose;
- private source content that must remain unchanged and unpublished;
- standalone validation required for completion.

Audit the source and target before modifying either repository.

## Method

1. Inspect current implementation, tests, documentation, configuration, and
   recent history in the source repository.
2. Inspect the target repository and preserve its identity, structure, and
   unrelated local changes.
3. Identify reusable components and their minimum dependencies.
4. Extract the stable pattern rather than copying task-specific prompts,
   private records, generated outputs, or local history.
5. Replace machine-specific paths and private constants with documented inputs
   or configuration only when required.
6. Preserve behavior with the smallest coherent target diff.
7. Update target documentation to match the extracted implementation.
8. Keep source repository metadata and `.git/` history out of copied content.
   Preserve existing target history, or prepare a new independent history only
   when explicitly requested.
9. Validate the target independently from the private source.

## Privacy and safety checks

Scan candidate content and the final diff for:

- names and contact details;
- usernames, personal URLs, and absolute paths;
- credentials, tokens, keys, and local databases;
- private project, client, employer, or application data;
- private metrics, benchmarks, logs, and generated artifacts;
- instructions that depend on one user's local structure.

Use fictional or anonymized examples. Do not copy secrets and then redact them
in a later commit; exclude them before writing public files.

## Validation

Run, when relevant:

- targeted and full relevant tests;
- static, type, and build checks;
- standalone smoke test;
- documentation path and link checks;
- secret and privacy scan;
- `git diff --check` and final diff review.

## Output

Report:

1. source and target state inspected;
2. reusable patterns extracted;
3. source-specific content deliberately excluded;
4. files added, modified, or removed in the target;
5. validation and privacy results;
6. remaining limitations.

Do not commit or publish unless explicitly requested. Do not modify the private
source unless the task separately requires it.
