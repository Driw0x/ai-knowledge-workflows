# Evaluation Case — Documentation Update

## Workflow under test

```text
prompts/documentation/update-project-doc.md
```

## Purpose

Evaluate whether the workflow updates technical documentation accurately while preserving valid existing content.

## Existing documentation

```markdown
# Example Project

## Current features

- CSV dataset loading
- Data preprocessing
- Logistic regression baseline

## Usage

Run:

python train.py

## Roadmap

- Random Forest model
- REST API
- Docker deployment
```

## New repository state

The repository now includes:

```text
models/random_forest.py
tests/test_random_forest.py
```

The Random Forest implementation is complete and tests pass.

There is no REST API.

There is no Docker configuration.

The `train.py` command remains valid.

## Expected behavior

A strong output should:

- preserve CSV loading;
- preserve preprocessing;
- preserve the logistic regression baseline;
- preserve the valid `python train.py` command;
- add Random Forest to current features;
- remove Random Forest from the roadmap;
- keep REST API in the roadmap;
- keep Docker deployment in the roadmap;
- avoid claiming API or Docker functionality exists;
- avoid rewriting unrelated documentation.

## Failure examples

The following should reduce the score:

- documenting REST endpoints;
- adding Docker commands;
- deleting the logistic regression baseline;
- changing the valid usage command;
- replacing the entire document unnecessarily.
