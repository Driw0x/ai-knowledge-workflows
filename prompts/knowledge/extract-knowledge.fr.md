[English](extract-knowledge.md) | [Français](extract-knowledge.fr.md) | [简体中文](extract-knowledge.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="extract-knowledge-prompt"></a>
# Prompts d'extraction de connaissances

Examinez le matériel source fourni et extrayez des connaissances durables utiles pour des raisonnements futurs.

<a id="possible-sources"></a>
## Sources possibles

- code du dépôt ;
- documentation ;
- notes de recherche ;
- rapports techniques ;
- journal d'expériences ;
- discussions sur un projet ;
- références externes.

<a id="extract"></a>
## Extraction

Identification :

- concepts ;
- méthodes ;
- algorithmes ;
- outils ;
- modèles architecturaux ;
- leçons d'implémentation ;
- contraintes réutilisables ;
- connaissances spécifiques au projet ;
- compétences démontrées.

<a id="rules"></a>
## Règles

- Extrait uniquement les informations appuyées par la source.
- Ne copiez pas l'historique de débogage transitif sauf s'il enseigne une leçon réutilisable.
- Ne dupliquez pas des informations déjà présentes dans la base de connaissances.
- Privilégiez des formulations concises et durables.
- Préservez les nuances techniques importantes.
- Séparez les connaissances générales des faits spécifiques au projet.
- Privilégiez une note canonique responsable pour chaque concept réutilisable. Conservez les résultats détaillés et l'histoire du projet dans leurs enregistrements d'origine.
- Préservez la provenance lorsque cela influence l'interprétation ou la force de la preuve.
- Ajoutez des liens vers des notes existantes lorsque cela est approprié.

<a id="output"></a>
## Sortie

Proposez :

- des notes à créer ;
- des notes existantes à mettre à jour ;
- des liens à ajouter ;
- des informations qui ne devraient pas être stockées.

Pour chaque candidat, nommez la source d'appui, la note responsable, le niveau maximal de preuve, et si elle doit être créée, consolidée, reportée ou ignorée.

Ne modifiez pas les fichiers sauf s'ils sont explicitement demandés.
