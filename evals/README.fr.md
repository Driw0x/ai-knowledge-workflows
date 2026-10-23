[English](README.md) | [Français](README.fr.md) | [简体中文](README.zh-CN.md)

[README du projet](../README.fr.md)

<a id="prompt-evaluation-benchmarks"></a>
# Benchmarks d'évaluation de prompts

Ce dossier définit des cas d'évaluation légers pour les flux de prompts de ce dépôt.

L'objectif est de rendre les modifications de prompts révisables et mesurables, au lieu de se fier uniquement aux impressions subjectives.

<a id="evaluation-flow"></a>
## Flux d'évaluation

```text
Prompt
  ↓
Evaluation case
  ↓
Agent / model output
  ↓
Evaluation rubric
  ↓
Evaluation report
  ↓
Comparison with previous prompt version
```

<a id="what-can-be-evaluated"></a>
## Qu'est-ce qui peut être évalué ?

Exemples incluent :

- des prompts de mise à jour de projet ;
- des prompts d'évaluation de compétences ;
- des prompts de mise à jour de documentation ;
- des prompts de recherche professionnelle ;
- des prompts de maintenance d'une base de connaissances.

<a id="directory-structure"></a>
## Structure du dossier

```text
evals/
├── README.md
├── rubrics/
│   └── prompt-evaluation-rubric.md
├── templates/
│   └── evaluation-report.md
├── cases/
│   ├── application-preparation.md
│   ├── project-update.md
│   ├── skill-evaluation.md
│   └── documentation-update.md
└── results/
    ├── application-preparation.md
    ├── project-update.md
    ├── skill-evaluation.md
    └── documentation-update.md
```

<a id="evaluation-principles"></a>
## Principes d'évaluation

<a id="use-representative-tasks"></a>
### Utilisez des tâches représentatives

Les cas d'évaluation doivent refléter des échecs réels dans les flux de travail ou des tâches récurrentes.

Ne créez pas de tests artificiels qui sont plus simples que l'utilisation réelle.

<a id="keep-evaluation-inputs-stable"></a>
### Gardez les entrées d'évaluation stables

Lors de la comparaison de versions de prompts, utilisez le même cas autant que possible.

Modifier à la fois le prompt et le cas d'évaluation en même temps rend la comparaison moins utile.

<a id="separate-prompt-quality-from-model-capability"></a>
### Séparez la qualité du prompt de la capacité du modèle

Enregistrez le modèle utilisé pour chaque exécution.

Un meilleur résultat obtenu avec un modèle plus puissant ne prouve pas nécessairement que le prompt a été amélioré.

<a id="penalize-unsupported-claims"></a>
### Sanctionnez les affirmations non prouvées

Une réponse fluide n'est pas une bonne réponse si elle invente des informations.

L'ancrage est un critère fondamental.

<a id="prefer-behavioral-evaluation"></a>
### Privilégiez une évaluation comportementale

Évaluez ce que fait réellement la sortie :

- est-elle conforme aux contraintes ?
- préserve-t-elle le contenu correct ?
- évite-t-elle des affirmations non prouvées ?
- produit-elle la structure demandée ?

<a id="running-an-evaluation"></a>
## Exécution d'une évaluation

1. Choisissez un prompt à évaluer.
2. Choisissez le cas correspondant sous `evals/cases/`.
3. Exécutez le prompt à l'aide des entrées du cas.
4. Notez la sortie avec `evals/rubrics/prompt-evaluation-rubric.md`.
5. Enregistrez le résultat avec `evals/templates/evaluation-report.md`.
6. Comparez le résultat avec les versions précédentes lorsqu'elles sont disponibles.

<a id="comparing-prompt-versions"></a>
## Comparaison entre versions de prompts

Une modification de prompt devrait idéalement améliorer une ou plusieurs dimensions sans provoquer une régression ailleurs.

Exemples :

```text
Prompt v1
vs
Prompt v2
```

ou :

```text
with AGENTS.md
vs
without AGENTS.md
```

ou :

```text
Model A
vs
Model B
```

<a id="regression"></a>
## Régression

Une régression se produit lorsque la nouvelle version de prompt se comporte de manière significativement pire sur un cas d'évaluation existant.

Exemples :

- introduit des affirmations non prouvées ;
- ignore une contrainte précédemment respectée ;
- réécrit des fichiers de manière inutile ;
- perd la structure de sortie requise ;
- manque des preuves importantes.

<a id="current-benchmark-scope"></a>
## Portée actuelle des benchmarks

L'ensemble manuel actuel de benchmarks inclut des cas et des résultats qualitatifs pour :

- la préparation d'applications et les décisions relatives au CV ;
- les mises à jour de projets ;
- l'évaluation des compétences ;
- les mises à jour de documentation.

Des cas supplémentaires pourraient couvrir :

- la recherche d'alternatives d'emploi ;
- l'extraction de connaissances ;
- synchronisation du portefeuille ;
- généralisation du référentiel ;
- analyse de compétence trans-project.

<a id="optional-automation"></a>
## Automatisation facultative

Le cadre est intentionnellement manuel et léger. Les rapports de `evals/results/` appliquent la rubrique partagée sans affirmer de performance mesurée du modèle ni de reproductibilité trans-model.

Ajouts possibles :

```text
evals/
├── scripts/
└── datasets/
```

L'automatisation doit être ajoutée uniquement après que les critères d'évaluation et les cas aient prouvé leur utilité lors d'exécutions manuelles répétées.
