[English](repository-audit.md) | [Français](repository-audit.fr.md) | [简体中文](repository-audit.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="repository-documentation-audit-prompt"></a>
# Promp d'audit de la documentation du dépôt

Audit de la documentation du dépôt pour véracité, complétude et cohérence.

<a id="compare"></a>
## Comparer

Comparer la documentation avec :

- le code source ;
- la configuration ;
- les interfaces de ligne de commande ;
- les tests ;
- la structure des dossiers ;
- l'état actuel du projet.

Examiner la branche actuelle et `HEAD`. Privilégier le code exécuté et les tests par rapport à la documentation obsolète lors de conflits. Noter les différences pertinentes non commitées ou liées à l'état distant au lieu de les combiner dans un état global du projet.

<a id="identify"></a>
## Identifier

- des sections obsolètes du README ;
- des modules importants non documentés ;
- des commandes qui ne fonctionnent plus ;
- des étapes de configuration manquantes ;
- des documents dupliqués ;
- des éléments de roadmap présentés comme réalisés ;
- des termes incohérents ;
- des limitations non documentées ;
- contexte de benchmark manquant ;
- liens manquants entre les documents associés.

<a id="prioritization"></a>
## Priorisation

Classer les résultats comme :

- **Critique**
- **Important**
- **Mineur**

<a id="rules"></a>
## Règles

- Ne pas réécrire la documentation lors de l'audit sauf si explicitement demandé.
- Privilégier la correction par rapport à la complétude.
- Ne pas exiger de documentation pour des détails internes triviaux.
- Se concentrer sur les informations qui affectent les utilisateurs, les contributeurs, la reproductibilité ou la compréhension du projet.
- Définir la portée de l'audit et les critères de succès avant l'inspection.

<a id="output"></a>
## Sortie

Produire une table contenant :

- problème ;
- fichier concerné ;
- preuve ;
- modification recommandée ;
- priorité.
