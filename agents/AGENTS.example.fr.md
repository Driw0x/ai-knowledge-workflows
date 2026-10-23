[English](AGENTS.example.md) | [Français](AGENTS.example.fr.md) | [简体中文](AGENTS.example.zh-CN.md)

[README du projet](../README.fr.md)

<a id="agent-instructions"></a>
# Instructions de l'agent

Ce fichier définit des règles opérationnelles réutilisables pour les agents IA utilisant ce dépôt.

Copiez-le vers `AGENTS.md` avant de l'adapter à votre propre environnement.

<a id="core-rules"></a>
## Règles fondamentales

1. Lisez les fichiers source pertinents avant d'agir.
2. Avant une modification substantielle, définissez les critères de succès, ce qui doit rester inchangé, et les vérifications nécessaires.
3. Considérez les fichiers de connaissances fournis comme la source de vérité pour les informations spécifiques à l'utilisateur.
4. Ne pas inventer des compétences, des expériences, des résultats de projets, des détails d'implémentation ou des préférences.
5. Faites une distinction claire entre :
   - des faits vérifiés ;
   - des analyses ;
   - des recommandations ;
   - des informations manquantes.
6. Privilégiez les sources primaires lors de la recherche d'informations actuelles.
7. Conservez les liens ou références de source pour les affirmations à caractère temporel.
8. Diagnostiquez les échecs avant de les corriger : reproduisez ou tracez l'échec, identifiez sa cause, puis modifiez la couche responsable.
9. Privilégiez l'implémentation la plus petite satisfaisant le besoin vérifié. Évitez les abstractions spéculatives et les nouvelles dépendances.
10. Ne pas modifier les fichiers de connaissances stables sauf si la tâche l'exige explicitement.
11. Conservez les rapports générés séparés des fichiers de vérité source.
12. Conservez le contenu utile existant lors de la mise à jour de la documentation.
13. Privilégiez les modifications minimales par rapport aux réécritures générales.
14. Ne jamais exposer des secrets, des données personnelles, des chemins privés ou des contextes privés dans les sorties publiques.
15. Lorsqu'une affirmation ne peut pas être vérifiée, indiquez la limitation au lieu de deviner.
16. Faites une distinction entre les travaux mis en œuvre, testés, validés, expérimentaux, planifiés, abandonnés et remplacés lorsqu'ils sont pertinents.
17. Ne pas affirmer la finalisation avant d'avoir exécuté les tests pertinents, les vérifications statiques, la compilation ou le test de fumée.

<a id="evidence-policy"></a>
## Politique de preuve

Une compétence, une fonctionnalité ou un résultat est considéré comme pris en charge uniquement s'il existe une preuve concrète telle que :

- du code source ;
- des documents du dépôt ;
- des tests ;
- des résultats de benchmark ;
- des rapports de projet ;
- des travaux académiques ;
- des expériences professionnelles ;
- des commandes reproductibles ;
- des sources vérifiables en dehors du système.

Le nom d'une technologie apparaissant dans un fichier n'est pas suffisant seul pour prouver une compétence.

L'absence de preuve sur une compétence signifie « non documenté », pas preuve que la personne manque de cette compétence.

<a id="file-safety"></a>
## Sécurité des fichiers

Les emplacements suivants sont par défaut privés :

```text
AGENTS.md
local/
private/
```

Ne pas déplacer du contenu de ces emplacements vers des fichiers publics sauf si explicitement demandé et revu pour anonymisation.

Lorsque vous dérivez un dépôt ou un document public à partir de sources privées, extrayez le modèle réutilisable plutôt que de copier le contenu source. Revoyez la différence résultante pour les données personnelles, les identifiants, les chemins absolus et les détails de projets privés.

<a id="career-workflow"></a>
## Workflow professionnel

Avant la recherche professionnelle, lisez :

```text
local/career-profile.md
```

Pour chaque opportunité :

- vérifiez qu'elle est actuellement accessible ;
- vérifier qu'il correspond au type de contrat requis ;
- vérifier la compatibilité géographique ;
- vérifier le niveau académique attendu ;
- extraire les exigences techniques et non techniques importantes ;
- comparer les exigences uniquement aux preuves disponibles pour les candidats pris en charge ;
- identifier les projets les plus solides en faveur de l'argumentation ;
- identifier les preuves manquantes ou faibles ;
- éviter d'inclure des correspondances faibles simplement pour augmenter le nombre de résultats.

Utiliser :

```text
templates/internship-research-report.md
```

pour la structure de la sortie.

<a id="project-workflow"></a>
## Workflow du projet

Lors de l'analyse d'un projet :

- examiner l'implémentation avant de se fier à la documentation ;
- distinguer l'implémentation actuelle des éléments de la roadmap ;
- distinguer les approches actives des expérimentations abandonnées ;
- ne pas attribuer des technologies qui ne sont pas effectivement utilisées ;
- garder les preuves liées à l'état du projet fondées sur des données ;
- privilégier les preu- uves provenant de dépôts plutôt que des formulations marketing.

<a id="knowledge-workflow"></a>
## Workflow de la connaissance

Lors de la mise à jour d'une base de connaissances :

- extraire des connaissances durables ;
- éviter de stocker des bruits de débogage transitoires sauf s'ils enseignent quelque chose d'usable ;
- réduire la duplication ;
- préserver les détails techniques utiles ;
- créer des liens entre concepts liés lorsqu'il est approprié ;
- ne pas fabriquer de certitude.

<a id="documentation-workflow"></a>
## Workflow de la documentation

Lors de la mise à jour de la documentation :

- préserver le contenu existant correct ;
- faire la modification la plus petite utile ;
- préférer les ajouts aux réécritures inutiles ;
- assurer que le comportement documenté correspond à l'implémentation actuelle ;
- séparer clairement les travaux futurs de la fonctionnalité actuelle.

<a id="failure-workflow"></a>
## Workflow des échecs

Lors de la correction d'une erreur ou d'un flux défaillant :

1. reproduire ou suivre l'échec avec des données concrètes ;
2. identifier la cause racine et les appels affectés ;
3. appliquer le plus petit correctif au niveau responsable ;
4. ajouter ou mettre à jour un contrôle de régression ciblé ;
5. exécuter les vérifications générales pertinentes et un test de fumée réel lorsque c'est pratique.
