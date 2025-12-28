# Chapitre 9 — Univers émergents et sélection d'histoires

---

## Introduction

Les chapitres précédents ont établi :
- Un espace d'histoires $\Omega_B$ avec une mesure de sélection $\mu_\beta$
- Des taux de nucléation $\lambda_{[\mathcal{G}]}$ pour les germes supercritiques
- Des phases macroscopiques (ergodiques ou mélanges)

Ce chapitre franchit une étape conceptuelle décisive : il définit ce qu'est un univers dans ce formalisme, et comment les univers sont distribués statistiquement.

> **Point clé :** Un univers n'est pas une histoire entière. C'est le futur causal d'une nucléation — une sous-structure infinie au sein d'une histoire donnée. Une même histoire peut contenir zéro, un, ou plusieurs univers.

Deux points de vue complémentaires émergent :
1. **Point de vue global (méta-vide)** : L'espace $(\Omega_B, \mu_\beta)$ comme "multivers combinatoire"
2. **Point de vue interne** : Un univers comme sous-structure causale observable "de l'intérieur"

---

## Partie I : Noyau ontologique

### 9.I.α — Principe d'univers comme futur causal

> **Un univers est le futur causal d'un événement de nucléation.**

Un "univers microscopique" est défini par :
- Une histoire $\omega \in \Omega_B$
- Un événement de nucléation $e_n$ dans cette histoire
- Le domaine causal $\mathcal{U}(e_n, \omega)$ — l'ensemble de tous les événements causalement influencés par le germe créé en $e_n$

L'univers n'est pas l'histoire entière, mais une sous-histoire enracinée dans une nucléation.

---

### 9.I.β — Principe d'infinitude

> **Un univers cosmologique est un domaine causal infini.**

Pour qu'un domaine causal mérite le nom d'"univers", il doit contenir un nombre infini d'événements. C'est précisément ce qui distingue les germes supercritiques (croissance illimitée) des fluctuations subcritiques (retour au vide).

Les univers finis sont des "proto-univers" avortés — ils n'ont pas de structure à grande échelle.

---

### 9.I.γ — Principe de coarse-graining d'univers

> **Les univers microscopiques se regroupent en types par équivalence macroscopique.**

Deux univers microscopiques qui partagent les mêmes propriétés à grande échelle (dimension effective, géométrie, contenu informationnel...) sont du même type.

Le coarse-graining $\Gamma^{\mathrm{univ}}$ définit cette équivalence. Le "type d'univers" est l'analogue, pour les univers, du "macrostate" pour les histoires.

---

### 9.I.δ — Principe de distribution des univers

> **La mesure de sélection $\mu_\beta$ induit une distribution sur les types d'univers.**

En conditionnant $\mu_\beta$ sur l'ensemble des nucléations, on obtient une mesure $\Pi^{\mathrm{univ}}$ sur l'espace des types d'univers. Cette distribution répond à la question : "Si on choisit une nucléation au hasard, quel type d'univers obtient-on ?"

---

### 9.I.ε — Principe d'émergence

> **Un type d'univers est "émergent" s'il a une probabilité non nulle.**

Les types d'univers avec $\Pi^{\mathrm{univ}}(\{u\}) > 0$ sont effectivement réalisés dans le vide. Les autres sont possibles (niveau I) mais non typiques (niveau II).

La physique observable correspond aux types d'univers émergents — ceux qui "existent" statistiquement.

---

### 9.I.ζ — Principe de dualité histoire/univers

> **On peut voir les histoires du point de vue des univers, et vice versa.**

Deux perspectives duales :
- **Histoires → Univers** : Chaque histoire contient un certain nombre d'univers
- **Univers → Histoires** : Choisir un univers sélectionne certaines histoires (celles qui le contiennent)

Cette dualité est formalisée par la mesure "size-biased" $\hat{\mu}_\beta^A$.

---

## Partie II : Choix de représentation

### 9.1 — Deux points de vue conceptuels

#### 9.1.1 — Point de vue global (méta-vide)

L'espace $(\Omega_B, \mu_\beta)$ représente un multivers combinatoire :
- Toutes les histoires admissibles "existent" comme possibilités
- Elles sont pondérées par $\mu_\beta$
- Aucune histoire n'est "la vraie" — la mesure encode la typicalité

#### 9.1.2 — Point de vue interne

Un univers est une sous-structure au sein d'une histoire :
- Il émerge à partir d'une nucléation
- Il a sa propre dynamique causale interne
- Un agent interne (au sens informationnel, formalisé plus tard) ne voit que son univers, pas l'histoire globale

**Objectif du chapitre :** Formaliser le passage entre ces deux points de vue.

---

### 9.2 — Univers microscopiques

#### 9.2.1 — Rappels sur les nucléations

Pour un germe supercritique $[\mathcal{G}]$ :
- $\mathsf{Nuc}_n([\mathcal{G}])$ : ensemble des histoires où $e_n$ est une nucléation de type $[\mathcal{G}]$
- $X_n^{[\mathcal{G}]}(\omega) = 1$ ssi $e_n$ est une nucléation de type $[\mathcal{G}]$

L'ensemble des indices de nucléation dans une histoire :

$$\mathsf{Nuc}(\omega) := \{n \in \mathbb{N} : \exists [\mathcal{G}], X_n^{[\mathcal{G}]}(\omega) = 1\}$$

#### 9.2.2 — Domaine causal d'un germe

**Définition 9.1 (Domaine causal).** Pour une histoire $\omega$ et un événement $e_n$ correspondant à une nucléation (au sens du Chapitre 7) de type $[\mathcal{G}]$, on note
$\mathrm{Germ}(e_n,\omega)$ le support du germe effectivement créé (par exemple le sous-hypergraphe induit par $\mathrm{New}(e_n)$, éventuellement complété par l’interface conservée si cela est utile). On ne retient que sa classe d’isomorphisme.

Le domaine causal associé est alors défini comme le futur causal de ce support :

$$\mathcal{U}(e_n, \omega) := \mathcal{F}(\mathrm{Germ}(e_n,\omega), \omega)$$

où $\mathcal{F}(X,\omega)$ désigne l’ensemble des événements (et régions du substrat) causalement influencés par $X$ via la relation de précédence $\prec$ (clôture transitive de la dépendance immédiate $\to$).

**Remarque (nucléation réussie vs avortée).** Si l’on adopte la convention que "nucléation" signifie *démarrage supercritique* (croissance non bornée), alors l’infinitude ci-dessous est vraie par définition. Si l’on souhaite distinguer des proto-nucléations (tentatives locales) des nucléations supercritiques, il suffit de réserver le terme "nucléation" au second cas.

**Propriétés (sous hypothèses de localité et localement fini).**
- $\mathcal{U}(e_n, \omega)$ est connexe (pour la connexité induite par le graphe causal des événements, ou par le graphe d’interaction restreint).
- Si $e_n$ est une nucléation supercritique, alors $|\mathcal{U}(e_n, \omega)| = \infty$.

#### 9.2.3 — Définition d'un univers microscopique

**Définition 9.2 (Univers microscopique).** Pour $\omega \in \Omega_B$ et $n \in \mathsf{Nuc}(\omega)$, l'univers microscopique associé est :

$$U_n(\omega) := (\omega, e_n)$$

muni de sa dynamique restreinte au domaine causal $\mathcal{U}(e_n, \omega)$ :
- Événements : restriction de $E(\omega)$ au futur causal de $e_n$
- Configurations : restrictions des $H_k$ à $\mathcal{U}(e_n, \omega)$

**Espace des univers microscopiques :**

$$\mathcal{U}_{\mathrm{mic}} := \{U_n(\omega) : \omega \in \Omega_B, n \in \mathsf{Nuc}(\omega)\}$$

#### 9.2.4 — Condition d'infinitude

Pour les considérations "cosmologiques", on se restreint aux univers dont le domaine causal est infini :

$$\mathcal{U}_{\mathrm{mic}}^\infty := \{U_n(\omega) \in \mathcal{U}_{\mathrm{mic}} : |\mathcal{U}(e_n, \omega)| = \infty\}$$

Par définition des germes supercritiques, tous les $U_n(\omega)$ avec $n \in \mathsf{Nuc}(\omega)$ satisfont cette condition dans des histoires où le budget permet la croissance.

---

### 9.3 — Types d'univers (réalisation de 9.I.γ)

#### 9.3.1 — Espace des types

**Définition 9.3 (Coarse-graining d'univers).** Un coarse-graining d'univers est une application mesurable :

$$\Gamma^{\mathrm{univ}} : \mathcal{U}_{\mathrm{mic}} \longrightarrow \mathcal{M}_{\mathrm{univ}}$$

où $(\mathcal{M}_{\mathrm{univ}}, \mathcal{M}_\sigma)$ est l'espace des types d'univers.

**Propriétés requises :**
- Mesurabilité (compatible avec $\Sigma_B$)
- Invariance par isomorphismes causaux pertinents

Les motifs étant des régions finies, $\Gamma^{\mathrm{univ}}$ peut être choisi de manière à prendre ses valeurs dans un espace mesurable standard (discret si l’on ne retient que des invariants discrets, ou standard borélien sinon). La mesurabilité de $\Gamma^{\mathrm{univ}}$ assure alors celle des ensembles de types, sans hypothèse de dénombrabilité.

#### 9.3.2 — Types d'univers

**Définition 9.4 (Type d'univers).** Un type d'univers est un élément $u \in \mathcal{M}_{\mathrm{univ}}$.

Deux univers microscopiques $U$ et $U'$ sont du même type si :

$$\Gamma^{\mathrm{univ}}(U) = \Gamma^{\mathrm{univ}}(U')$$

#### 9.3.3 — Exemples de coarse-grainings

**Exemple 1 : Univers 1D (chaînes)**

$$\mathcal{M}_{\mathrm{univ}}^{(1D)} := \{0, 1\} \times \{0, 1\}$$

avec $\Gamma^{\mathrm{univ}}(U) = (d_{\mathrm{eff}}(U), o(U))$ où :
- $d_{\mathrm{eff}}(U) \in \{0, 1\}$ : dimension effective (croissance des boules)
- $o(U) \in \{0, 1\}$ : présence d'observateurs

**Exemple 2 : Univers 2D (réseaux)**

$$\mathcal{M}_{\mathrm{univ}}^{(2D)} := \mathbb{N} \times \{0, 1\}^2$$

avec :
- Premier entier : dimension effective
- Premier bit : composante infinie de type 2D
- Second bit : présence d'observateurs

**Exemple 3 : Classification physique**

$$\mathcal{M}_{\mathrm{univ}}^{\mathrm{phys}} := \{d, g, \Lambda, \text{obs}\}$$

où :
- $d$ : dimension effective
- $g$ : structure de groupe de symétrie
- $\Lambda$ : constante cosmologique effective
- obs : type d'observateurs

### 9.4 — Distribution des univers (réalisation de 9.I.δ)

#### 9.4.1 — Ensemble des nucléations à l'indice 0

L'ensemble des histoires dont le premier événement est une nucléation :

\1

> **Remarque (jauge de codage).** L’écriture "$e_0(\omega)$" et l’usage du décalage $\Theta$ reposent sur un choix de linéarisation (jauge). Les quantités introduites ici sont physiquement pertinentes dès lors que la propriété "être une nucléation" est invariante sous permutations d’événements concurrents (ou, à défaut, après moyennage sur les linéarisations). Sous stationnarité, tout indice est équivalent : $\mu_\beta(\mathsf{Nuc}_n)=\mu_\beta(\mathsf{Nuc}_0)$ pour tout $n$.


**Hypothèse :** Le taux total de nucléation est non nul :

$$\lambda_{\mathrm{tot}} := \mu_\beta(\mathsf{Nuc}_0) > 0$$

#### 9.4.2 — Mesure conditionnelle de nucléation

**Définition 9.5 (Mesure de nucléation).** La mesure conditionnelle de nucléation est :

$$\mu_\beta^{\mathrm{Nuc}}(A) := \mu_\beta(A \mid \mathsf{Nuc}_0) = \frac{\mu_\beta(A \cap \mathsf{Nuc}_0)}{\mu_\beta(\mathsf{Nuc}_0)}$$

**Interprétation :** Sous $\mu_\beta^{\mathrm{Nuc}}$, on conditionne sur le fait que $e_0$ est une nucléation (par stationnarité de $\mu_\beta$, la distribution des nucléations ne dépend pas de l’indice : on peut choisir l’indice 0 sans perte de généralité).

#### 9.4.3 — Univers aléatoire typique

Sur $\mathsf{Nuc}_0$, on peut définir le type de l'univers associé à $e_0$ :

$$U_0^{\mathrm{type}}(\omega) := \Gamma^{\mathrm{univ}}(U_0(\omega)) \in \mathcal{M}_{\mathrm{univ}}$$

**Définition 9.6 (Univers aléatoire typique).** L'univers aléatoire typique est la variable aléatoire :

$$U_* := U_0^{\mathrm{type}}$$

définie sur $(\mathsf{Nuc}_0, \mu_\beta^{\mathrm{Nuc}})$.

#### 9.4.4 — Distribution des types d'univers

**Définition 9.7 (Distribution des univers).** La distribution des types d'univers est :

$$\Pi^{\mathrm{univ}}(A) := \mu_\beta^{\mathrm{Nuc}}(U_* \in A) = \mu_\beta^{\mathrm{Nuc}}(\{\omega \in \mathsf{Nuc}_0 : \Gamma^{\mathrm{univ}}(U_0(\omega)) \in A\})$$

**Interprétation :** $\Pi^{\mathrm{univ}}(A)$ est la probabilité qu'une nucléation "typique" donne un univers de type dans $A$.

---

### 9.5 — Univers émergents (réalisation de 9.I.ε)

#### 9.5.1 — Définition

**Définition 9.8 (Type émergent).** Un type d'univers $u \in \mathcal{M}_{\mathrm{univ}}$ est émergent (pour le vide $(\Omega_B, \mu_\beta)$) si :

$$\Pi^{\mathrm{univ}}(\{u\}) > 0$$

#### 9.5.2 — Types typiques

**Définition 9.9 (Types typiques).** Un ensemble $A \subseteq \mathcal{M}_{\mathrm{univ}}$ est un ensemble de types typiques si :

$$\Pi^{\mathrm{univ}}(A) = 1$$

**Interprétation :**
- Types émergents : réalisés avec probabilité non nulle
- Types typiques : réalisés presque sûrement

#### 9.5.3 — Hiérarchie des types

La distribution $\Pi^{\mathrm{univ}}$ induit une hiérarchie sur les types d'univers :

| Catégorie | Condition | Interprétation |
|-----------|-----------|----------------|
| **Dominant** | $\Pi^{\mathrm{univ}}(\{u\})$ maximal | Type le plus fréquent |
| **Émergent** | $\Pi^{\mathrm{univ}}(\{u\}) > 0$ | Type réalisé |
| **Rare** | $\Pi^{\mathrm{univ}}(\{u\})$ très petit | Type exceptionnel |
| **Supprimé** | $\Pi^{\mathrm{univ}}(\{u\}) = 0$ | Type jamais réalisé (sous $\mu_\beta$) |

---

### 9.6 — Sélection d'histoires par les univers (réalisation de 9.I.ζ)

#### 9.6.1 — Compteur d'univers

Pour un ensemble de types $A \subseteq \mathcal{M}_{\mathrm{univ}}$, le compteur d'univers est :

$$N_A(\omega) := |\{n \in \mathsf{Nuc}(\omega) : \Gamma^{\mathrm{univ}}(U_n(\omega)) \in A\}|$$

C'est le nombre d'univers de type dans $A$ qui émergent dans l'histoire $\omega$.

\1

> **Condition suffisante (intensité finie).** Une condition naturelle assurant $0<\mathbb{E}_{\mu_\beta}[N_A]<\infty$ est l’existence d’une intensité finie de nucléations (par événement ou par “volume combinatoire”) dans des fenêtres finies, et une probabilité conditionnelle non nulle d’obtenir un type dans $A$. Dans les modèles à cutoff $\Lambda$, cette finitude est souvent automatique (espace effectif fini), puis discutée en limite $\Lambda\to\infty$.



Nous nous restreignons aux ensembles de types $A$ pour lesquels le nombre d’univers de type $A$ par histoire est intégrable, de sorte que $\hat{\mu}_\beta^A$ soit bien définie.

#### 9.6.2 — Mesure size-biased

**Définition 9.10 (Mesure size-biased).** La mesure biaisée par les univers de type $A$ est :

$$\hat{\mu}_\beta^A(d\omega) := \frac{N_A(\omega)}{\mathbb{E}_{\mu_\beta}[N_A]} \cdot \mu_\beta(d\omega)$$

**Propriétés :**
- $\hat{\mu}_\beta^A$ est une probabilité sur $(\Omega_B, \Sigma_B)$
- Les histoires avec plus d'univers de type $A$ ont plus de poids

#### 9.6.3 — Interprétation

L'expérience abstraite suivante :
1. Tirer $\omega$ selon $\mu_\beta$
2. Tirer uniformément un univers $U_n(\omega)$ de type dans $A$

donne une distribution marginale sur $\omega$ égale à $\hat{\mu}_\beta^A$.

**Slogan :** $\hat{\mu}_\beta^A$ est la loi des histoires vue du point de vue d'un univers de type $A$.

---

### 9.7 — Définition complète d'univers émergent

En combinant les éléments précédents :

**Définition 9.11 (Univers émergent - définition complète).** Un type d'univers $u \in \mathcal{M}_{\mathrm{univ}}$ est un univers émergent pour le vide $(\Omega_B, \mu_\beta)$ si :

1. **Réalisation :** $\Pi^{\mathrm{univ}}(\{u\}) > 0$
2. **Normalisation :** $0 < \mathbb{E}_{\mu_\beta}[N_{\{u\}}] < \infty$

Dans ce cas :
- $\Pi^{\mathrm{univ}}(\{u\})$ mesure la fréquence des univers de type $u$
- $\hat{\mu}_\beta^{\{u\}}$ décrit les histoires vues depuis un univers de type $u$

---

### 9.8 — Synthèse conceptuelle

La logique d'ensemble, sans quitter le formalisme :

```
NIVEAU I + μ₀ (Multivers combinatoire)
    │
    │ Ω_B contient toutes les histoires admissibles
    │ μ₀ = mesure de référence (non sélectionnée)
    ▼
SÉLECTION (Chapitre 8)
    │
    │ Action locale ℓ + principe variationnel
    │ → mesure μ_β sur Ω_B
    ▼
PHASES ET NUCLÉATION (Chapitres 6-7)
    │
    │ Décomposition ergodique de μ_β
    │ Taux de nucléation λ_[G]
    ▼
UNIVERS MICROSCOPIQUES
    │
    │ U_n(ω) = futur causal de e_n dans ω
    │ Domaine causal U(e_n, ω)
    ▼
TYPES D'UNIVERS
    │
    │ Coarse-graining Γ^univ : U_mic → M_univ
    │ Types u = classes d'équivalence macro
    ▼
DISTRIBUTION DES UNIVERS
    │
    │ Conditionnement sur Nuc₀
    │ → Π^univ sur M_univ
    ▼
UNIVERS ÉMERGENTS
    │
    │ Types u avec Π^univ({u}) > 0
    │ Mesure size-biased μ̂_β^{u}
    ▼
SÉLECTION D'HISTOIRES PAR LES UNIVERS
    
    Dualité : histoires ↔ univers
```

**Ce qui n'est PAS introduit :**
- Temps fondamental (la translation $\Theta$ est un reparamétrage)
- Superposition d'histoires (mesure de Kolmogorov classique)
- Effondrement quantique (sélection par conditionnement)

---

## Résumé de la structure

```
CHAPITRE 9 — UNIVERS ÉMERGENTS
│
├── Partie I : NOYAU ONTOLOGIQUE (6 principes)
│   ├── 9.I.α  Univers = futur causal       [définition fondamentale]
│   ├── 9.I.β  Infinitude                   [condition cosmologique]
│   ├── 9.I.γ  Coarse-graining              [types d'univers]
│   ├── 9.I.δ  Distribution                 [Π^univ induite par μ_β]
│   ├── 9.I.ε  Émergence                    [Π^univ({u}) > 0]
│   └── 9.I.ζ  Dualité                      [histoires ↔ univers]
│
└── Partie II : REPRÉSENTATION (8 sections)
    ├── 9.1  Deux points de vue             [global vs interne]
    ├── 9.2  Univers microscopiques         [U_n(ω), domaine causal]
    ├── 9.3  Types d'univers                [Γ^univ, M_univ]
    ├── 9.4  Distribution des univers       [Π^univ]
    ├── 9.5  Univers émergents              [Π^univ({u}) > 0]
    ├── 9.6  Sélection d'histoires          [mesure size-biased]
    ├── 9.7  Définition complète            [synthèse]
    └── 9.8  Logique d'ensemble             [récapitulatif]
```

---

## Remarques critiques

### Sur le choix de $\Gamma^{\mathrm{univ}}$

Le coarse-graining d'univers $\Gamma^{\mathrm{univ}}$ est une donnée du modèle, pas une conséquence des axiomes. 

$\Gamma^{\mathrm{univ}}$ devrait être choisi de façon :

- causale (ne dépend que du domaine causal de la nucléation),
- invariant par isomorphismes internes de cet univers,
- éventuellement compatible avec la stationnarité interne.

**Questions ouvertes :**
- Existe-t-il un $\Gamma^{\mathrm{univ}}$ "naturel" ?
- Comment caractériser "notre type d'univers" ?
- Le type inclut-il la présence d'observateurs (circularité potentielle) ?

### Sur la relation avec le principe anthropique

La distribution $\Pi^{\mathrm{univ}}$ peut être interprétée de deux façons :

1. **Interprétation fréquentiste** : Parmi tous les univers qui nucléent, quelle fraction est de type $u$ ?

2. **Interprétation anthropique** : Si on conditionne sur "je suis un observateur", quelle est la distribution sur les types d'univers ?

La seconde interprétation nécessite de définir ce qu'est un "observateur" (chapitre 10).

### Sur la mesure size-biased

La mesure $\hat{\mu}_\beta^A$ résout un problème conceptuel :

> "Comment passer du point de vue 'créateur' (mesure $\mu_\beta$ sur toutes les histoires) au point de vue 'créature' (vue depuis un univers particulier) ?"

C'est une forme de conditionnement par l'existence qui évite les paradoxes du type "pourquoi quelque chose plutôt que rien".

---

## Lien avec les autres chapitres

| Chapitre | Relation avec Ch.9 |
|----------|-------------------|
| Ch.7 (Nucléation) | Définit $\mathsf{Nuc}_0$ et les taux $\lambda_{[\mathcal{G}]}$ |
| Ch.8 (Sélection) | Fournit $\mu_\beta$ qui détermine $\Pi^{\mathrm{univ}}$ |
| Ch.6 (Phases) | Les phases ergodiques correspondent à des régimes de nucléation |
| Ch.10 (Observateurs) | Définit ce qu'est un observateur dans un univers |

---

## Glossaire du chapitre

| Terme | Définition |
|-------|------------|
| **Univers microscopique** $U_n(\omega)$ | Couple $(\omega, e_n)$ avec dynamique restreinte |
| **Domaine causal** $\mathcal{U}(e_n, \omega)$ | Futur causal du germe créé par $e_n$ |
| **Type d'univers** $u$ | Élément de $\mathcal{M}_{\mathrm{univ}}$ |
| **Coarse-graining** $\Gamma^{\mathrm{univ}}$ | $\mathcal{U}_{\mathrm{mic}} \to \mathcal{M}_{\mathrm{univ}}$ |
| **Distribution** $\Pi^{\mathrm{univ}}$ | Loi de $U_*$ sous $\mu_\beta^{\mathrm{Nuc}}$ |
| **Type émergent** | $\Pi^{\mathrm{univ}}(\{u\}) > 0$ |
| **Mesure size-biased** $\hat{\mu}_\beta^A$ | $(N_A / \mathbb{E}[N_A]) \cdot \mu_\beta$ |

