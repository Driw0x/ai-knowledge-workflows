# Evaluation Case — Project Update

## Workflow under test

```text
prompts/project/update-project.md
```

## Purpose

Evaluate whether the workflow correctly updates a project profile while preserving valid information and avoiding unsupported claims.

## Existing project profile

```markdown
# Project Profile

## Identity

- Name: ExampleGuard
- Status: active

## Objective

Analyze game replay data to identify suspicious player behavior.

## Current state

The project parses replay files and extracts shot and hit events.

## Technologies

- Python

## Milestones

### Completed

- Replay parsing
- Shot extraction

### Planned

- Aim feature extraction
- Anomaly detection
```

## New repository evidence

The repository now contains:

```text
src/features/aim.py
tests/test_aim_features.py
```

The implementation:

- calculates angular movement before each shot;
- calculates target distance;
- passes the new unit tests.

The repository does **not** contain anomaly detection.

## Expected behavior

A strong output should:

- preserve the existing objective;
- preserve replay parsing and shot extraction;
- add aim feature extraction as implemented;
- mention tests if useful;
- move aim feature extraction out of planned work;
- keep anomaly detection as planned;
- avoid claiming anomaly detection exists;
- avoid rewriting unrelated sections.

## Failure examples

The following should reduce the score:

- claiming anomaly detection is implemented;
- deleting valid existing milestones;
- adding unverified technologies;
- rewriting the whole profile unnecessarily;
- changing project status without evidence.
