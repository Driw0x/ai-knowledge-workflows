# AI Knowledge Workflows

[English](README.md) | [Français](README.fr.md) | [简体中文](README.zh-CN.md)

Workflows d'agents IA réutilisables, modèles de prompts et templates de Knowledge Base pour la recherche, la gestion de projets, l'évaluation des compétences et la documentation technique.

Le repository repose sur un principe simple :

> conserver le contexte durable dans des fichiers versionnés, garder les prompts centrés sur la tâche et structurer suffisamment les sorties pour pouvoir les vérifier.

## Ce que démontre ce repository

Ce projet n'a pas vocation à être une liste de prompts isolés.

Il présente une architecture de workflows réutilisables pour les agents IA, notamment :

- décomposition des prompts ;
- gestion du contexte ;
- contraintes de tâche explicites ;
- raisonnement fondé sur des preuves ;
- contrats de sortie ;
- templates réutilisables ;
- contexte local respectueux de la confidentialité ;
- stratégies de mise à jour avec diff minimal ;
- recherche vérifiable par un humain ;
- versionnage des prompts avec Git.

Ces patterns sont utiles avec des agents de code et de recherche tels que Codex et d'autres assistants basés sur des LLM.

## Architecture

```text
Requête utilisateur
    ↓
AGENTS.md
    ↓
Connaissances privées / locales
    ↓
Prompt spécifique à la tâche
    ↓
Recherche ou inspection du repository
    ↓
Sortie structurée
    ↓
Revue humaine
    ↓
Mise à jour de la Knowledge Base
```

Le repository public contient le workflow réutilisable.

Le contexte personnel reste local.

## Structure du repository

```text
ai-knowledge-workflows/
├── README.md
├── LICENSE
├── .gitignore
│
├── agents/
│
├── prompts/
│   ├── application/
│   ├── career/
│   ├── project/
│   ├── knowledge/
│   ├── skills/
│   ├── documentation/
│   └── portfolio/
│
├── templates/
│
├── examples/
│
├── docs/
│
└── evals/
    ├── README.md
    ├── rubrics/
    ├── templates/
    ├── results/
    └── cases/
```

## Catalogue des workflows

### Candidatures

`prompts/application/`

Prépare des documents de candidature fondés sur les sources et choisit s'il faut réutiliser, adapter ou créer un CV. Les workflows conservent la revue humaine et l'envoi manuel.

Pour une application autonome qui met en œuvre ce workflow, voir [AI Job Application Workbench](https://github.com/Driw0x/ai-job-application-workbench).

### Carrière

`prompts/career/internship-research.md`

Recherche des offres de stage actuelles et les compare à un profil candidat vérifié.

Principales idées :

- vérification à partir de sources actuelles ;
- contraintes géographiques et de rôle ;
- analyse d'adéquation ;
- extraction récurrente des écarts de compétences ;
- correspondance projets-postes ;
- rapports de recherche datés.

### Projets

`prompts/project/`

Crée, met à jour et évalue les fiches projet à partir de preuves issues du repository.

Les workflows distinguent :

- fonctionnalités implémentées ;
- fonctionnalités prévues ;
- approches abandonnées ;
- compétences démontrées ;
- hypothèses non étayées.

### Connaissances

`prompts/knowledge/`

Extrait des connaissances durables à partir de sources, consolide les notes qui se chevauchent et audite une Knowledge Base pour détecter les incohérences.

### Compétences

`prompts/skills/`

Évalue quelles compétences sont réellement démontrées par les preuves disponibles, synchronise les fiches de compétences avec les projets et l'expérience actuels, et analyse les preuves de compétences à travers plusieurs projets.

### Documentation

`prompts/documentation/`

Audite ou met à jour la documentation technique et extrait un repository autonome réutilisable à partir de sources privées tout en préservant la confidentialité et le comportement fonctionnel.

### Portfolio

`prompts/portfolio/synchronize-portfolio.md`

Synchronise le portfolio public avec la Knowledge Base vérifiée tout en préservant la confidentialité et en privilégiant des diffs minimaux.

## Évaluation des prompts

`evals/`

Évalue le comportement des prompts avec des cas réutilisables, une grille commune et des rapports d'évaluation structurés.

## Démarrage rapide

Clonez le repository :

```bash
git clone https://github.com/<your-username>/ai-knowledge-workflows.git
cd ai-knowledge-workflows
```

Créez les instructions locales de l'agent :

```bash
cp agents/AGENTS.example.md AGENTS.md
```

Créez un espace de travail privé local :

```text
local/
├── career-profile.md
├── projects/
├── knowledge/
└── research/
```

Copiez le template de profil candidat :

```bash
cp templates/career-profile.md local/career-profile.md
```

`AGENTS.md`, `local/` et `private/` sont ignorés par Git.

## Principes de conception des prompts

### 1. Séparer le contexte des instructions

Les informations stables doivent être stockées dans des fichiers.

Le prompt doit se concentrer sur ce que l'agent doit accomplir maintenant.

### 2. Rendre explicites les exigences de preuve

Les prompts doivent indiquer ce qui constitue une preuve suffisante pour étayer une affirmation.

Par exemple :

```text
Do not infer a skill from a technology being mentioned only once.
```

### 3. Définir le contrat de sortie

Les prompts précisent :

- ce qui doit être produit ;
- où le résultat doit être stocké ;
- ce qui ne doit pas être modifié ;
- comment l'incertitude doit être représentée.

### 4. Privilégier les diffs minimaux

Les workflows de documentation et de Knowledge Base préservent les informations valides au lieu de réécrire inutilement des fichiers entiers.

### 5. Distinguer les faits de l'analyse

Les prompts de recherche séparent les informations vérifiées de l'interprétation et des recommandations.

### 6. Concevoir pour la réutilisation

Les détails propres à un candidat ou à un projet restent hors du prompt public chaque fois que possible.

Voir `docs/prompt-engineering.md` pour les patterns de prompt engineering utilisés dans ce repository.

## Modèle de confidentialité

Le repository public doit contenir uniquement :

- des workflows réutilisables ;
- des templates génériques ;
- des exemples fictifs ou anonymisés ;
- de la documentation publique.

Ne commitez pas :

- des CV contenant des informations privées ;
- l'historique des candidatures ;
- des rapports de recherche privés ;
- des notes internes de projet qui doivent rester privées ;
- des clés API ;
- des tokens ;
- des mots de passe ;
- des secrets propres à une machine.

## État actuel

**Statut : v1 terminée — maintenue et étendue avec des workflows de candidature fondés sur les sources et de généralisation de repositories.**

### Carrière
- [x] Recherche de stages

### Candidatures
- [x] Préparation de candidatures fondée sur les sources
- [x] Décision de réutilisation / adaptation / création de CV

### Projets
- [x] Ajouter un projet
- [x] Mettre à jour un projet
- [x] Évaluer un projet

### Connaissances
- [x] Extraire les connaissances
- [x] Consolider les connaissances
- [x] Auditer la Knowledge Base

### Compétences
- [x] Évaluer les compétences démontrées
- [x] Synchroniser les compétences avec les projets
- [x] Analyse des compétences à travers plusieurs projets

### Documentation
- [x] Mettre à jour le README
- [x] Mettre à jour la documentation projet
- [x] Auditer la documentation du repository
- [x] Généraliser un repository privé ou local

### Portfolio
- [x] Workflow de synchronisation du portfolio

### Évaluation des prompts
- [x] Cas d'évaluation, grille et résultats qualitatifs

## Extensions possibles

Les éléments suivants sont facultatifs et hors du périmètre de la v1 :

- [ ] Comparaison des sorties entre modèles

## Licence

[Licence MIT](LICENSE)
