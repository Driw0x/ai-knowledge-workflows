[English](adapt-resume.md) | [Français](adapt-resume.fr.md) | [简体中文](adapt-resume.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="adapt-resume-prompt"></a>
# Prompt d’adaptation du CV

Choisir et préparer le CV le plus approprié pour une seule annonce d'emploi, en utilisant uniquement des preuves de candidat vérifiées.

<a id="read-before-starting"></a>
## Lire avant de commencer

1. `AGENTS.md`
2. L'annonce complète d'emploi
3. Preuves de candidat vérifiées
4. Variantes de CV existantes et leur contenu réel
5. Contraintes de format et de longueur du CV

<a id="decision"></a>
## Décision

Choisir exactement une action :

- **REUSE** - un CV existant s'adapte suffisamment sans modifications substantielles.
- **ADAPT** - un CV existant est une base appropriée, mais l'accent, l'ordre ou le langage doivent être modifiés.
- **CREATE** - aucun CV existant ne fournit une base suffisamment appropriée.

Privilégier `REUSE`, puis `ADAPT`, lorsqu'ils représentent fidèlement les preuves. Ne créez pas une nouvelle variante simplement parce que le langage pourrait être différent.

<a id="rules"></a>
## Règles

- Comparer les responsabilités et exigences de l'emploi avec le contenu du CV, et non avec les noms de fichiers ou les étiquettes de variantes.
- Ne pas inventer une compétence, une expérience, un rôle de projet, un résultat, une date ou une métrique.
- Ne pas transformer une expérience liée en expérience exacte.
- Préserver le sens factuel lors de la réduction ou de la reformulation des preuves.
- Prioriser les preuves pertinentes et supprimer uniquement le contenu de moindre valeur nécessaire pour respecter les contraintes de format.
- Conserver un langage lisible par un recruteur et suffisamment précis pour être vérifié.
- Enregistrer les exigences importantes non soutenues plutôt que de les insérer dans le CV.
- Préserver le CV source ou le modèle. Écrire la version adaptée dans un document cible séparé lorsqu'une modification est requise.

<a id="output"></a>
## Sortie

Fournir :

1. `REUSE`, `ADAPT` ou `CREATE`;
2. le CV de base sélectionné, s'il existe;
3. raisonnement fondé sur les preuves;
4. contenu à souligner, à réorganiser, à réécrire ou à omettre;
5. des lacunes importantes qui ne doivent pas être affirmées;
6. le fichier cible, lorsqu'un nouveau document est demandé;
7. les vérifications effectuées sur la précision factuelle, le format et la lisibilité.

Le candidat examine le CV final avant utilisation.
