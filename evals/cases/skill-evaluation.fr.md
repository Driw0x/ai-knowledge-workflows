[English](skill-evaluation.md) | [Français](skill-evaluation.fr.md) | [简体中文](skill-evaluation.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="evaluation-case--skill-evaluation"></a>
# Cas d'évaluation - Évaluation des compétences

<a id="workflows-under-test"></a>
## Flux de travail soumis à l'évaluation

Principal :

```text
prompts/skills/evaluate-skills.md
```

Optionnel :

```text
prompts/skills/cross-project-competency-analysis.md
```

<a id="purpose"></a>
## Objectif

Évaluer si le flux de travail distingue des preuves solides, concentrées, faibles et non soutenues concernant les compétences.

<a id="evidence"></a>
## Preuves

<a id="project-alpha"></a>
### Projet Alpha

- Application en Python
- Formation d'un modèle PyTorch
- tests unitaires pour le prétraitement des données
- résultats de formation documentés

<a id="project-beta"></a>
### Projet Beta

- application en Python
- pipeline de classification scikit-learn
- ingénierie de caractéristiques
- évaluation avec validation croisée

<a id="project-gamma"></a>
### Projet Gamma

- interface frontend en TypeScript
- composants React
- aucune déploiement backend

<a id="skills-to-assess"></a>
## Compétences à évaluer

- Python
- PyTorch
- scikit-learn
- Apprentissage automatique
- React
- Docker
- Kubernetes

<a id="expected-behavior"></a>
## Comportement attendu

Une réponse forte devrait conclure approximativement :

<a id="python"></a>
### Python

Preuves solides dans plusieurs projets indépendants.

<a id="machine-learning"></a>
### Apprentissage automatique

Preuves solides et distribuées dans Alpha et Beta.

<a id="pytorch"></a>
### PyTorch

Preuves solides mais concentrées dans Alpha.

<a id="scikit-learn"></a>
### scikit-

Preuves modérées ou solides mais concentrées dans Beta, selon la rubrique exacte utilisée.

<a id="react"></a>
### React

Démontrée, mais concentrée dans Gamma.

<a id="docker"></a>
### Docker

Non soutenue.

<a id="kubernetes"></a>
### Kubernetes

Non soutenue.

<a id="failure-examples"></a>
## Exemples de défaillances

Les cas suivants devraient réduire la note :

- affirmer Docker parce que les projets sont des projets logiciels ;
- affirmer Kubernetes sans preuve ;
- considérer chaque technologie comme ayant une force égale ;
- ignorer les preuves croisées pour Python et Apprentissage automatique ;
- évaluer PyTorch comme distribué dans plusieurs projets.
