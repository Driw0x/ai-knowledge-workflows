[English](project-update.md) | [Français](project-update.fr.md) | [简体中文](project-update.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="evaluation-case--project-update"></a>
# Cas d'évaluation - Mise à jour du projet

<a id="workflow-under-test"></a>
## Flux en cours de test

```text
prompts/project/update-project.md
```

<a id="purpose"></a>
## Objectif

Évaluer si le flux met à jour correctement le profil du projet tout en conservant les informations valides et en évitant les affirmations non justifiées.

<a id="existing-project-profile"></a>
## Profil de projet existant

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

<a id="new-repository-evidence"></a>
## Nouvelles preuves du dépôt

Le dépôt contient maintenant :

```text
src/features/aim.py
tests/test_aim_features.py
```

L'implémentation :

- calcule le mouvement angulaire avant chaque tir ;
- calcule la distance cible ;
- passe les nouveaux tests unitaires.

Le dépôt ne contient pas de détection d'anomalies.

<a id="expected-behavior"></a>
## Comportement attendu

Un résultat solide doit :

- conserver l'objectif existant ;
- conserver la lecture des reprises et l'extraction des tirs ;
- ajouter l'extraction de la cible comme implémentée ;
- mentionner les tests si pertinent ;
- déplacer l'extraction de la cible hors des travaux planifiés ;
- conserver la détection d'anomalies comme planifiée ;
- éviter d'affirmer que la détection d'anomalies existe ;
- éviter de réécrire des sections inconnues.

<a id="failure-examples"></a>
## Exemples de défaillances

Les éléments suivants doivent réduire la note :

- affirmer que la détection d'anomalies est implémentée ;
- supprimer des jalons existants valides ;
- ajouter des technologies non vérifiées ;
- réécrire entièrement le profil sans nécessité ;
- changer l'état du projet sans preuve.
