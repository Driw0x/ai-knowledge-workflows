[English](prepare-application.md) | [Français](prepare-application.fr.md) | [简体中文](prepare-application.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="prepare-application-prompt"></a>
# Prompt de préparation de candidature

Préparer les documents de candidature pour une opportunité sélectionnée explicitement, sans soumettre la candidature.

<a id="read-before-starting"></a>
## Lire avant de commencer

1. `AGENTS.md`
2. L’offre d’emploi complète et sa source canonique
3. Profil de candidat vérifié, projet, compétence et expérience
4. Documents de candidature existants et variantes de CV, lorsqu'ils sont fournis
5. `prompts/application/adapt-resume.md` lorsqu'une décision sur le CV est requise

<a id="objective"></a>
## Objectif

Produire un package de préparation fondé sur des preuves, qui aide le candidat à examiner et à soumettre une candidature solide de manière manuelle.

<a id="analysis"></a>
## Analyse

1. Extraire les responsabilités réelles, les qualifications requises, les qualifications préférées, le lieu, la période et les contraintes de candidature.
2. Séparer les faits vérifiés dans l'annonce de l'interprétation et de l'information manquante.
3. Associer chaque exigence importante aux preuves du candidat.
4. Classer les preuves du candidat comme prouvées, partielles, non documentées, grande lacune ou condition critique potentiellement bloquante.
5. Sélectionner uniquement les projets et expériences les plus pertinents.
6. Enregistrer les lacunes importantes au lieu de les cacher par des formulations plus générales.
7. Si nécessaire, appliquer la décision `REUSE`, `ADAPT` ou `CREATE` provenant de `adapt-resume.md`.

<a id="grounding-rules"></a>
## Règles d’ancrage dans les sources

- Ne pas inventer des compétences, des expériences, des indicateurs, des résultats, des responsabilités, un niveau de langue, une disponibilité ou une motivation.
- Ne pas inférer des preuves du candidat à partir de l'annonce du poste.
- Préserver le sens et les limites des preuves sources.
- Ne pas inclure des chemins internes de fichiers ni des notes privées dans les documents visibles par le candidat.
- Considérer les faits sur une entreprise comme actuels uniquement s'ils sont soutenus par une source fiable.
- Distinger les faits des recommandations et des formulations proposées.

<a id="optional-cover-letter"></a>
## Lettre de motivation facultative

Créer une lettre de motivation uniquement si demandée. Fondé chaque élément du candidat sur les preuves fournies. Relier les preuves les plus fortes au poste réel, indiquer honnêtement les domaines d'apprentissage importants, éviter les louanges génériques ou les listes de technologies. Garder les champs d'identité et de contact séparés des textes générés lorsque le modèle de document les prévoit.

<a id="human-review"></a>
## Revue humaine

Le candidat doit examiner toutes les affirmations, formulations, dates, détails de contact et pièces jointes avant soumission. Ne pas soumettre des formulaires, envoyer des messages ou effectuer des inscriptions massives.

<a id="output"></a>
## Sortie

Fournir :

1. résumé vérifié de l'opportunité et de sa source ;
2. analyse des exigences versus preuves ;
3. preuves les plus fortes à mettre en avant ;
4. lacunes et exigences non prouvées ;
5. décision sur le CV et justification, si applicable ;
6. documents de candidature proposés par l'utilisateur ;
7. faits ou formulations nécessitant une revue humaine ;
8. actions à suivre manuellement.

Modifier uniquement les fichiers de candidature explicitement demandés. Préservé les profils sources, les enregistrements de projets, les CVs et les modèles existants.
