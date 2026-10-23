[English](consolidate-knowledge.md) | [Français](consolidate-knowledge.fr.md) | [简体中文](consolidate-knowledge.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="consolidate-knowledge-prompt"></a>
# Prompt d'approfondissement des connaissances

Examinez la zone demandée dans la base de connaissances et consolidez les informations redondantes ou fragmentées.

<a id="objective"></a>
## Objectif

Améliorer la structure sans perdre les détails techniques utiles.

Identifier :

- des notes dupliquées ;
- des explications fragmentées ;
- des termes incohérents ;
- des informations périmées ;
- des concepts liés faiblement entre eux ;
- des fichiers inutiles ;
- des notes à fusionner ;
- des notes à garder séparées.

<a id="rules"></a>
## Règles

- Privilégiez l'amélioration d'une note existante plutôt que la création d'une duplication.
- Conservez les exemples utiles et les détails techniques.
- Ne fusionnez pas des concepts simplement parce qu'ils sont liés.
- Affectez une seule note responsable à chaque concept ou résultat précis.
- Conservez les faits spécifiques à un projet, les métriques complètes et les expériences historiques dans leurs enregistrements d'origine ; faites les liens à ces enregistrements au lieu de les copier à travers les concepts.
- Maintenez les liens existants valides.
- Conservez l'origine et le statut de preuve lors du déplacement ou de la condensation des informations.
- Évitez une réorganisation à grande échelle sauf s'il y a un bénéfice clair.
- Privilégiez un changement structurel minimal.

<a id="output"></a>
## Sortie

Proposez :

1. des fusions proposées ;
2. des mises à jour proposées ;
3. des suppressions ou archivages proposés ;
4. des liens croisés à ajouter ;
5. des termes à standardiser.

Si des modifications de fichiers sont requises, appliquez l'ensemble minimal utile de changements.
