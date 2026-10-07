# AI Knowledge Workflows

[English](README.md) | [Français](README.fr.md) | [简体中文](README.zh-CN.md)

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
│   ├── application/
│   ├── career/
│   ├── project/
│   ├── knowledge/
│   ├── skills/
│   ├── documentation/
│   └── portfolio/
│
├── templates/
│
├── examples/
│
├── docs/
│
└── evals/
    ├── README.md
    ├── rubrics/
    ├── templates/
    ├── results/
    └── cases/
```

## Workflow catalog

### Applications

`prompts/application/`

Prepare grounded application materials and choose whether to reuse, adapt, or
create a resume. The workflows preserve human review and manual submission.

For a standalone application that implements this workflow, see [AI Job Application Workbench](https://github.com/Driw0x/ai-job-application-workbench).

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

Evaluate which skills are actually demonstrated by available evidence, synchronize skill records with current projects and experience, and analyze competency evidence across multiple projects.

### Documentation

`prompts/documentation/`

Audit or update technical documentation, and extract a reusable standalone
repository from private sources while preserving privacy and working behavior.

### Portfolio

`prompts/portfolio/synchronize-portfolio.md`

Synchronize the public portfolio with the verified knowledge base while preserving privacy and using minimal diffs.

## Prompt evaluation

`evals/`

Evaluate prompt behavior with reusable cases, a shared rubric, and structured evaluation reports.

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

**Status: v1 complete — maintained and extended with grounded application and repository-generalization workflows.**

### Career
- [x] Internship research

### Applications
- [x] Grounded application preparation
- [x] Resume reuse / adaptation / creation decision

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
- [x] Cross-project competency analysis

### Documentation
- [x] Update README
- [x] Update project documentation
- [x] Audit repository documentation
- [x] Generalize a private or local repository

### Portfolio
- [x] Portfolio synchronization workflow

### Prompt evaluation
- [x] Prompt evaluation cases, rubric, and qualitative results

## Possible extensions

The following items are optional and outside the v1 scope:

- [ ] Model-to-model output comparison

## License

[MIT License](LICENSE)
