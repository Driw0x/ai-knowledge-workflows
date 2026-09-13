# AI Knowledge Workflows

Reusable AI-agent workflows, prompt patterns, and knowledge-base templates for research, project management, skill assessment, and technical documentation.

The repository is built around a simple principle:

> keep durable context in versioned files, keep prompts focused on the task, and make outputs structured enough to verify.

## What this repository demonstrates

This project is not intended to be a list of isolated prompts.

It demonstrates a reusable workflow architecture for AI agents, including:

- prompt decomposition;
- context management;
- explicit task constraints;
- evidence-based reasoning;
- output contracts;
- reusable templates;
- privacy-aware local context;
- minimal-diff update strategies;
- human-verifiable research;
- prompt versioning through Git.

These patterns are useful with coding and research agents such as Codex and other LLM-based assistants.

## Architecture

```text
User request
    ↓
AGENTS.md
    ↓
Private / local knowledge
    ↓
Task-specific prompt
    ↓
Research or repository inspection
    ↓
Structured output
    ↓
Human review
    ↓
Knowledge-base update
```

The public repository contains the reusable workflow.

Personal context remains local.

## Repository structure

```text
ai-knowledge-workflows/
├── README.md
├── LICENSE
├── .gitignore
│
├── agents/
│   └── AGENTS.example.md
│
├── prompts/
│   ├── career/
│   │   └── internship-research.md
│   ├── project/
│   │   ├── add-project.md
│   │   ├── update-project.md
│   │   └── evaluate-project.md
│   ├── knowledge/
│   │   ├── extract-knowledge.md
│   │   ├── consolidate-knowledge.md
│   │   └── audit-knowledge.md
│   ├── skills/
│   │   ├── evaluate-skills.md
│   │   └── sync-skills.md
│   └── documentation/
│       ├── update-readme.md
│       ├── update-project-doc.md
│       └── repository-audit.md
│
├── templates/
│   ├── career-profile.md
│   ├── internship-research-report.md
│   └── project-profile.md
│
├── examples/
│   └── internship-research-example.md
│
└── docs/
    └── prompt-engineering.md
```

## Workflow catalog

### Career

`prompts/career/internship-research.md`

Search current internship opportunities and compare them against a verified candidate profile.

Main ideas:

- current-source verification;
- geographic and role constraints;
- fit analysis;
- recurring skill-gap extraction;
- project-to-role matching;
- dated research reports.

### Projects

`prompts/project/`

Create, update, and evaluate project records from repository evidence.

The workflows distinguish between:

- implemented functionality;
- planned functionality;
- abandoned approaches;
- demonstrated skills;
- unsupported assumptions.

### Knowledge

`prompts/knowledge/`

Extract durable knowledge from source material, consolidate overlapping notes, and audit a knowledge base for inconsistencies.

### Skills

`prompts/skills/`

Evaluate which skills are actually demonstrated by available evidence and synchronize skill records with current projects and experience.

### Documentation

`prompts/documentation/`

Update READMEs and technical documentation while preserving valid content and minimizing unnecessary rewrites.

## Quick start

Clone the repository:

```bash
git clone https://github.com/<your-username>/ai-knowledge-workflows.git
cd ai-knowledge-workflows
```

Create local agent instructions:

```bash
cp agents/AGENTS.example.md AGENTS.md
```

Create a local private workspace:

```text
local/
├── career-profile.md
├── projects/
├── knowledge/
└── research/
```

Copy the candidate profile template:

```bash
cp templates/career-profile.md local/career-profile.md
```

`AGENTS.md`, `local/`, and `private/` are ignored by Git.

## Prompt design principles

### 1. Separate context from instructions

Stable information belongs in files.

The prompt should focus on what the agent needs to do now.

### 2. Make evidence requirements explicit

Prompts should tell the agent what counts as support for a claim.

For example:

```text
Do not infer a skill from a technology being mentioned only once.
```

### 3. Define the output contract

Prompts specify:

- what must be produced;
- where it should be stored;
- what must not be modified;
- how uncertainty should be represented.

### 4. Prefer minimal diffs

Documentation and knowledge-base workflows preserve valid information instead of rewriting entire files unnecessarily.

### 5. Distinguish fact from analysis

Research prompts separate verified information from interpretation and recommendations.

### 6. Design for reuse

Candidate-specific or project-specific details are kept outside the public prompt whenever possible.

See `docs/prompt-engineering.md` for the prompt-engineering patterns used in this repository.

## Privacy model

The public repository should contain only:

- reusable workflows;
- generic templates;
- fictional or anonymized examples;
- public documentation.

Do not commit:

- CVs containing private information;
- application history;
- private research reports;
- internal project notes that should remain private;
- API keys;
- tokens;
- passwords;
- machine-specific secrets.

## Current status

### Career
- [x] Internship research

### Projects
- [x] Add project
- [x] Update project
- [x] Evaluate project

### Knowledge
- [x] Extract knowledge
- [x] Consolidate knowledge
- [x] Audit knowledge base

### Skills
- [x] Evaluate demonstrated skills
- [x] Synchronize skills with projects

### Documentation
- [x] Update README
- [x] Update project documentation
- [x] Audit repository documentation

## Future work

- [ ] CV adaptation workflow
- [ ] Portfolio synchronization workflow
- [ ] Application preparation workflow
- [ ] Cross-project competency analysis
- [ ] Prompt evaluation benchmarks
- [ ] Model-to-model output comparison

## License

[MIT License](LICENSE)
