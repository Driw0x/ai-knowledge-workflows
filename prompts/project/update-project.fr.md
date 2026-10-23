[English](update-project.md) | [Français](update-project.fr.md) | [简体中文](update-project.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="update-project-prompt"></a>
# Mettre à jour le prompt du projet

Examinez le dépôt actuel du projet et comparez-le avec l'entrée de la base de connaissances existante.

<a id="objective"></a>
## Objectif

Mettez à jour uniquement les informations qui ont subi une modification substantielle.

Avant de modifier, définissez la mise à jour attendue, quel contenu valide doit rester, et les vérifications nécessaires pour valider le résultat.

Revue :

- état du projet ;
- points de référence ;
- fonctionnalités mises en œuvre ;
- architecture ou méthodes ;
- technologies ;
- compétences démontrées ;
- résultats de benchmark ou d'évaluation ;
- limites ;
- approches abandonnées ;
- étapes suivantes.

<a id="rules"></a>
## Règles

- Conservez les informations valides existantes.
- Préférez des différences minimales.
- Préférez les ajouts plutôt que des réécritures inutiles.
- Supprimez ou corrigez les affirmations qui ne sont plus vraies.
- Ne documentez pas les éléments de roadmap comme réalisés.
- Ne pas inférer des compétences ou des technologies.
- Utiliser les preuves du dépôt comme source principale.
- Inspectez la branche actuelle et `HEAD`. Distinquez l'implémentation actuelle de l'état distant, l'historique Git normal, et les travaux locaux ou en point d'arrêt abandonnés lorsque pertinent.
- Traitez les tests et les benchmarks comme des preuves uniquement dans leur portée réelle. Indiquez si les résultats ont été reproduits lors de la mise à jour ou seulement documentés.
- Distinquez les travaux mis en œuvre, testés, validés, expérimentaux, planifiés, abandonnés et remplacés.
- Préservez le statut d'un résultat important (réproduit, documenté, historique ou remplacé).
- Conservez uniquement les informations historiques lorsque celles-ci apportent un contexte utile au projet.
- Marquez clairement les travaux mis en pause, abandonnés, expérimentaux ou terminés lorsque cela est pertinent.
- Indiquez la propreté du dépôt lorsque des modifications locales peuvent affecter l'état observé.

<a id="output"></a>
## Sortie

Mettez à jour le registre existant de manière in situ.

En fin de compte, fournissez un bref résumé de :

- ce qui a changé ;
- ce qui a été conservé intentionnellement ;
- tout incertitude qui reste.
