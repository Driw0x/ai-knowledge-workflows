[English](synchronize-portfolio.md) | [Français](synchronize-portfolio.fr.md) | [简体中文](synchronize-portfolio.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="portfolio-synchronization-prompt"></a>
# Prompts de synchronisation du portefeuille

Synchroniser le portefeuille public avec la base de connaissances vérifiée actuelle.

<a id="read-before-starting"></a>
## Lire avant de commencer

1. `AGENTS.md`
2. Profil de projet pertinent
3. Enregistrements de compétences pertinents
4. Informations sur la carrière ou le rôle cible
5. Le dépôt actuel du portefeuille

Avant de modifier, inspectez les deux arbres de travail et identifiez les modifications locales inutiles qui doivent être conservées.

<a id="source-of-truth"></a>
## Source de vérité

Considérez la base de connaissances vérifiée comme source de vérité pour :

- l'état des projets ;
- les descriptions des projets ;
- les technologies ;
- les compétences démontrées ;
- les jalons ;
- les résultats mesurables.

Considérez le portefeuille comme la couche de présentation publique.

<a id="objective"></a>
## Objectif

Mettre à jour le portefeuille afin qu'il reflète le profil actuel du candidat sans révéler d'informations privées ou internes inutiles.

Vérification :

- les projets mis en avant ;
- l'état des projets ;
- les descriptions des projets ;
- les technologies ;
- les compétences ;
- les relations projet-compétence ;
- les liens ;
- la position actuelle du rôle ;
- des affirmations obsolètes.

<a id="rules"></a>
## Règles

- Ne pas inventer des affirmations dans le portefeuille.
- Ne pas ajouter de compétences non appuyées par la base de connaissances.
- Ne pas révéler des notes privées, des évaluations internes ou des données d'application.
- Comparer le portefeuille actuel directement avec la source de vérititecture actuelle ; ne pas supposer que la dernière synchronisation est encore valide.
- Conserver la structure actuelle du portefeuille sauf si une modification structurelle est clairement justifiée.
- Privilégier les différences minimales.
- Ne pas publier chaque jalonnement interne.
- Afficher uniquement des informations utiles pour un lecteur externe, tel qu'un recruteur ou un revue technique.
- Maintenir les formulations des projets concises et fondées sur des preuves.
- Assurer que l'état des projets correspond à la source de vérité actuelle.
- Conserver les limites sur les projets mis en avant sauf si explicitement demandé autrement.
- Ne pas remplacer une preuve forte d'une compétence par un projet plus récent mais moins solide.
- Éviter de dupliquer la même compétence dans plusieurs descriptions lorsque cela n'ajoute pas de valeur.
- Conserver les modifications locales inutiles dans le dépôt du portefeuille.
- Valider la construction du portefeuille ou le contrôle équivalent pertinent après modification.

<a id="synchronization-checks"></a>
## Vérifications de synchronisation

<a id="projects"></a>
### Projets

Pour chaque projet du portefeuille, vérifiez :

- le nom ;
- l'état ;
- la description ;
- les technologies ;
- les liens ;
- les preuves clés ;
- si le projet doit encore être mis en avant.

<a id="skills"></a>
### Compétences

Vérifiez que chaque compétence affichée est appuyée par :

- des projets ;
- des études ;
- l'expérience professionnelle ;
- d'autres preuves documentées.

<a id="positioning"></a>
### Positionnement

Vérifiez que le portefeuille reflète toujours les rôles cibles actuels du candidat et ses domaines techniques les plus forts.

<a id="output"></a>
## Sortie

Fournissez :

1. les fichiers qui doivent être modifiés ;
2. l'information obsolète exacte ;
3. des propositions de mises à jour minimales ;
4. des informations intentionnellement non diffusées publiquement ;
5. tout incohérence dans le portefeuille qui doit être examinée manuellement.

Si une modification de fichier est demandée, appliquez uniquement les changements nécessaires.

Ne modifiez pas la base de connaissances privée lors de la synchronisation du portefeuille.
