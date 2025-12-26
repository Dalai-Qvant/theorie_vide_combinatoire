# Guide de contribution

Merci de votre intérêt pour contribuer à la théorie du vide combinatoire ! Ce guide explique comment participer efficacement au projet.

---

## Philosophie du projet

Ce projet est collaboratif et ouvert, mais maintient une rigueur scientifique. Nous cherchons à :

- Consolider, améliorer ou invalider la théorie proposée
- Maintenir un haut niveau de rigueur mathématique et physique
- Rester ouverts à la critique constructive
- Construire une communauté respectueuse et productive

---

## Types de contributions

### 1. Vérification mathématique

**Quoi :** Vérifier la validité des démonstrations, propositions, théorèmes

**Comment :**
1. Ouvrir une [Issue](../../issues/new?template=correction-mathematique.md) en indiquant :
   - Chapitre et numéro de proposition/théorème concerné
   - Nature de l'erreur (erreur de raisonnement, cas non traité, hypothèse manquante, etc.)
   - Proposition de correction si possible

**Exemple :**
```
Titre : [Ch14 - Théorème R] Hypothèse manquante sur la réversibilité

Dans la démonstration du Théorème R (réversibilité des états purs), 
ligne 47, l'argument suppose implicitement que...
```

### 2. Clarifications et améliorations rédactionnelles

**Quoi :** Améliorer la clarté, corriger typos, reformuler passages obscurs

**Comment :**
- Pour petites corrections : Pull Request directe
- Pour reformulations importantes : Discussion via Issue d'abord

### 3. Suggestions théoriques

**Quoi :** Proposer extensions, nouvelles pistes, connexions avec d'autres théories

**Comment :**
1. Ouvrir une [Discussion GitHub](../../discussions)
2. Présenter l'idée de manière structurée
3. Argumenter avec références si possible

### 4. Simulations informatiques

**Quoi :** Développer des codes pour vérifier l'émergence numérique

**Comment :**
1. Consulter les besoins dans le dossier `simulations/`
2. Proposer votre approche via Issue
3. Soumettre le code via Pull Request

### 5. Vulgarisation et pédagogie

**Quoi :** Créer des analogies, schémas, explications simplifiées

**Comment :**
- Ajouter dans les sections "Intuition" des chapitres
- Créer des documents complémentaires dans `docs/pedagogie/`



### 6. Traductions

**Quoi :** Traduction du projet dans différentes langues (anglais minimum) pour permettre des contributeurs non francophones

**Comment :**

- Conserver la structure actuelle, la version française étant celle de référence
- Créer un répertoire pour chaque langue dans lequel les pages seront insérées
- Tenir un registre des pages traduites (avec la dernière date de traduction, pour actualisation en cas de modification d'une page)

---

## Processus de contribution

### Via GitHub Issues (pour les discussions)

1. **Vérifier** qu'une issue similaire n'existe pas déjà
2. **Créer** une nouvelle issue avec le template approprié
3. **Argumenter** clairement et rigoureusement
4. **Participer** à la discussion
5. **Attendre la validation** par les mainteneurs avant intégration

### Via Pull Requests (pour les modifications directes)

1. **Fork** le repository
2. **Créer une branche** : `git checkout -b correction/ch12-typo`
3. **Modifier** les fichiers concernés
4. **Commit** avec message explicite : `git commit -m "Fix: Correction équation 12.3"`
5. **Push** : `git push origin correction/ch12-typo`
6. **Ouvrir une Pull Request** en expliquant les changements

### Via Discord (pour discussions informelles)

- Questions rapides, brainstorming, aide à la compréhension
- Les décisions importantes doivent être reportées sur GitHub

---

## Critères de validation

Une contribution sera intégrée si :

- Elle est rigoureusement argumentée
- Elle améliore la clarté ou la validité du modèle
- Elle respecte le style et la cohérence du document
- Elle a été revue par au moins 2 relecteurs compétents

Les contributions validées seront **explicitement attribuées** au contributeur dans le chapitre concerné.

---

## Standards de rédaction

### Format Markdown

- Utiliser Markdown standard
- Équations en LaTeX : `$E = mc^2$` (inline) ou `$$E = mc^2$$` (bloc)
- Numéroter propositions, théorèmes, équations : `**Proposition 3.1.**`

### Style rédactionnel

- **Clarté** avant tout : expliquer les concepts
- **Rigueur** : justifier chaque affirmation
- **Structure** : utiliser des sous-sections logiques
- **Références** : citer les sources externes

### Conventions mathématiques

- Variables scalaires : italique `$x$`
- Vecteurs : gras `$\mathbf{v}$`
- Opérateurs : roman `$\mathrm{Tr}$`
- Ensembles : calligraphique `$\mathcal{H}$`

---

## Niveaux de relecture

Selon votre expertise, vous pouvez contribuer à différents niveaux :

| Niveau | Expertise requise | Type de contribution |
|--------|-------------------|----------------------|
| **Basique** | Lecture attentive | Typos, clarté, cohérence |
| **Intermédiaire** | Maths/physique niveau M1-M2 | Vérification raisonnements simples |
| **Avancé** | Chercheur ou équivalent | Validation théorèmes, propositions nouvelles |
| **Expert** | Spécialiste du domaine | Critique profonde, extensions théoriques |

**Tous les niveaux sont précieux !** Une typo corrigée évite des malentendus futurs.

---

## Ce qui ne sera pas accepté

- Commentaires non argumentés ("c'est bien", "c'est nul")
- Critiques ad hominem ou irrespectueuses
- Propositions sans justification scientifique
- Spam, publicité, contenu hors-sujet
- Modifications massives non discutées au préalable

---

## Reconnaissance des contributions

Les contributeurs seront reconnus de plusieurs façons :

1. **Mention explicite** dans les chapitres modifiés
2. **Section Contributors** dans le README
3. **Badge de contributeur** GitHub
4. **Co-auteur** sur publications futures si contribution substantielle

---

## Besoin d'aide ?

- **Première fois sur GitHub ?** Voir [GitHub Guide](https://guides.github.com/activities/hello-world/)
- **Question sur le contenu ?** Posez-la sur Discord ou ouvrez une Discussion
- **Problème technique ?** Ouvrez une Issue avec le label `help wanted`

---

## Communication

- **Discord** : [Lien à venir] - Discussions rapides, questions
- **GitHub Issues** : Suivi des corrections et problèmes identifiés
- **GitHub Discussions** : Échanges ouverts, idées nouvelles
- **Email** : [À définir] - Contact direct avec le mainteneur principal

---

## Licence des contributions

En contribuant, vous acceptez que vos modifications soient publiées sous la même licence que le projet : [CC BY-SA 4.0](LICENSE.md).

Vous conservez vos droits d'auteur, mais accordez une licence libre pour utilisation et redistribution.

---

## Merci !

Votre contribution, quelle qu'elle soit, aide à faire progresser ce projet ambitieux. La science se construit collectivement, et chaque pierre apportée compte.

**Bon courage et bonnes contributions !**
