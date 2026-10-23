[English](audit-knowledge.md) | [Français](audit-knowledge.fr.md) | [简体中文](audit-knowledge.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="audit-knowledge-base-prompt"></a>
# Prompts de base de connaissances d'audit

Vérifier la base de connaissances pour sa qualité, sa cohérence et sa maintenabilité.

<a id="check-for"></a>
## Vérifier pour

- des notes orphelines;
- du contenu dupliqué;
- des termes incohérents;
- des affirmations non justifiées;
- un état de projet obsolète;
- des liens périmés;
- des liens manquants entre les éléments;
- des preuves faibles pour les compétences déclarées;
- des connaissances sur des projets stockées dans le mauvais endroit;
- des résultats précis dupliqués dans plusieurs notes de concept;
- des informations transitoires qui ne devraient pas être conservées;
- des concepts importants qui sont fréquemment référencés mais non documentés.

<a id="prioritization"></a>
## Priorisation

Classer les résultats en :

- **Élevé** - susceptible de tromper les raisonnements futurs
- **Moyen** - réduit la clarté ou la maintenabilité
- **Faible** - nettoyage ou amélioration de la présentation

<a id="rules"></a>
## Règles

- Ne modifiez pas les fichiers sauf si explicitement demandé.
- Ne proposez pas de réorganisation simplement pour une cohérence esthétique.
- Préservez le contexte historique utile.
- Identifiez le flux de travail ou la note responsable de chaque correction recommandée.
- Privilégiez les corrections à fort impact par rapport aux nettoyages généraux.

<a id="output"></a>
## Sortie

Produire un rapport d'audit priorisé contenant :

- l'incident ;
- le fichier ou zone concerné ;
- pourquoi cela importe ;
- l'action recommandée ;
- la priorité.
