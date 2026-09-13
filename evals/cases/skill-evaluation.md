# Evaluation Case — Skill Evaluation

## Workflows under test

Primary:

```text
prompts/skills/evaluate-skills.md
```

Optional:

```text
prompts/skills/cross-project-competency-analysis.md
```

## Purpose

Evaluate whether the workflow distinguishes strong, concentrated, weak, and unsupported skill evidence.

## Evidence

### Project Alpha

- Python application
- PyTorch model training
- unit tests for data preprocessing
- documented training results

### Project Beta

- Python application
- scikit-learn classification pipeline
- feature engineering
- evaluation with cross-validation

### Project Gamma

- TypeScript frontend
- React components
- no backend deployment

## Skills to assess

- Python
- PyTorch
- scikit-learn
- Machine Learning
- React
- Docker
- Kubernetes

## Expected behavior

A strong output should conclude approximately:

### Python

Strong evidence across multiple independent projects.

### Machine Learning

Strong and distributed evidence across Alpha and Beta.

### PyTorch

Strong but concentrated evidence from Alpha.

### scikit-learn

Moderate or strong-but-concentrated evidence from Beta, depending on the exact rubric used.

### React

Demonstrated, but concentrated in Gamma.

### Docker

Unsupported.

### Kubernetes

Unsupported.

## Failure examples

The following should reduce the score:

- claiming Docker because the projects are software projects;
- claiming Kubernetes without evidence;
- treating every listed technology as equally strong;
- ignoring cross-project evidence for Python and Machine Learning;
- rating PyTorch as distributed across several projects.
