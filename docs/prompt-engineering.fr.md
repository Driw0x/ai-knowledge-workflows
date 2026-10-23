[English](prompt-engineering.md) | [Français](prompt-engineering.fr.md) | [简体中文](prompt-engineering.zh-CN.md)

[README du projet](../README.fr.md)

<a id="prompt-engineering-patterns"></a>
# Patterns d'ingénierie de prompts

Ce dépôt utilise l'ingénierie de prompts comme pratique de conception logicielle, plutôt que comme une collection d'instructions isolées.

<a id="1-context-decomposition"></a>
## 1. Décomposition du contexte

Un prompt ne doit pas contenir toutes les pièces de contexte utilisateur ou projet.

Au contraire :

```text
AGENTS.md
+ domain knowledge
+ task prompt
+ output template
```

Cela améliore la réutilisation et réduit la duplication.

<a id="2-explicit-evidence-policy"></a>
## 2. Politique d'éléments de preuve

Les prompts définissent ce qui constitue une preuve.

Exemple :

```text
Do not infer competence from a technology being mentioned only once.
```

Cela réduit les conclusions non fondées.

<a id="3-positive-and-negative-constraints"></a>
## 3. Contraintes positives et négatives

Les bons prompts de tâche spécifient à la fois :

- ce que l'agent doit faire ;
- ce que l'agent doit éviter.

Exemple :

```text
Preserve valid existing content.
Prefer minimal diffs.
Do not document roadmap items as implemented.
```

<a id="4-output-contracts"></a>
## 4. Contrats d'output

L'agent reçoit une structure cible plutôt qu'une demande ouverte.

Cela inclut par exemple :

- des profils de projet ;
- des rapports de recherche sur des stages ;
- des tables d'audit.

Cela rend les sorties plus faciles à comparer, à examiner et à versionner.

<a id="5-tool-aware-prompting"></a>
## 5. Prompting conscient des outils

Les prompts de recherche exigent une vérification à partir de sources actuelles.

Les prompts de dépôt exigent une inspection du code source avant de faire confiance à la documentation.

Le prompt reflète donc les capacités requises pour la tâche.

Dans le cas d'un dépôt, l'implémentation actuelle et les tests exécutables ont priorité sur la documentation obsolète. La documentation reste un élément de preuve utile, mais pas lorsque celle-ci contredit le comportement observé.

<a id="6-uncertainty-handling"></a>
## 6. Gestion de l'incertitude

Les workflows instruisent l'agent à distinguer :

- des faits vérifiés ;
- des analyses ;
- des recommandations ;
- des informations manquantes.

Cela est plus fiable que de forcer une réponse définitive.

<a id="7-minimal-diff-editing"></a>
## 7. Édition minimal-diff

Pour la maintenance de la documentation et de la base de connaissances, les prompts privilégient explicitement des modifications minimales.

Cela aide à préserver le contexte écrit par les humains et réduit les retours accidentels.

<a id="8-privacy-aware-prompting"></a>
## 8. Prompting conscient de la confidentialité

Les prompts réutilisables sont séparés du contexte local privé.

Le workflow peut être open source tout en gardant les données personnelles locales.

<a id="9-versionability"></a>
## 9. Versionnabilité

Les prompts sont stockés sous forme de fichiers texte et versionnés avec Git.

Les modifications peuvent donc être revues comme du code :

- qu'est-ce qui a changé ;
- pourquoi cela a changé ;
- quelle comportement de workflow est affecté.

<a id="10-evaluation-oriented-design"></a>
## 10. Conception orientée évaluation

Un workflow de prompt devient plus robuste lorsqu'il peut être évalué.

Ce dépôt inclut :

- des cas d'évaluation stables ;
- une rubrique partagée ;
- des rapports qualitatifs de résultats ;
- des critères de régression pour comparer le comportement des prompts.

Ce cadre reste manuel et léger. Les comparaisons entre modèles, l'exécution automatisée et les tests de cohérence sur plusieurs exécutions restent des extensions optionnelles plutôt que des exigences de version 1.

<a id="11-success-criteria-before-execution"></a>
## 11. Critères de succès avant exécution

Avant une modification substantielle, définir :

- le résultat observable ;
- le comportement et les fichiers qui doivent rester inchangés ;
- les vérifications requises avant la finalisation.

Cela empêche l'implémentation de devenir la définition de succès après coup.

<a id="12-diagnose-fix-and-verify"></a>
## 12. Diagnostiquer, corriger et vérifier

Un workflow fiable est :

```text
reproduce or trace the failure
    ↓
identify the root cause
    ↓
apply a targeted fix
    ↓
run a regression check
    ↓
run broader relevant checks and a smoke test
```

Écrire la modification constitue seulement une étape. Un workflow ne doit pas considérer la finalisation jusqu'à ce que la validation pertinente ait été exécutée.

<a id="13-grounded-generation-pipelines"></a>
## 13. Pipelines d'origine fondée

Lorsque la sortie contient des affirmations concernant une personne, un projet ou un système, utiliser un pipeline explicite :

```text
source facts
    ↓
relevant evidence selection
    ↓
generation
    ↓
claim and output validation
```

Le modèle peut sélectionner, condenser, organiser et reformuler des preuves. Il ne doit pas créer de faits, de métriques, d'expériences ou de résultats manquants.

<a id="14-human-in-the-loop-boundaries"></a>
## 14. Limites de l'humain dans le processus

Les workflows à forte impact doivent identifier les décisions qui restent des actions humaines. Par exemple, les workflows d'application peuvent découvrir, analyser et préparer des matériels, mais le candidat examine le contenu final et le soumet manuellement.

```text
discovery
    ↓
analysis
    ↓
preparation
    ↓
human review
    ↓
manual action
    ↓
tracking
```

<a id="15-reusable-extraction-across-repository-boundaries"></a>
## 15. Extraction réutilisable au-delà des limites du dépôt

Une source privée peut informer une dérivée publique sans être copiée dedans :

```text
private source evidence
    ↓
identify stable reusable rules
    ↓
remove personal and machine-specific context
    ↓
apply the smallest public change
    ↓
validate behavior, links, and privacy
```

La source reste autoritaire. La dérivée expose uniquement des informations utiles à l'extérieur. Conserver les modifications locales inconnexes dans les deux dépôts et ne jamais utiliser la dérivée publique pour surécrire les faits de la source privée.
