[English](prompt-evaluation-rubric.md) | [Français](prompt-evaluation-rubric.fr.md) | [简体中文](prompt-evaluation-rubric.zh-CN.md)

[README du projet](../../README.fr.md)

<a id="prompt-evaluation-rubric"></a>
# Rubrique d'évaluation de prompt

Utilisez cette rubrique pour évaluer les sorties produites par les workflows du dépôt.

Chaque critère est noté sur une échelle de **1 à 5**.

<a id="1-grounding"></a>
## 1. Ancrage dans les sources

Mesure si les affirmations sont appuyées par les preuves fournies.

<a id="score"></a>
### Note

- **5** - toutes les affirmations importantes sont appuyées par des preuves disponibles
- **4** - principalement appuyées, avec seulement une interprétation mineure non justifiée
- **3** - certaines affirmations non justifiées ou faiblement appuyées
- **2** - plusieurs affirmations importantes manquent de preuves
- **1** - la sortie repose fortement sur des informations inventées ou non justifiées

<a id="2-instruction-following"></a>
## 2. Respect des instructions

Mesure le respect des contraintes explicites de la tâche.

Exemples :

- lire les fichiers requis ;
- préserver le contenu existant ;
- éviter les modifications inutiles ;
- utiliser les classifications demandées ;
- respecter les règles de confidentialité.

<a id="score-1"></a>
### Note

- **5** - respecte toutes les instructions importantes
- **4** - une instruction mineure manquée
- **3** - respect partiel des instructions
- **2** - manque plusieurs contraintes importantes
- **1** - ignore largement les instructions de la tâche

<a id="3-output-structure"></a>
## 3. Structure de la sortie

Mesure si la sortie respecte le format demandé.

<a id="score-2"></a>
### Note

- **5** - complète et correctement structurée
- **4** - structure correcte avec quelques omissions mineures
- **3** - structure identifiable mais incohérente
- **2** - plusieurs sections requises sont manquantes
- **1** - la sortie ne suit pas la structure demandée

<a id="4-unsupported-claims"></a>
## 4. Affirmations non justifiées

Mesure l'évitement des hallucinations.

Un score plus élevé signifie moins d'affirmations non justifiées.

<a id="score-3"></a>
### Note

- **5** - aucune affirmation non justifiée
- **4** - une déclaration mineure non justifiée
- **3** - plusieurs hypothèses faibles
- **2** - des affirmations importantes non justifiées
- **1** - hallucination ou fabrication substantielle

<a id="5-minimal-diff-behavior"></a>
## 5. Comportement minimal-diff

Mesure si le workflow préserve le contenu existant valide lorsqu'une tâche d'édition exige des modifications minimales.

<a id="score-4"></a>
### Note

- **5** - seulement les modifications nécessaires sont apportées
- **4** - quelques modifications inutiles, aucune perte importante
- **3** - réécriture inutile remarquable
- **2** - réécriture importante malgré des modifications limitées requises
- **1** - réécriture destructive ou inappropriée

Pour les tâches non d'édition, indiquez ce critère comme **N/A**.

<a id="6-completeness"></a>
## 6. Complétude

Mesure si la réponse couvre toutes les parties importantes de la tâche.

<a id="score-5"></a>
### Note

- **5** - toutes les exigences importantes sont traitées
- **4** - une omission mineure
- **3** - utile mais incomplète
- **2** - plusieurs omissions importantes
- **1** - plusieurs parties importantes de la tâche sont absentes

<a id="scoring"></a>
## Évaluation

Score standard maximum :

```text
30
```

Si `Minimal-diff behavior` n'est pas applicable, calculez le résultat à partir de :

```text
25
```

<a id="interpretation"></a>
## Interprétation

Pour une évaluation de 30 points :

- **27–30** - excellent
- **23–26** - fort
- **18–22** - acceptable mais doit être amélioré
- **12–17** - faible
- **6–11** - évaluation échouée

Ne vous fiez pas uniquement au score total.

Un mauvais ancrage dans les sources ou une fausse interprétation peut invalider un résultat autrement bien noté.

<a id="regression-rule"></a>
## Règle de régression

Une nouvelle version de prompt doit être revue si :

- le score total diminue de manière importante ;
- l’ancrage dans les sources diminue ;
- les affirmations non justifiées augmentent ;
- une contrainte explicite respectée auparavant est maintenant ignorée ;
- le comportement minimal-diff s'aggrave.

Les régressions critiques doivent bloquer la nouvelle version de prompt jusqu'à revue.
