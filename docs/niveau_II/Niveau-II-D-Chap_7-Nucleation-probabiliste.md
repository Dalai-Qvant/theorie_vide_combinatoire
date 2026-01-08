# Niveau II - Chapitre 7

# D. Nucléation probabiliste des germes supercritiques

---

## Introduction

Le niveau I a introduit les germes supercritiques : des motifs qui, une fois formés, engendrent une croissance causale illimitée. Ce sont les "graines" potentielles d'univers.

Au niveau I, la nucléation est un concept déterministe : pour une histoire $\omega$ donnée, soit un germe nucléé, soit non.

Ce chapitre transpose la nucléation dans le cadre probabiliste du niveau II :
- Les événements de nucléation deviennent des variables aléatoires
- On définit des taux de nucléation (intensités) par type de germe
- On classifie les phases selon leur comportement vis-à-vis de la nucléation

> **Point clé :** Le passage niveau I → niveau II transforme une question binaire ("le germe $[\mathcal{G}]$ nucléé-t-il ?") en une question quantitative ("quelle est la fréquence de nucléation de $[\mathcal{G}]$ ?").

---

## Partie I : Noyau ontologique

### 7.I.α — Principe de nucléation comme observable

> **La nucléation est une propriété mesurable des histoires.**

Pour chaque germe supercritique $[\mathcal{G}]$ et chaque position $n$ dans le codage, la propriété "$e_n$ est un événement de nucléation de type $[\mathcal{G}]$" définit un sous-ensemble mesurable de $\Omega_B$.

Cette mesurabilité est essentielle : elle permet de définir des probabilités de nucléation.

---

### 7.I.β — Principe de stationnarité du processus de nucléation

> **La nucléation est statistiquement homogène le long de la causalité.**

Sous une mesure stationnaire $\mu$, la probabilité qu'un événement soit une nucléation de type $[\mathcal{G}]$ est indépendante de sa position dans le codage (jauge), pour des observables invariantes sous permutations d'événements concurrents.

Ce principe découle de l'invariance de $\mu$ par $\Theta$ (chapitre 4).

---

### 7.I.γ — Principe de filtrage par le crédit

> **Le crédit combinatoire $B$ détermine quels germes peuvent nucléer.**

Un germe $[\mathcal{G}]$ ne peut nucléer que si son crédit minimal de formation $B_{\mathrm{form}}([\mathcal{G}])$ est inférieur ou égal à $B$.

Si $B < B_{\mathrm{form}}([\mathcal{G}])$, alors $\lambda_{[\mathcal{G}]} = 0$ identiquement : le germe est "interdit" par le budget combinatoire.

---

### 7.I.δ — Principe de hiérarchie des germes

> **Les germes supercritiques forment une hiérarchie ordonnée par leur taux de nucléation.**

Parmi tous les germes admissibles ($B_{\mathrm{form}} \leq B$), certains nuclèent fréquemment, d'autres rarement. Cette hiérarchie est capturée par le spectre de nucléation $\Lambda$.

Le spectre détermine quels types d'univers sont statistiquement favorisés.

---

### 7.I.ε — Principe de régime de phase

> **Les phases se distinguent par leur comportement vis-à-vis de la nucléation.**

Une phase peut être :
- **Sans nucléation** : aucun germe supercritique ne nucléé (vide stérile)
- **À nucléation rare** : les nucléations sont des événements exceptionnels
- **À nucléation fréquente** : les nucléations sont omniprésentes

Ces régimes correspondent à des structures macroscopiques qualitativement différentes.

---

## Partie II : Choix de représentation

### 7.1 — Cadre et rappels

On fixe :
- Un système de niveau I $(H_0, \mathcal{R}, K, B)$
- L'espace $(\Omega_B, \Sigma_B)$ avec une mesure stationnaire $\mu$
- L'opérateur de translation $\Theta$

Le quadruplet $(\Omega_B, \Sigma_B, \mu, \Theta)$ est un système dynamique mesuré.

#### 7.1.1 — Rappel : germes supercritiques (niveau I)

Un motif $[\mathcal{G}]$ est un germe supercritique si :
1. Il existe une histoire $\omega$ contenant une occurrence $\mathcal{R}_0 \simeq \mathcal{G}$
2. Le futur causal de $\mathcal{R}_0$ engendre des régions de taille non bornée :
   $$\sup_n |\mathcal{R}_n| = +\infty$$

#### 7.1.2 — Rappel : événement de nucléation (niveau I)

Un événement $e$ est une nucléation de type $[\mathcal{G}]$ si :
1. $e$ crée une occurrence $\mathcal{R}_0 \simeq \mathcal{G}$
2. Le futur causal de $\mathcal{R}_0$ a une croissance non bornée
3. $e$ est minimal pour cette propriété au sens de l'ordre causal $\prec$ : il n'existe pas d'événement $e' \prec e$ tel que $e'$ crée déjà une occurrence supercritique (au sens 1–2) dont le futur causal engendre la même composante de croissance non bornée.


#### 7.1.3 — Convention de jauge (linéarisation) et typage canonique

Dans ce chapitre, on utilise un codage linéarisé des événements $(e_n)_{n\ge 0}$ (cf. chapitre 4) obtenu à partir d'une extension linéaire de l'ordre causal.  
Ce choix est une jauge de représentation : deux codages qui ne diffèrent que par permutation d'événements concurrents (commutants) décrivent la même histoire au sens causal.

Les quantités définies ici (processus $X_n$, taux $\lambda$, spectre $\Lambda$) sont donc physiquement significatives dès lors que l'énoncé « être une nucléation » :
- dépend uniquement de la structure causale $(\prec)$ et de voisinages causaux finis, et
- est invariant sous permutation d'événements concurrents (ou, à défaut, est moyenné sur des linéarisations admissibles).

Un même événement peut, en principe, satisfaire plusieurs étiquettes « nucléation de type $[\mathcal G]$ » (types imbriqués).  
Pour obtenir un spectre normalisable et des ensembles disjoints, on fixe une convention de typage canonique.

**Définition 7.0 (Typage canonique).** On choisit un bon-ordre mesurable $\triangleleft$ sur l'ensemble dénombrable des types de germes supercritiques (par exemple : ordre lexicographique sur $(B_{\mathrm{form}}, K, |\mathcal G|)$).  
Pour chaque événement $e$ dans une histoire $\omega$, on définit :

- $\mathrm{Cand}(e,\omega)$ : l'ensemble (éventuellement vide) des types $[\mathcal G]$ tels que $e$ vérifie la définition de nucléation de type $[\mathcal G]$,
- $\mathrm{Type}(e,\omega)$ : l'unique élément minimal de $\mathrm{Cand}(e,\omega)$ pour $\triangleleft$, s'il existe, sinon $\bot$ (« pas de nucléation »).

Par construction, pour un événement donné, un seul type est assigné.


---

### 7.2 — Processus de nucléation

#### 7.2.1 — Ensemble des histoires avec nucléation en position 0

Pour un germe supercritique $[\mathcal{G}]$, on définit :

$$\mathsf{Nuc}_0([\mathcal{G}]) := \{\omega \in \Omega_B \mid \mathrm{Type}(e_0(\omega),\omega) = [\mathcal{G}]\}$$

**Proposition (Mesurabilité).** L'ensemble $\mathsf{Nuc}_0([\mathcal{G}])$ appartient à $\Sigma_B$ (voir remarques critiques).

*Esquisse de preuve.* La propriété "être une nucléation" se décompose en :
- Création d'un motif local (propriété cylindrique finie)
- Croissance non bornée du futur (limite d'événements cylindriques)
- Minimalité (condition sur le passé causal fini)

Toutes ces propriétés sont mesurables pour $\Sigma_B$.

**Ensemble total de nucléation :**

$$\mathsf{Nuc}_0 := \bigcup_{[\mathcal{G}] \in \mathcal{G}_{\mathrm{sup}}} \mathsf{Nuc}_0([\mathcal{G}])$$

Les motifs sont des régions finies sur des types discrets, l’ensemble des classes d’isomorphisme $\mathcal{G}_{\mathrm{sup}}$ est dénombrable. L’union est dénombrable, donc mesurable.

#### 7.2.2 — Variable indicatrice de nucléation

**Définition.** L'indicatrice de nucléation de type $[\mathcal{G}]$ à la position $0$ est :

$$X^{[\mathcal{G}]}_0 : \Omega_B \to \{0, 1\}, \quad X^{[\mathcal{G}]}_0(\omega) := \mathbf{1}_{\mathsf{Nuc}_0([\mathcal{G}])}(\omega)$$

> Remarque (jauge). $e_0(\omega)$ dépend du codage linéarisé. Le typage canonique et la minimalité en $\prec$ rendent toutefois l'événement « être une nucléation typée » insensible aux permutations d'événements concurrents.


#### 7.2.3 — Processus stationnaire

Par translation, on définit pour tout $n \geq 0$ :

$$X^{[\mathcal{G}]}_n(\omega) := X^{[\mathcal{G}]}_0(\Theta^n \omega)$$

**Interprétation :** $X^{[\mathcal{G}]}_n(\omega) = 1$ ssi l'événement $e_n$ est une nucléation de type $[\mathcal{G}]$.

**Propriété.** La famille $(X^{[\mathcal{G}]}_n)_{n \geq 0}$ est un processus stochastique stationnaire :

- Toutes les $X^{[\mathcal{G}]}_n$ ont même loi (par $\Theta$-invariance de $\mu$)
- Les lois jointes sont invariantes par décalage

#### 7.2.4 — Processus ponctuel de nucléation

Pour chaque histoire $\omega$, on définit l'ensemble des instants de nucléation :

$$T_{[\mathcal{G}]}(\omega) := \{n \in \mathbb{N} \mid X^{[\mathcal{G}]}_n(\omega) = 1\}$$

C'est un processus ponctuel stationnaire sur $\mathbb{N}$ : les positions des nucléations de type $[\mathcal{G}]$ le long du codage.

---

### 7.3 — Taux de nucléation

#### 7.3.1 — Intensité moyenne

**Définition 7.1 (Taux de nucléation).** Le taux de nucléation de type $[\mathcal{G}]$ est :

$$\lambda_{[\mathcal{G}]} := \mathbb{E}_\mu[X^{[\mathcal{G}]}_0] = \mu(\mathsf{Nuc}_0([\mathcal{G}]))$$



**Définition 7.1bis (Taux total de nucléation).** On définit

$$\lambda_{\mathrm{tot}} := \mu(\mathsf{Nuc}_0) = \sum_{[\mathcal G]\in\mathcal G_{\mathrm{sup}}} \lambda_{[\mathcal G]}\,,$$

qui est la probabilité qu'un événement (dans la jauge choisie) soit typé comme une nucléation.
**Interprétation :** $\lambda_{[\mathcal{G}]}$ est la probabilité qu'un événement "typique" (tiré selon $\mu$) soit une nucléation de type $[\mathcal{G}]$.

**Propriété (Stationnarité) :** Pour tout $n$ :

$$\mathbb{E}_\mu[X^{[\mathcal{G}]}_n] = \lambda_{[\mathcal{G}]}$$

#### 7.3.2 — Fréquence empirique

Pour $N \in \mathbb{N}$, le compteur de nucléations est :

$$N_{[\mathcal{G}]}(\omega; N) := \sum_{n=0}^{N-1} X^{[\mathcal{G}]}_n(\omega) = |\{0 \leq n < N : e_n \text{ est nucléation de type } [\mathcal{G}]\}|$$

La fréquence empirique est :

$$f_{[\mathcal{G}]}(\omega; N) := \frac{N_{[\mathcal{G}]}(\omega; N)}{N}$$

#### 7.3.3 — Convergence ergodique

**Théorème 7.2 (Taux de nucléation par événement).** Si $\mu$ est ergodique, alors pour $\mu$-presque toute histoire $\omega$ :

$$\lim_{N \to \infty} f_{[\mathcal{G}]}(\omega; N) = \lambda_{[\mathcal{G}]}$$

*Preuve.* Application directe du théorème ergodique de Birkhoff à l'observable $X^{[\mathcal{G}]}_0$.

**Interprétation :** Dans une phase ergodique, la fréquence empirique de nucléation converge vers le taux moyen. Une histoire "typique" voit exactement la densité de nucléation prédite par $\mu$.

---

### 7.4 — Densité de nucléation par volume causal (optionnel)

On peut raffiner en mesurant la nucléation par "volume causal" plutôt que par nombre d'événements.

#### 7.4.1 — Poids de volume

On associe à chaque événement un volume combinatoire $V(e) \geq 0$ (par exemple, nombre de sites modifiés).

On suppose $V(e_0)$ est bornée ou au moins intégrable sous $\mu$, ce qui est naturel puisque le support combinatoire de chaque événement est fini.

#### 7.4.2 — Densité par volume

Le volume cumulé** est :

$$V_N(\omega) := \sum_{n=0}^{N-1} V(e_n(\omega))$$

Par ergodicité :

$$\lim_{N \to \infty} \frac{V_N(\omega)}{N} = \mathbb{E}_\mu[V(e_0)] \quad \text{p.s.}$$

**Définition.** La densité de nucléation par volume est :

$$\rho_{[\mathcal{G}]} := \frac{\lambda_{[\mathcal{G}]}}{\mathbb{E}_\mu[V(e_0)]}$$

**Interprétation :** $\rho_{[\mathcal{G}]}$ est le nombre moyen de nucléations de type $[\mathcal{G}]$ par unité de volume combinatoire.

---

### 7.5 — Filtre du crédit (réalisation de 7.I.γ)

Le crédit combinatoire $B$ agit comme un filtre sur les germes supercritiques.

#### 7.5.1 — Crédit minimal de formation

Rappel (niveau I) : Pour un motif $[\mathcal{P}]$, le crédit minimal de formation est :

$$B_{\mathrm{form}}([\mathcal{P}]) := \min_{\omega, \gamma} \max_{n \in \gamma} (-S_n(\omega))$$

où le minimum porte sur les histoires $\omega$ contenant $[\mathcal{P}]$ et les chemins $\gamma$ menant à sa formation.

#### 7.5.2 — Germes interdits

**Proposition 7.3 (Germes interdits par le crédit).** Si $B < B_{\mathrm{form}}([\mathcal{G}])$, alors :

$$\lambda_{[\mathcal{G}]} = 0$$

*Preuve.* Si $B < B_{\mathrm{form}}([\mathcal{G}])$, aucune histoire de $\Omega_B$ ne contient $[\mathcal{G}]$ (proposition du niveau I). Donc $\mathsf{Nuc}_0([\mathcal{G}]) = \varnothing$, et $\lambda_{[\mathcal{G}]} = \mu(\varnothing) = 0$.

#### 7.5.3 — Classification des germes

| Condition | Statut du germe |
|-----------|-----------------|
| $B_{\mathrm{form}}([\mathcal{G}]) > B$ | **Interdit** : $\lambda_{[\mathcal{G}]} = 0$ (impossible) |
| $B_{\mathrm{form}}([\mathcal{G}]) \leq B$ et $\lambda_{[\mathcal{G}]} = 0$ | **Admissible mais non réalisé** (supprimé par $\mu$) |
| $B_{\mathrm{form}}([\mathcal{G}]) \leq B$ et $\lambda_{[\mathcal{G}]} > 0$ | **Actif** : nucléé effectivement |

---

### 7.6 — Spectre de nucléation (réalisation de 7.I.δ)

#### 7.6.1 — Définition du spectre

Soit $\mathcal{G}_{\mathrm{sup}}$ l'ensemble des germes supercritiques pour $(H_0, \mathcal{R})$.

**Définition 7.4 (Spectre de nucléation).** Le **spectre de nucléation** est la fonction :

$$\Lambda : \mathcal{G}_{\mathrm{sup}} \to [0, 1], \quad \Lambda([\mathcal{G}]) := \lambda_{[\mathcal{G}]}$$

**Propriété de normalisation :** Par construction du typage canonique $\mathrm{Type}$, les ensembles $\mathsf{Nuc}_0([\mathcal G])$ sont disjoints et inclus dans $\Omega_B$. On a donc :

$$\sum_{[\mathcal{G}] \in \mathcal{G}_{\mathrm{sup}}} \Lambda([\mathcal{G}]) = \lambda_{\mathrm{tot}} \le 1.$$

On définit alors

$$\Lambda_{\mathrm{none}} := 1-\lambda_{\mathrm{tot}},$$

qui est la probabilité qu'un événement ne soit pas typé comme une nucléation.

#### 7.6.2 — Distribution relative

**Définition 7.5 (Distribution relative).** Si $\lambda_{\mathrm{tot}} > 0$, la **distribution relative** est :

$$\tilde{\Lambda}([\mathcal{G}]) := \frac{\lambda_{[\mathcal{G}]}}{\sum_{[\mathcal{G}'] \in \mathcal{G}_{\mathrm{sup}}} \lambda_{[\mathcal{G}']}}$$

**Interprétation :** $\tilde{\Lambda}([\mathcal{G}])$ est la probabilité conditionnelle qu'une nucléation (sachant qu'il y en a une) soit de type $[\mathcal{G}]$.

#### 7.6.3 — Hiérarchie des germes

Le spectre $\Lambda$ définit une hiérarchie sur les types de germes :

- **Germes dominants** : $\Lambda([\mathcal{G}])$ grand → types d'univers les plus fréquents
- **Germes subdominants** : $\Lambda([\mathcal{G}])$ petit → types d'univers rares
- **Germes supprimés** : $\Lambda([\mathcal{G}]) = 0$ → types jamais réalisés

Cette hiérarchie dépend de la mesure $\mu$ (et donc, via le chapitre 8, du principe de sélection).

---

### 7.7 — Régimes de phase (réalisation de 7.I.ε)

#### 7.7.1 — Phase sans nucléation

**Définition.** Une phase est sans nucléation si :

$$\lambda_{[\mathcal{G}]} = 0 \quad \forall [\mathcal{G}] \in \mathcal{G}_{\mathrm{sup}}$$

**Conséquence :** Pour $\mu$-presque toute histoire :

$$T_{[\mathcal{G}]}(\omega) = \varnothing \quad \forall [\mathcal{G}]$$

Aucun germe supercritique ne nucléé.

> **Conséquence (sous une hypothèse de démarrage local).** Si l'on suppose que toute croissance non bornée (composante « infinie » au sens du chapitre 6) est engendrée par au moins une nucléation minimale locale, alors l'absence de nucléation implique l'absence de croissance non bornée : le vide reste stérile (fluctuations finies).

**Mécanismes possibles :**
- Filtre par $B$ : tous les germes ont $B_{\mathrm{form}} > B$
- Suppression dynamique : le noyau $T$ évite les configurations menant aux germes

#### 7.7.2 — Phase à nucléation rare

**Définition.** Une phase est à nucléation rare si :

$$0 < \lambda_{\mathrm{tot}} \ll 1$$

**Caractéristiques :**
- Les nucléations sont des événements exceptionnels
- (Heuristique) Les germes supercritiques sont typiquement espacés ; les grandes composantes ont peu de chances d'interagir.
- Structure de type "archipel d'univers" dans un océan de fluctuations subcritiques

#### 7.7.3 — Phase à nucléation fréquente

**Définition.** Une phase est à nucléation fréquente si :

$$\lambda_{\mathrm{tot}} \approx 1$$

**Caractéristiques :**
- Presque chaque événement est une nucléation
- Les composantes infinies se "recouvrent"
- Structure globalement percolante

#### 7.7.4 — Tableau récapitulatif

| Régime | Condition sur $\Lambda$ | Structure typique |
|--------|------------------------|-------------------|
| Sans nucléation | $\lambda_{\mathrm{tot}} = 0$ | Vide stérile (sous hypothèse de démarrage local) |
| Nucléation rare | $0 < \lambda_{\mathrm{tot}} \ll 1$ | Germes typiquement espacés; "archipel" (heuristique) |
| Nucléation fréquente | $\lambda_{\mathrm{tot}} \approx 1$ | Forte densité de germes; percolation (composantes d'interaction, chap. 6) |

---

## Résumé de la structure

```
CHAPITRE 7 — NUCLÉATION PROBABILISTE
│
├── Partie I : NOYAU ONTOLOGIQUE (5 principes)
│   ├── 7.I.α  Nucléation mesurable       [sous-ensemble de Σ_B]
│   ├── 7.I.β  Stationnarité              [λ indépendant de n]
│   ├── 7.I.γ  Filtrage par crédit        [B_form ≤ B nécessaire]
│   ├── 7.I.δ  Hiérarchie des germes      [spectre Λ]
│   └── 7.I.ε  Régimes de phase           [stérile/rare/fréquent]
│
└── Partie II : REPRÉSENTATION (7 sections)
    ├── 7.1  Cadre et rappels             [germes, nucléation niveau I]
    ├── 7.2  Processus de nucléation      [X^[G]_n, processus ponctuel]
    ├── 7.3  Taux de nucléation           [λ_[G], Birkhoff]
    ├── 7.4  Densité par volume           [ρ_[G] optionnel]
    ├── 7.5  Filtre du crédit             [B_form vs B]
    ├── 7.6  Spectre de nucléation        [Λ, distribution relative]
    └── 7.7  Régimes de phase             [classification]
```

---

## Remarques critiques

### Sur la mesurabilité de la nucléation

La proposition 7.1 affirme que $\mathsf{Nuc}_0([\mathcal{G}]) \in \Sigma_B$. L'argument est esquissé mais pas complètement rigoureux.

**Difficulté :** La croissance non bornée du futur est une propriété asymptotique (limite $n \to \infty$). Elle s'exprime comme :

$$\{\omega : \sup_n |\mathcal{R}_n(\omega)| = \infty\} = \bigcap_{M} \bigcup_{n} \{\omega : |\mathcal{R}_n(\omega)| \geq M\}$$

Chaque ensemble $\{|\mathcal{R}_n| \geq M\}$ est mesurable (dépend d'un nombre fini d'événements). L'intersection et l'union dénombrables préservent la mesurabilité. 

### Sur le lien entre spectre et physique

Le spectre $\Lambda$ est entièrement déterminé par $\mu$. Or $\mu$ dépend du principe de sélection (chapitre 8).

**Question :** Le spectre de notre univers correspond-il à un $\mu_\beta$ particulier ? Si oui, quel $\beta$ ?

Cette question relie directement la nucléation à la sélection par action.

### Sur la distinction rare/fréquent

La frontière entre "nucléation rare" et "nucléation fréquente" est qualitative, pas rigoureusement définie.

**Proposition de critère :** Une transition rare → fréquent pourrait être définie par le passage d'une phase non percolante à une phase percolante (au sens du chapitre 6).

### Sur l'absence de temps

Il est important de noter que les "taux de nucléation" ne sont pas des taux temporels. Ce sont des densités par événement (ou par volume combinatoire). Ces taux ne supposent pas l’existence d’un temps physique : ils sont définis par rapport à l’indice interne des événements dans une histoire.

La conversion en taux temporels nécessiterait :
1. Une définition de temps émergent dans chaque univers
2. Un lien entre le comptage d'événements et ce temps émergent

Ceci sera abordé au chapitre 10 (observateurs internes).

---

## Lien avec les autres chapitres

| Chapitre | Relation avec Ch.7 |
|----------|-------------------|
| Ch.3 (Niveau I) | Définit les germes supercritiques et $B_{\mathrm{form}}$ |
| Ch.4 (Probabilités) | Fournit $(\Omega_B, \Sigma_B, \mu)$ et la stationnarité |
| Ch.6 (Phases) | Les régimes de nucléation sont des types de phases |
| Ch.8 (Sélection) | $\mu_\beta$ détermine le spectre $\Lambda$ |
| Ch.9 (Univers) | Les univers émergents sont les futurs causaux des nucléations |

---

## Glossaire du chapitre

| Terme | Définition |
|-------|------------|
| **Taux de nucléation** $\lambda_{[\mathcal{G}]}$ | $\mu(\mathsf{Nuc}_0([\mathcal{G}]))$ |
| **Spectre de nucléation** $\Lambda$ | Fonction $[\mathcal{G}] \mapsto \lambda_{[\mathcal{G}]}$ |
| **Distribution relative** $\tilde{\Lambda}$ | $\Lambda$ normalisée sur les germes actifs |
| **Germe actif** | $\lambda_{[\mathcal{G}]} > 0$ |
| **Germe interdit** | $B_{\mathrm{form}}([\mathcal{G}]) > B$ |
| **Phase sans nucléation** | $\lambda_{\mathrm{tot}} = 0$ |

