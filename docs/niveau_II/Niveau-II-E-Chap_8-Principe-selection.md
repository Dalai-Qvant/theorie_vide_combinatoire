# Chapitre 8 — Principe de sélection et mesures d'action minimale

---

## Introduction

Les chapitres précédents ont établi :
- Un espace de mesures stationnaires $\mathcal{M}_{\mathrm{stat}}$ sur $(\Omega_B, \Sigma_B, \Theta)$
- Des notions de phases (ergodiques) et de nucléation
- Mais aucun critère pour choisir une mesure particulière

Ce chapitre introduit le principe de sélection : parmi toutes les mesures stationnaires possibles, certaines sont "physiques" : elles minimisent une fonctionnelle combinant action et entropie.

> **Point clé :** Le principe de sélection est une version statistique du principe de moindre action. On ne sélectionne pas une histoire unique, mais une distribution d'histoires optimisée.

C'est ce principe qui détermine quelles phases existent, quels germes nucléent, et ultimement quels types d'univers émergent.

---

## Partie I : Noyau ontologique

### 8.I.α — Principe d'action locale

> **Chaque événement porte un coût combinatoire intrinsèque.**

À partir de la structure du niveau I (complexité $K$, motifs locaux), on peut définir un "coût" ou "action" associé à chaque événement. Ce coût ne dépend que du voisinage causal local de l'événement.

L'action d'une histoire est la somme (ou l'intégrale) des coûts de ses événements.

---

### 8.I.β — Principe de mesure de référence

> **Il existe une mesure "neutre" représentant l'exploration a priori du vide.**

Avant toute sélection, le vide explore l'espace des histoires selon une mesure de référence $\mu_0$. Cette mesure représente ce que "verrait" un observateur sans préférence pour les histoires de faible ou haute action.

La mesure de référence est une donnée du modèle, pas une conséquence des axiomes.

---

### 8.I.γ — Principe de sélection variationnelle

> **La physique émerge des mesures qui minimisent l'action-information.**

Parmi toutes les mesures stationnaires, les mesures "physiques" sont celles qui réalisent un compromis optimal entre :
- **Minimiser l'action moyenne** (favoriser les histoires de faible coût)
- **Maximiser l'entropie** (préserver la diversité des histoires)

Ce compromis est contrôlé par un paramètre $\beta > 0$.

---

### 8.I.δ — Principe de limite thermodynamique

> **La sélection se définit par une limite sur des systèmes de taille croissante.**

La mesure sélectionnée $\mu_\beta$ est obtenue comme limite de mesures $\mu_N^\beta$ définies sur des préfixes de longueur $N$, quand $N \to \infty$.

Cette limite existe sous des conditions de régularité (localité de l'action, non-dégénérescence de $\mu_0$).

---

### 8.I.ε — Principe de stationnarité de la sélection

> **La mesure sélectionnée est stationnaire.**

Bien que la construction passe par des mesures $\mu_N^\beta$ non stationnaires (elles privilégient une fenêtre $[0, N-1]$), la limite $\mu_\beta$ est $\Theta$-invariante.

La sélection ne brise pas l'homogénéité du vide.

---

### 8.I.ζ — Principe de transition de phase

> **Le paramètre de sélection $\beta$ peut induire des transitions qualitatives.**

Pour certaines valeurs critiques de $\beta$, la structure de la mesure $\mu_\beta$ change de manière discontinue (ou non-analytique). Ces transitions séparent des régimes macroscopiques qualitativement différents.

---

## Partie II : Choix de représentation

### 8.1 — Cadre général

On rappelle :
- $(H_0, \mathcal{R}, K, B)$ : système de niveau I
- $(\Omega_B, \Sigma_B)$ : espace mesurable des histoires
- $\Theta$ : opérateur de translation
- $\mathcal{M}_{\mathrm{stat}}$ : ensemble des mesures $\Theta$-stationnaires sur $(\Omega_B, \Sigma_B)$

**Objectif du chapitre :** Définir un critère pour sélectionner $\mu \in \mathcal{M}_{\mathrm{stat}}$.

---

### 8.2 — Action locale

#### 8.2.1 — Densité d'action locale

**Définition 8.1 (Densité d'action locale).** Une densité d'action est une application mesurable :

$$\ell : \Omega_B \longrightarrow \mathbb{R}$$

satisfaisant :

1. **Localité causale** : Il existe $R_\ell \geq 0$ tel que $\ell(\omega)$ ne dépend que de la zone causale $N_{R_\ell}(e_0)$ :
   $$\ell(\omega) = \phi([N_{R_\ell}(e_0)])$$
   pour une fonction $\phi$ sur les classes d'isomorphisme de voisinages causaux.

2. **Invariance par isomorphisme** : Si $\omega$ et $\omega'$ coïncident à isomorphisme près dans $N_{R_\ell}(e_0)$, alors $\ell(\omega) = \ell(\omega')$.

3. **Contrôle par la complexité** : Il existe $a, b \geq 0$ tels que :
   $$|\ell(\omega)| \leq a \cdot |\Delta K(e_0(\omega))| + b$$

**Remarque (jauge de codage).** La notation $e_0(\omega)$ renvoie à un choix de linéarisation/codage (jauge) des événements. Cette dépendance est acceptable ici parce que les quantités finales (action moyenne, principe variationnel, taux de nucléation) seront formulées pour des observables intrinsèques : invariantes sous permutation d'événements concurrents (commutations autorisées), ou bien définies après une moyenne explicite sur les choix de codage. Une alternative entièrement intrinsèque consiste à remplacer $e_0$ par une agrégation (moyenne/histogramme) sur un ensemble canonique d'événements d'une même couche de référence.


#### 8.2.2 — Modèle canonique

**Exemple 8.2 (Densité canonique).** Le choix le plus simple est :

$$\ell_{\mathrm{can}}(\omega) := \alpha \cdot \Delta K(e_0) + \lambda \cdot n_{\mathrm{loc}}(e_0)$$

où :
- $\alpha, \lambda \in \mathbb{R}$ sont des constantes
- $\Delta K(e_0) = K(H_1) - K(H_0)$ est la variation de complexité
- $n_{\mathrm{loc}}(e_0)$ est le nombre de sites affectés par $e_0$

**Cas particuliers :**

| Choix | Interprétation |
|-------|----------------|
| $\ell = \Delta K$ | Action = variation de complexité |
| $\ell = $ constante | Action compte les événements |
| $\ell = n_{\mathrm{loc}}$ | Action = "volume" de l'événement |

#### 8.2.3 — Action tronquée

Pour $N \in \mathbb{N}$, l'action tronquée est :

$$S_N(\omega) := \sum_{n=0}^{N-1} \ell(\Theta^n \omega)$$

**Propriétés :**
- $S_N$ dépend des $N$ premiers événements (et de leurs voisinages de rayon $R_\ell$)
- $S_N$ est mesurable pour la σ-algèbre des cylindres de longueur $N + R_\ell$

**Action moyenne par événement :**

$$\bar{S}_N(\omega) := \frac{S_N(\omega)}{N}$$

---

### 8.3 — Mesure de référence (réalisation de 8.I.β)

#### 8.3.1 — Définition

**Définition 8.3 (Mesure de référence).** Une mesure de référence est une mesure $\mu_0$ sur $(\Omega_B, \Sigma_B)$ telle que :

1. $\mu_0$ est stationnaire : $\mu_0 \circ \Theta^{-1} = \mu_0$
2. $\mu_0$ est non dégénérée : elle attribue un poids non nul à un ensemble "large" d'histoires

#### 8.3.2 — Exemples de mesures de référence

| Construction | Description |
|--------------|-------------|
| **Markovienne uniforme** | $T_0(e \mid H) = \frac{1}{|\mathcal{E}(H)|}$ (équiprobabilité locale) |
| **Maximum d'entropie** | $\mu_0 = \arg\max_\mu h(\mu)$ sous contraintes |
| **Gibbs à $\beta = 0$** | Limite de $\mu_\beta$ quand $\beta \to 0$ |

**Remarque importante :** Le choix de $\mu_0$ est une donnée du modèle. Différents $\mu_0$ donnent différentes physiques émergentes.

---

### 8.4 — Mesures de Gibbs à volume fini

#### 8.4.1 — Poids d'action

On fixe un paramètre de sélection $\beta > 0$.

Pour chaque $N$, le poids d'action est :

$$W_N(\omega) := \exp(-\beta S_N(\omega)) = \exp\left(-\beta \sum_{n=0}^{N-1} \ell(\Theta^n \omega)\right)$$

**Interprétation :** $W_N$ pénalise exponentiellement les histoires de haute action.

#### 8.4.2 — Fonction de partition

La fonction de partition à volume $N$ est :

$$Z_N(\beta) := \int_{\Omega_B} W_N(\omega) \, \mu_0(d\omega) = \mathbb{E}_{\mu_0}[e^{-\beta S_N}]$$

On suppose $0 < Z_N(\beta) < \infty$ (condition de régularité).

#### 8.4.3 — Mesure de Gibbs à volume fini

**Définition 8.4 (Mesure de Gibbs à volume $N$).** La mesure :

$$\mu_N^\beta(d\omega) := \frac{W_N(\omega)}{Z_N(\beta)} \mu_0(d\omega)$$

est la mesure de Gibbs à volume $N$ et paramètre $\beta$.

**Propriétés :**
- $\mu_N^\beta$ est une probabilité sur $(\Omega_B, \Sigma_B)$
- $\mu_N^\beta$ n'est pas stationnaire (elle privilégie la fenêtre $[0, N-1]$)
- $\mu_N^\beta$ favorise les histoires de faible action $S_N$

---

### 8.5 — Limite thermodynamique (réalisation de 8.I.δ)

#### 8.5.1 — Convergence des marges

Pour $n$ fixé, la marge de $\mu_N^\beta$ sur les cylindres de longueur $n$ est notée $\mu_{N,n}^\beta$.

**Définition 8.5 (Existence de la limite).** La limite thermodynamique existe si, pour tout $n$ :

$$\mu_n^\beta := \lim_{N \to \infty} \mu_{N,n}^\beta$$

existe au sens de la convergence faible.

#### 8.5.2 — Mesure de sélection

Si la limite existe, la famille $(\mu_n^\beta)_{n \geq 0}$ est cylindriquement cohérente (par construction). Par le théorème de Kolmogorov :

**Définition 8.6 (Mesure de sélection).** La mesure de sélection $\mu_\beta$ est l'unique mesure sur $(\Omega_B, \Sigma_B)$ dont les marges sont $(\mu_n^\beta)$.

#### 8.5.3 — Hypothèse d'existence

**Hypothèse 8.7 (Spécification locale et existence d'états de Gibbs).** On suppose que :

1. (**Admissibilité locale**) L'ensemble admissible $\Omega_B$ est décrit par des contraintes locales (portée finie) sur les cylindres, et est stable par décalage $\Theta$.
2. (**Localement fini / cutoff**) On travaille à cutoff (par exemple sur $\Omega_{B,\Lambda}$ ou une fenêtre de taille $N$) de sorte que les voisinages causaux de portée finie soient finis et que les normalisations soient bien définies.
3. (**Potentiel de portée finie**) La densité $\ell$ est de portée finie et uniformément bornée (ou, plus généralement, quasi-locale avec une condition de sommabilité suffisante pour contrôler les termes de bord).
4. (**Mesure de référence**) La mesure $\mu_0$ est $\Theta$-stationnaire et non dégénérée au sens où elle attribue une masse strictement positive à tout cylindre admissible de portée finie.

Alors, pour tout $\beta>0$, la famille $\{\mu_N^\beta\}_N$ (ou $\{\mu_{\Lambda}^\beta\}_\Lambda$) est tendue et admet des sous-limites. Toute sous-limite est une mesure de Gibbs au sens des spécifications locales (DLR) associées au potentiel $\beta\ell$. L'unicité n'est pas automatique : plusieurs mesures de Gibbs peuvent coexister (transitions de phase).

> **Cas particulier (toy models).** Lorsque $\Omega_B$ se réduit à un shift symbolique à alphabet fini avec contraintes de type fini, on peut invoquer les résultats classiques de Bowen–Ruelle/Ruelle sur l'existence (et, à haute température, souvent l'unicité) des mesures de Gibbs.

#### 8.5.4 — Stationnarité

**Proposition 8.8.** Sous les hypothèses ci-dessus, toute sous-limite $\mu_\beta$ (et a fortiori toute limite) est $\Theta$-stationnaire.

*Esquisse de preuve.* Pour $N$ fixé, $\mu_N^\beta$ est définie par la densité $\exp(-\beta S_N(\omega))$ où $S_N=\sum_{n=0}^{N-1}\ell(\Theta^n\omega)$. Si l'on décale la fenêtre de $k$ pas, on compare $S_N(\Theta^k\omega)$ et $S_N(\omega)$ : la différence ne porte que sur des termes de bord d'épaisseur contrôlée par la portée de $\ell$. Si $\ell$ est bornée et de portée finie, cette différence est $O(1)$, donc $\frac{1}{N}|S_N(\Theta^k\omega)-S_N(\omega)|\to 0$ lorsque $N\to\infty$. En passant à la limite le long d'une sous-suite, on obtient l'invariance $\mu_\beta=\mu_\beta\circ\Theta^{-1}$ sur les cylindres, donc sur $\Sigma_B$.


---

### 8.6 — Principe variationnel (réalisation de 8.I.γ)

#### 8.6.1 — Action moyenne

Pour une mesure stationnaire $\mu$, l'action moyenne par événement est :

$$\mathcal{A}(\mu) := \int_{\Omega_B} \ell(\omega) \, \mu(d\omega) = \mathbb{E}_\mu[\ell]$$

Par stationnarité :

$$\mathcal{A}(\mu) = \lim_{N \to \infty} \frac{1}{N} \mathbb{E}_\mu[S_N] \quad \text{(p.s. par Birkhoff)}$$

#### 8.6.2 — Entropie métrique

L'entropie métrique (ou entropie de Kolmogorov–Sinai) de $\mu$ pour $\Theta$ est définie relativement à une partition $\mathcal P$ (ici, la partition cylindrique induite par le codage) :

$$h_{\mathcal P}(\mu) := \lim_{n \to \infty} \frac{1}{n} H_\mu(\mathcal{P}_n)$$

où $\mathcal{P}_n := \bigvee_{k=0}^{n-1} \Theta^{-k}\mathcal P$ et $H_\mu$ est l'entropie de Shannon. Dans un cadre symbolique, $h_{\mathcal P}$ coïncide avec l'entropie KS si $\mathcal P$ est génératrice. Par abus de notation, on écrira simplement $h(\mu)$.

**Remarque (dépendance au codage).** Comme $\mathcal P$ provient d'un choix de représentation (jauge), $h(\mu)$ est à comprendre comme un taux d'information dans ce codage. Les énoncés physiques viseront des conclusions robustes sous changements raisonnables de codage ou formulées via des observables intrinsèques.

On restreint l’analyse variationnelle aux mesures stationnaires $\mu \in \mathcal{M}_{\mathrm{stat}}$ telles que $h(\mu)$ soit finie (ce qui est assuré au niveau cutoff sous les hypothèses de portée finie/borne).

**Interprétation :** $h(\mu)$ mesure le "taux de production d'information" par événement.

#### 8.6.3 — Fonctionnelle d'action-information

**Définition 8.9 (Fonctionnelle d'action-information).** Pour $\beta > 0$ :

$$\mathcal{I}_\beta[\mu] := \beta \, \mathcal{A}(\mu) - h(\mu)$$

Ou de manière équivalente, l'énergie libre :

$$\mathcal{F}_\beta(\mu) := \mathcal{A}(\mu) - \frac{1}{\beta} h(\mu) = \frac{1}{\beta} \mathcal{I}_\beta[\mu]$$

Le choix de la fonctionnelle $\mathcal{I}_\beta = \beta \mathcal{A} - h$ et du principe de minimisation est un axiome du niveau II, motivé par l’analogie thermodynamique, et non une conséquence des axiomes du niveau I.

#### 8.6.4 — Principe de sélection

**Principe 8.10 (Sélection par action-information).** Les mesures physiques sont les solutions de :

$$\mu_\beta = \arg\min_{\mu \in \mathcal{M}_{\mathrm{stat}}} \mathcal{I}_\beta[\mu]$$

Ou de manière équivalente :

$$\mu_\beta = \arg\min_{\mu \in \mathcal{M}_{\mathrm{stat}}} \mathcal{F}_\beta(\mu)$$

**Interprétation du compromis :**

| Terme | Rôle | Favorise |
|-------|------|----------|
| $\beta \mathcal{A}(\mu)$ | Coût | Histoires de faible action |
| $-h(\mu)$ | Pénalité entropique | Mesures concentrées |
| Compromis | Équilibre | Faible action + diversité |

#### 8.6.5 — Correspondance Gibbs-variationnel

**Théorème 8.11 (Principe variationnel, admis).** Sous les hypothèses de régularité :

$$\mu_\beta = \arg\min_{\mu \in \mathcal{M}_{\mathrm{stat}}} \mathcal{F}_\beta(\mu)$$

où $\mu_\beta$ est la mesure de Gibbs obtenue par limite thermodynamique.

*Référence (cas symbolique) : résultats de Bowen–Ruelle/Ruelle pour les mesures de Gibbs sur les shifts ; dans le cadre général, voir le formalisme des spécifications locales (DLR).*

---

### 8.7 — Rôle du paramètre $\beta$

#### 8.7.1 — Régimes limites

| Limite | Comportement | Interprétation |
|--------|--------------|----------------|
| $\beta \to 0$ | $\mu_\beta \to \mu_0$ | Pas de sélection (max entropie) |
| $\beta \to \infty$ | concentration sur les minimiseurs (états fondamentaux) de l'action | Sélection "zéro température" ; la limite peut être un mélange (dégénérescence) |
| $\beta$ intermédiaire | Compromis | Régime "physique" |

#### 8.7.2 — Transitions de phase (réalisation de 8.I.ζ)

Pour certaines valeurs critiques $\beta_c$, la mesure $\mu_\beta$ peut présenter des discontinuités :

- **Transition du premier ordre** : Saut dans $\mathcal{A}(\mu_\beta)$ ou $h(\mu_\beta)$
- **Transition du second ordre** : Discontinuité dans les dérivées

Ces transitions séparent des phases macroscopiques qualitativement différentes.

---

### 8.8 — Lien avec la nucléation

#### 8.8.1 — Spectre de nucléation sélectionné

Sous la mesure $\mu_\beta$, les taux de nucléation (chapitre 7) deviennent :

$$\lambda_{[\mathcal{G}]}(\beta) := \mathbb{E}_{\mu_\beta}[X^{[\mathcal{G}]}_0] = \mu_\beta(\mathsf{Nuc}_0([\mathcal{G}]))$$

Le spectre de nucléation $\Lambda_\beta([\mathcal{G}]) := \lambda_{[\mathcal{G}]}(\beta)$ dépend de $\beta$.

#### 8.8.2 — Effet de $\beta$ sur la nucléation

| Régime | Effet sur la nucléation |
|--------|------------------------|
| $\beta$ petit | Haute entropie → nucléation fréquente (si $\ell$ pénalise les germes) |
| $\beta$ grand | Faible action → nucléation selon le coût des germes |

**Observation clé :** En variant $\beta$, on peut passer d'une phase stérile à une phase fertile en univers.

---

### 8.9 — Paramètres et classes d'universalité

#### 8.9.1 — Paramètres du niveau II

Le principe de sélection introduit les paramètres suivants :

| Paramètre | Nature | Rôle |
|-----------|--------|------|
| $\mu_0$ | Mesure | Référence (exploration a priori) |
| $\ell$ | Fonction | Densité d'action locale |
| $\beta$ | Réel > 0 | Force de la sélection |

Ces paramètres ne sont pas dérivés des axiomes du niveau I. Ils définissent une famille de modèles.

#### 8.9.2 — Classes d'universalité

**Définition 8.12 (Classe d'universalité).** Deux triplets $(\mu_0, \ell, \beta)$ et $(\mu_0', \ell', \beta')$ sont dans la même classe d'universalité pour un ensemble d'observables $\mathcal{O}$ si :

$$\mu_\beta^{\mathcal{O}} = \mu_{\beta'}^{\prime \mathcal{O}}$$

(mêmes distributions marginales sur $\mathcal{O}$).

**Interprétation :** Différents choix microscopiques peuvent donner la même physique macroscopique.

---

## Résumé de la structure

```
CHAPITRE 8 — PRINCIPE DE SÉLECTION
│
├── Partie I : NOYAU ONTOLOGIQUE (6 principes)
│   ├── 8.I.α  Action locale              [coût par événement]
│   ├── 8.I.β  Mesure de référence        [exploration a priori μ_0]
│   ├── 8.I.γ  Sélection variationnelle   [min I_β = βA - h]
│   ├── 8.I.δ  Limite thermodynamique     [N → ∞]
│   ├── 8.I.ε  Stationnarité              [μ_β est Θ-invariante]
│   └── 8.I.ζ  Transitions de phase       [β critique]
│
└── Partie II : REPRÉSENTATION (9 sections)
    ├── 8.1  Cadre général                [rappels]
    ├── 8.2  Action locale                [ℓ, S_N]
    ├── 8.3  Mesure de référence          [μ_0]
    ├── 8.4  Mesures de Gibbs             [μ_N^β = W_N/Z_N · μ_0]
    ├── 8.5  Limite thermodynamique       [μ_β = lim μ_N^β]
    ├── 8.6  Principe variationnel        [min F_β(μ)]
    ├── 8.7  Rôle de β                    [régimes, transitions]
    ├── 8.8  Lien avec nucléation         [λ_[G](β)]
    └── 8.9  Classes d'universalité       [équivalence macro]
```

---

## Remarques critiques

### Sur le statut du principe de sélection

Le principe variationnel (8.I.γ) est postulé, pas dérivé. C'est une hypothèse fondamentale du niveau II.

**Questions ouvertes :**
- Pourquoi ce principe plutôt qu'un autre ?
- Peut-on le dériver de considérations plus fondamentales ?

**Justifications possibles :**
1. **Analogie thermodynamique** : La nature "choisit" les états de basse énergie libre
2. **Principe d'économie** : Minimiser le coût tout en préservant la diversité
3. **Sélection anthropique** : Seuls certains $\beta$ permettent des observateurs

### Sur la non-unicité de $\mu_\beta$

Pour certains $\beta$, il peut exister plusieurs mesures minimisant $\mathcal{F}_\beta$ (coexistence de phases).

Dans ce cas, la "mesure physique" est un mélange de ces phases, et la question de laquelle est "réalisée" devient contextuelle (ou anthropique).

### Sur la calculabilité

En pratique, calculer $\mu_\beta$ explicitement est très difficile :
- L'espace $\Omega_B$ est de dimension infinie
- La limite $N \to \infty$ est non triviale
- Les transitions de phase compliquent l'analyse

Des résultats rigoureux nécessiteraient des modèles simplifiés (shifts de type fini sur alphabets finis).

---

## Lien avec les autres chapitres

| Chapitre | Relation avec Ch.8 |
|----------|-------------------|
| Ch.4 (Probabilités) | Fournit $\mathcal{M}_{\mathrm{stat}}$ et la construction de mesures |
| Ch.6 (Phases) | Les phases ergodiques sont les composantes de $\mu_\beta$ |
| Ch.7 (Nucléation) | Le spectre $\Lambda$ dépend de $\mu_\beta$ |
| Ch.9 (Univers) | Les univers émergent dans les phases sélectionnées |
| Ch.3 (Niveau I) | $K$ fournit la base de $\ell$ |

---

## Glossaire du chapitre

| Terme | Définition |
|-------|------------|
| **Densité d'action** $\ell$ | Coût local par événement |
| **Action tronquée** $S_N$ | $\sum_{n=0}^{N-1} \ell(\Theta^n \omega)$ |
| **Mesure de référence** $\mu_0$ | Mesure stationnaire "neutre" |
| **Mesure de Gibbs** $\mu_N^\beta$ | $(W_N / Z_N) \cdot \mu_0$ |
| **Mesure de sélection** $\mu_\beta$ | $\lim_{N \to \infty} \mu_N^\beta$ |
| **Action moyenne** $\mathcal{A}(\mu)$ | $\mathbb{E}_\mu[\ell]$ |
| **Entropie métrique** $h(\mu)$ | Taux d'information par événement |
| **Énergie libre** $\mathcal{F}_\beta$ | $\mathcal{A} - h/\beta$ |

