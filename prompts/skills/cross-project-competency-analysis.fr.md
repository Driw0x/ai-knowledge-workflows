[English](cross-project-competency-analysis.md) | [Français](cross-project-competency-analysis.fr.md) | [简体中文](cross-project-competency-analysis.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="cross-project-competency-analysis-prompt"></a>
# Prompts d'analyse de compétences transverses entre projets

Analyser les projets du candidat collectivement afin de déterminer les compétences fortement démontrées dans son portefeuille.

<a id="read-before-starting"></a>
## Lire avant de commencer

1. `AGENTS.md`
2. Profilss des projets pertinents
3. Enregistrements des compétences pertinents
4. Le profil professionnel du candidat, s'il est disponible

<a id="objective"></a>
## Objectif

Évaluer les compétences à travers plusieurs projets plutôt que projet par projet.

Identifier :

- des compétences démontrées par plusieurs projets indépendants ;
- des compétences démontrées de manière forte par un seul projet uniquement ;
- des compétences avec une preuve faible ou indirecte ;
- des compétences non soutenues ;
- des preuves de projets redondants ;
- des lacunes dans le portefeuille global des projets ;
- la preuve la plus forte pour chaque famille de poste cible.

<a id="evidence-rules"></a>
## Règles de preuve

Une compétence est plus forte lorsque elle est soutenue par :

- plusieurs projets indépendants ;
- une profondeur d'implémentation importante ;
- des tests ou des benchmarks ;
- une utilisation répétée dans différents contextes ;
- des résultats mesurables ;
- une documentation technique claire.

Ne classez pas automatiquement une compétence comme forte parce qu'elle apparaît dans plusieurs descriptions de projets.

Une répétition de preuves faibles ne signifie pas une preuve forte.

<a id="classification"></a>
## Classification

Pour chaque compétence, attribuer l'un des suivants :

- **Fortement réparti** - preuve forte dans plusieurs projets
- **Fort mais concentré** - preuve forte, mais principalement dans un seul projet
- **Modéré** - preuve claire avec une profondeur ou une largeur limitée
- **Faible** - preuve minimale ou indirecte
- **Non soutenu** - aucune preuve fiable

<a id="analysis"></a>
## Analyse

Produire un tableau avec :

|Compétence|Projets illustrant la compétence|Résumé de la preuve|Couverture|
|---|---|---|---|
|  |  |  |Fortement réparti / Fort mais concentré / Modéré / Faible / Non soutenu|

Puis identifier :

<a id="cross-project-strengths"></a>
### Points forts transverses entre projets

Des compétences soutenues par plusieurs projets et utiles dans plusieurs familles de postes cibles.

<a id="concentrated-strengths"></a>
### Points forts concentrés

Des compétences bien démontrées, mais dépendantes d'un seul projet principal.

<a id="portfolio-redundancies"></a>
### Redondances dans le portefeuille

Des projets qui démontrent presque les mêmes compétences sans apporter de nouvelle preuve significative.

<a id="portfolio-gaps"></a>
### Lacunes dans le portefeuille

Des compétences importantes manquantes ou seulement faiblement démontrées.

<a id="best-proof-projects"></a>
### Projets les plus convaincants

Pour chaque famille de poste cible, identifier les projets les plus forts ou les deux pour servir de preuve.

<a id="recommendations"></a>
## Recommandations

Recommander :

- quels projets devraient rester prépondérants ;
- quels projets devra etre renforcés ;
- quelles compétences manquantes apporteraient la plus grande valeur au portefeuille ;
- où un nouveau projet serait justifié.
- où un projet existant doit être amélioré au lieu de créer un nouveau projet.

Ne pas recommander de nouveaux projets simplement pour augmenter le nombre de projets.

Privilégier les améliorations qui étendent ou approfondissent la base de preuves.

<a id="output"></a>
## Sortie

Retour :

1. matrice de compétences ;
2. forces transverses entre projets ;
3. forces concentrées ;
4. redondances ;
5. lacunes du portefeuille ;
6. meilleurs projets de preuve par famille de rôle ;
7. recommandations priorisées.

Ne pas modifier les fichiers source sauf si explicitement demandé.
