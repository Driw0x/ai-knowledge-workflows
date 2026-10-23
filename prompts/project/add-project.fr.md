[English](add-project.md) | [Français](add-project.fr.md) | [简体中文](add-project.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="add-project-prompt"></a>
# Ajouter un prompt de projet

Examinez le référentiel cible et créez une entrée de projet structurée en utilisant uniquement des informations vérifiables.

<a id="read-before-starting"></a>
## Lisez avant de commencer

1. `AGENTS.md`
2. `templates/project-profile.md`
3. Fichiers pertinents du référentiel
4. Conventions existantes de la base de connaissances, si disponibles

Avant d'écrire, identifiez les critères de succès, le répertoire cible du projet et les fichiers qui doivent rester inchangés.

<a id="objective"></a>
## Objectif

Créez un registre bref mais utile de projet qui capture :

- l'objectif du projet ;
- le problème résolu ;
- l'état actuel ;
- les technologies réellement utilisées ;
- l'architecture ou les méthodes importants ;
- les compétences démontrées ;
- les jalons vérifiés ;
- les résultats mesurables ;
- les limites ;
- le prochain objectif pertinent.

<a id="rules"></a>
## Règles

- Vérifiez l'implémentation avant de faire confiance aux affirmations du README.
- Vérifiez la branche actuelle et `HEAD` ; distinguez les fichiers actuels de l'état distant ou des expériences historiques lorsque cela est pertinent.
- Utilisez les tests et les artefacts de benchmark comme preuves, et indiquez si des vérifications importantes ont été effectuées lors de l'analyse ou seulement documentées.
- Ne pas inférer des technologies qui ne sont pas utilisées dans le dépôt.
- Ne pas affirmer des compétences sans preuves concrètes.
- Distinguez la fonctionnalité mise en œuvre de l'œuvre planifiée.
- Distinguez les approches actives des expériences abandonnées.
- Préservez la terminologie du dépôt lorsque celle-ci est claire et précise.
- Évitez de copier de grandes sections du README telles quelles.
- Privilégiez des informations durables par rapport aux détails transitoires de débogage.
- Signalez la propreté du dépôt lorsque des modifications non commitées peuvent affecter l'état observé.

<a id="output"></a>
## Sortie

Utilisez `templates/project-profile.md`.

Si la base de connaissances dispose d'une convention de répertoire pour les projets, placez l'entrée là-dedans.

Ne pas modifier des fichiers de projet inconnexes.
