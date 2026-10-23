[English](application-preparation.md) | [Français](application-preparation.fr.md) | [简体中文](application-preparation.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="evaluation-result--application-preparation"></a>
# Résultat d'évaluation - Préparation de candidature

<a id="configuration"></a>
## Configuration

- **Date:** 2026-10-06
- **Cas:** `evals/cases/application-preparation.md`
- **Workflows:** `prompts/application/prepare-application.md` et `prompts/application/adapt-resume.md`
- **Rubrique:** `evals/rubrics/prompt-evaluation-rubric.md`
- **Méthode:** parcours manuel contre le cas synthétique fixé
- **Modèle:** non applicable ; aucune exécution de modèle n'est revendiquée

<a id="rubric-results"></a>
## Résultats de la rubrique

|Critère|Résultat|Observation|
|---|---|---|
|Grounding|Pass|Les affirmations relatives à la prévision, à l'évaluation et aux API correspondent directement aux preuves fournies dans le projet.|
|Suivi des instructions|Pass|Les exigences non prises en charge restent des lacunes et la soumission reste manuelle.|
|Structure de sortie|Pass|Les workflows exigent une cartographie des exigences, une décision de CV, une revue des éléments et des actions suivantes.|
|Affirmations non prises en charge|Pass|Kubernetes, déploiement, opérations en production et discours public ne sont pas ajoutés.|
|Comportement minimal-diff|Pass|Le CV A est réutilisée ou adaptée de manière restreinte ; un nouveau CV nécessite une raison matérielle.|
|Complétude|Pass|Les qualifications requises et préférées, les preuves, les lacunes, le choix de la fiche de candidature et la revue humaine sont couverts.|

<a id="observed-result"></a>
## Résultat observé

L'application des workflows sélectionne le CV A comme base la plus proche fondée sur des preuves. Le projet Alpha soutient la prévision et l'évaluation. Le projet Beta soutient une API testée, pas un déploiement. Kubernetes et les opérations en production restent non documentés. Le candidat revient sur tous les éléments et soumet manuellement.

<a id="gaps-and-limitations"></a>
## Lacunes et limites

- Ceci est un parcours manuel déterministe, pas une évaluation de modèle mesurée.
- Il ne teste ni la rendu de documents ni un portfolio de fiches de candidature complexe.
- Aucune exécution répétée ni comparaison de modèles n'a été effectuée.

<a id="conclusion"></a>
## Conclusion

Les workflows passent ce cas qualitatif. Ils conservent le grounding, les modifications minimales de la fiche de candidature, les lacunes explicites et le contrôle humain, sans revendiquer une performance mesurée d'un modèle.
