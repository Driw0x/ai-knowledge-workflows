[English](internship-research.md) | [Français](internship-research.fr.md) | [简体中文](internship-research.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="internship-research-prompt"></a>
# Prompts de recherche pour stage

Effectuer une recherche actuelle sur des opportunités de stage pour les derniers ans correspondant au profil du candidat.

<a id="read-before-starting"></a>
## Lire avant de commencer

1. `AGENTS.md`
2. `local/career-profile.md`
3. `templates/internship-research-report.md`
4. Lire les fichiers précédents `local/research/` uniquement lorsqu'ils sont utiles pour la détection de doublons ou le suivi des modifications

<a id="objective"></a>
## Objectif

Identifier des opportunités de stage actuellement accessibles qui correspondent véritablement au profil et aux contraintes du candidat.

Pour les offres sélectionnées, déterminer :

- pourquoi chaque offre est pertinente ;
- les compétences et technologies principales requises ;
- quels exigences sont déjà soutenus par les preuves du candidat ;
- quels exigences sont faiblement démontrés ;
- quels exigences sont manquants ;
- quels projets existants fournissent la preuve la plus forte ;
- quels gaps de compétences se répètent dans plusieurs offres ;
- quelles opportunités devraient être prioritaires ;
- quelles sont les compétences que le candidat devrait renforcer.

<a id="research-rules"></a>
## Règles de recherche

- Rechercher sur le web des offres actuelles.
- Respecter les contraintes géographiques, de poste, de niveau d'études, de durée et de timing du profil du candidat.
- Préférer les pages de carrière des employeurs originaux lorsqu'elles sont disponibles.
- Ne pas considérer des offres inaccessibles ou clairement expirées comme actives.
- Évaluer les responsabilités réelles et les exigences, et non uniquement le titre du poste.
- Rechercher dans des familles de postes compatibles et des domaines adjacents définis par le profil du candidat, au lieu de se baser sur un seul titre ou mot-clé.
- Considérez le domaine d'application séparément de l'adaptation technique.
- Éliminez les offres identiques provenant de différentes sources, en utilisant l'identifiant officiel de demande ou l'URL d'application lorsque disponible.
- Distinguez une offre accessible d'une position confirmée comme toujours ouverte.
- Enregistrez uniquement les dates de publication vérifiées. Marquez les dates déduites du langage relatif comme « déduites ».
- Conservez l'identifiant officiel de demande lorsque disponible et privilégiez l'URL officielle de l'employeur ou du système de gestion des candidatures par rapport aux réflexions.
- Ne pas inférer des compétences des candidats qui ne sont pas soutenues par les fichiers fournis.
- Ne pas inclure des offres faiblement liées simplement pour augmenter le nombre de résultats.
- Conservez les URLs ou références des sources nécessaires à la vérification des offres sélectionnées.
- Séparez les faits de l'analyse.
- Exprimez explicitement l'incertitude.

<a id="discovery-and-selection-boundary"></a>
## Limite de découverte et de sélection

Traitez la découverte et la préparation de l'application comme des étapes séparées. Ce workflow peut classer et rapporter des opportunités, mais il ne doit pas créer de dossiers d'application, adapter des CV ou préparer des documents d'application sans une sélection explicite de la part de l'utilisateur.

Attribuez à chaque offre présélectionnée un identifiant unique dans le rapport (`O01`, `O02`, etc.) et répétez-le dans sa fiche. L'utilisateur peut ainsi sélectionner les offres par identifiant.

<a id="fit-evaluation"></a>
## Évaluation de l'adaptation

Utilisez des niveaux qualitatifs :

- **Fort**
- **Bon**
- **Partiel**
- **Faible**

Évitez une précision numérique artificielle sauf si une méthode de notation a été explicitement définie.

<a id="output"></a>
## Sortie

Utilisez :

```text
templates/internship-research-report.md
```

Enregistrez le rapport personnel à :

```text
local/research/YYYY-MM-DD-internships.md
```

Si ce nom de fichier existe déjà, utiliser le prochain suffixe disponible (`-2`, `-3`, etc.). Ne pas écraser un rapport précédent sauf demande explicite de correction.

Ne pas modifier le profil du candidat ou les modèles publics sauf si une demande explicite est formulée.
