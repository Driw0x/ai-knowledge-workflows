[English](documentation-update.md) | [Français](documentation-update.fr.md) | [简体中文](documentation-update.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="evaluation-case--documentation-update"></a>
# Cas d'évaluation - Mise à jour de la documentation

<a id="workflow-under-test"></a>
## Workflow soumis à l'évaluation

```text
prompts/documentation/update-project-doc.md
```

<a id="purpose"></a>
## Objectif

Évaluer si le workflow met à jour avec précision la documentation technique tout en conservant le contenu existant valide.

<a id="existing-documentation"></a>
## Documentation existante

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

<a id="new-repository-state"></a>
## État du nouveau dépôt

Le dépôt inclut maintenant :

```text
models/random_forest.py
tests/test_random_forest.py
```

L'implémentation de Random Forest est complète et les tests passent.

Il n'y a pas d'API REST.

Il n'y a pas de configuration Docker.

L'identifiant `train.py` reste valide.

<a id="expected-behavior"></a>
## Comportement attendu

Une sortie forte doit :

- conserver le chargement du CSV ;
- conserver le prétraitement ;
- conserver la base de départ en régression logistique ;
- conserver l'identifiant valide `python train.py` ;
- ajouter Random Forest aux fonctionnalités actuelles ;
- supprimer Random Forest de la roadmap ;
- garder l'API REST dans la roadmap ;
- garder la déployement Docker dans la roadmap ;
- éviter de prétendre que des fonctionnalités API ou Docker existent ;
- éviter de réécrire des documents inappropriés.

<a id="failure-examples"></a>
## Exemples de défaillances

Les éléments suivants doivent réduire la note :

- mentionner des points d'entrée REST ;
- ajouter des commandes Docker ;
- supprimer la base de départ en régression logistique ;
- modifier l'usage valide de la commande ;
- remplacer entièrement le document de manière inutile.
