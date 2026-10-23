[English](generalize-repository.md) | [Français](generalize-repository.fr.md) | [简体中文](generalize-repository.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="generalize-repository-prompt"></a>
# Prompts de dépôt généralisés

Extraire un dépôt public réutilisable à partir d'une source privée ou locale tout en préservant le comportement fonctionnel et les limites privées.

<a id="define-before-acting"></a>
## Définir avant d'agir

- but public prévu et public cible ;
- composants nécessaires à ce but ;
- contenu de la source privée qui doit rester inchangé et non publié ;
- validation autonome requise pour la finalisation.

Vérifier la source et la cible avant de modifier l'un des deux dépôts.

<a id="method"></a>
## Méthode

1. Examiner l'implémentation actuelle, les tests, la documentation, la configuration et l'histoire récente du dépôt source.
2. Examiner le dépôt cible et préserver son identité, sa structure et les modifications locales inutiles.
3. Identifier les composants réutilisables et leurs dépendances minimales.
4. Extraire le modèle stable plutôt que de copier des prompts spécifiques à une tâche, des enregistrements privés, des sorties générées ou de l'historique local.
5. Remplacer les chemins spécifiques à une machine et les constantes privées par des entrées documentées ou une configuration uniquement lorsque cela est requis.
6. Préserver le comportement avec la différence cible la plus cohérente possible.
7. Mettre à jour la documentation cible pour correspondre à l'implémentation extraite.
8. Conserver les métadonnées du dépôt source et l'historique `.git/` dans le contenu copié. Préserver l'historique existant de la cible, ou préparer un nouvel historique indépendant uniquement lorsque cela est explicitement demandé.
9. Valider la cible de manière indépendante par rapport à la source privée.

<a id="privacy-and-safety-checks"></a>
## Contrôles de confidentialité et de sécurité

Scanner le contenu candidat et la différence finale pour :

- noms et coordonnées personnelles ;
- identifiants, URLs personnelles et chemins absolus ;
- identifiants, tokens, clés et bases de données locales ;
- données privées de projet, client, employeur ou application ;
- métriques, benchmarks, journaux et artefacts générés ;
- instructions dépendant de la structure locale d'un utilisateur.

Utiliser des exemples fictifs ou anonymisés. Ne pas copier des secrets puis les supprimer dans une autre version ; les exclure avant d'écrire les fichiers publics.

<a id="validation"></a>
## Validation

Exécuter, lorsque pertinent :

- tests ciblés et tests complets pertinents ;
- vérifications statiques, de type et de compilation ;
- test de fumée autonome ;
- vérifications du chemin et des liens de documentation ;
- analyse de secrets et de confidentialité ;
- revue de l'historique `git diff --check` et de la différence finale.

<a id="output"></a>
## Résultat

Rapport :

1. état de la source et de la cible examiné ;
2. modèles réutilisables extraits ;
3. contenu spécifique à la source exclusivement délibérément ;
4. fichiers ajoutés, modifiés ou supprimés dans la cible ;
5. résultats de validation et de confidentialité ;
6. limitations restantes.

Ne pas commiter ni publier sauf si explicitement demandé. Ne pas modifier la source privée sauf si la tâche l'exige séparément.
