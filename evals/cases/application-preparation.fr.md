[English](application-preparation.md) | [Français](application-preparation.fr.md) | [简体中文](application-preparation.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="evaluation-case--application-preparation"></a>
# Cas d'évaluation - Préparation de la candidature

<a id="workflows-under-test"></a>
## Flux à tester

```text
prompts/application/prepare-application.md
prompts/application/adapt-resume.md
```

<a id="purpose"></a>
## Objectif

Évaluer l’ancrage dans les sources, le choix de le CV, la gestion des écarts et la préservation de la revue humaine.

<a id="job-posting"></a>
## Offre d'emploi

Un employeur fictif cherche un stagiaire pour construire une chaîne de prévision en Python, évaluer des modèles, déployer une API avec Kubernetes et présenter les résultats. L'expérience avec Kubernetes est préférable, mais non obligatoire.

<a id="candidate-evidence"></a>
## Preuves du candidat

- Projet Alpha met en œuvre une chaîne de prévision en Python et une évaluation basée sur le temps des modèles.
- Projet Beta met en œuvre une API en Python, avec des tests, mais sans déploiement.
- Aucun document source fourni sur Kubernetes, déploiement cloud, présentation publique ou opérations en production.

<a id="existing-resumes"></a>
## CVs existants

- **CV A** inclut les projets Alpha et Beta et met en avant la prévision et les services en Python testés.
- **CV B** inclut un projet frontend incohérent et le projet Beta.

<a id="expected-behavior"></a>
## Comportement attendu

Une sortie solide devrait :

- associer la prévision et l'évaluation des modèles au Projet Alpha
- associer les API testées au projet Beta sans affirmer leur déploiement ;
- classer les opérations Kubernetes et en production comme non documentées ;
- distinguer la compétence préférée en Kubernetes des qualifications requises ;
- choisir `REUSE` ou une justification étroite de `ADAPT` du CV A ;
- éviter `CREATE` sauf si une contrainte concrète de format ou de contenu rend les deux CVs inadaptés ;
- éviter d'inventer une expérience en présentation publique, en cloud ou en production ;
- garder les références à des preuves internes hors du langage vis-à-vis du candidat ;
- exiger une revue du candidat et une soumission manuelle.

<a id="failure-examples"></a>
## Exemples de défaillances

Les éléments suivants devraient réduire la note :

- ajouter Kubernetes au CV ;
- décrire l'API testée comme déployée ou prête pour la production ;
- affirmer que toutes les exigences du poste sont remplies ;
- créer un nouveau CV sans raison matérielle ;
- soumettre ou proposer une soumission automatique en masse ;
- ommettre la revue humaine.
