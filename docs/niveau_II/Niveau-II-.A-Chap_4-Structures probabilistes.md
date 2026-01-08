# Niveau II - Chapitre 4

# A. Structures probabilistes sur l'espace des histoires

------

## Introduction

Le niveau I définit l'espace $\Omega_B$ de toutes les histoires combinatoirement admissibles. Toutes ces histoires ont le même statut ontologique : elles "existent" comme potentialités.

Le niveau II introduit une notion de typicalité : certaines histoires sont plus "probables" que d'autres, au sens d'une mesure sur $\Omega_B$.

> **Point clé :** La probabilité au niveau II n'est pas une probabilité de "se réaliser" (toutes les histoires existent). C'est une mesure de typicalité statistique — une façon de dire quelles structures sont génériques vs exceptionnelles.

Ce chapitre établit le cadre mathématique pour définir de telles mesures. Il construit rigoureusement :
1. Une topologie sur l'espace $\Omega$ des histoires
2. Une structure mesurable compatible avec la causalité
3. Des mesures de typicalité (mesures de Gibbs)
4. Des algèbres d'observables locales

------

## Partie I : Noyau ontologique

### 4.I.α — Principe de typicalité

> **L'espace des histoires admet une notion de typicalité.**

Il existe une structure permettant de distinguer les histoires "génériques" des histoires "exceptionnelles". Cette structure prend la forme d'une mesure de probabilité sur $\Omega_B$.

La mesure n'est pas unique : différentes mesures correspondent à différentes notions de typicalité, donc à différentes "physiques émergentes".

------

### 4.I.β — Principe de localité statistique

> **La typicalité se construit à partir de propriétés locales.**

Une mesure sur $\Omega_B$ est entièrement déterminée par :

- les probabilités de préfixes finis (segments d'histoires de longueur bornée)
- une condition de cohérence (compatibilité par extension)

Il n'existe pas de contrainte "globale" irréductible sur la typicalité : tout se ramène à des propriétés locales le long de la causalité.

------

### 4.I.γ — Principe de compatibilité causale

> **La structure de typicalité respecte l'ordre causal.**

Une mesure admissible sur $\Omega_B$ doit être compatible avec la structure causale définie au niveau I :

- elle ne peut attribuer de poids qu'aux histoires causalement cohérentes
- les probabilités conditionnelles respectent la direction causale

------

### 4.I.δ — Principe de stationnarité

> **Le vide n'a pas de position privilégiée le long de la causalité.**

Une mesure représentant le "vide fondamental" doit être invariante par translation le long du codage causal. La statistique des événements est la même "partout" dans l'histoire.

Ce principe exprime l'homogénéité du vide : il n'y a pas d'"instant zéro" ou de région causale distinguée.

------

### 4.I.ε — Principe de non-dégénérescence

> **Le vide explore effectivement l'espace des possibles.**

Une mesure représentant le vide ne doit pas être concentrée sur un ensemble "trop petit" d'histoires. Elle doit attribuer un poids non nul à une variété suffisante de structures.

Formellement : l'entropie métrique de la mesure est strictement positive.

------

## Partie II : Choix de représentation

### 4.1 — Rappels et codage linéaire

On travaille avec un système $(H_0, \mathcal{R}, K, B)$ satisfaisant les axiomes du niveau I.

**Notation :**

- $\Omega_B$ : histoires admissibles (respectant le crédit $B$)
- $E(\omega)$ : ensemble des événements d'une histoire $\omega$
- $\prec$ : ordre causal sur $E(\omega)$

#### 4.1.1 — Extension linéaire de l'ordre causal

Pour chaque histoire $\omega$, on fixe une extension linéaire $\leq'_\omega$ de l'ordre partiel $\prec$ (existence garantie par le théorème de Szpilrajn).

On énumère alors les événements :

$$\omega^{\mathrm{lin}} = (e_0, e_1, e_2, \ldots)$$

Cette linéarisation est un outil technique sans signification physique. Deux linéarisations différentes de la même histoire représentent la même réalité.

#### 4.1.2 — Espace des histoires linéarisées (choix de jauge)

On note $\mathrm{Lin}(\omega)$ l'ensemble des extensions linéaires possibles de l'ordre causal (partiel) associé à une histoire $\omega$.
Une même histoire possède en général plusieurs linéarisations, correspondant à des permutations d'événements concurrents (non comparables pour $\prec$).

On définit l'espace des histoires linéarisées comme l'ensemble des suites admissibles pouvant provenir d'au moins une histoire :

$$\Omega_B^{\mathrm{lin}} := \bigcup_{\omega\in\Omega_B} \mathrm{Lin}(\omega).$$

Il n'existe pas d'identification canonique $\Omega_B\simeq\Omega_B^{\mathrm{lin}}$.
Pour travailler avec des suites, on peut :

- soit fixer une section (choix de jauge) $\Phi$ qui sélectionne, pour chaque $\omega$, une linéarisation $\Phi(\omega)\in\mathrm{Lin}(\omega)$ ;
- soit considérer la relation d'équivalence $\sim$ sur $\Omega_B^{\mathrm{lin}}$ engendrée par les commutations d'événements concurrents (et par les relabelings / isomorphismes). Dans ce cas, l'histoire physique correspond à une classe $[\omega^{\mathrm{lin}}]$ et l'on a heuristiquement :
$$\Omega_B \simeq \Omega_B^{\mathrm{lin}}/\!\sim.$$

Dans la suite, lorsque nous écrivons une histoire comme une suite $(e_0,e_1,\dots)$, c'est toujours à jauge fixée (ou modulo $\sim$), et les énoncés physiques doivent être invariants sous changement de jauge.

------

### 4.2 — Topologie et espace mesurable des histoires

Cette section établit la structure topologique et mesurable de $\Omega_B$. Nous construisons :
1. Une topologie cylindrique naturelle
2. Une σ-algèbre permettant de définir des mesures
3. Des propriétés topologiques fondamentales (séparation, compacité conditionnelle)

#### 4.2.1 — Cylindres de base

**Motivation :** Deux histoires $\omega, \omega'$ sont "proches" si elles coïncident sur un grand intervalle de temps (nombre de pas causaux).

**Définition 4.1** (Cylindre temporel)

Pour $n \in \mathbb{N}$ et une suite finie d'événements $\mathbf{e} = (e_0, e_1, \ldots, e_n)$, le cylindre temporel est :

$$C_n(\mathbf{e}) = \{\omega \in \Omega : \omega|_{[0,n]} = \mathbf{e}\}$$

c'est-à-dire l'ensemble des histoires qui coïncident avec $\mathbf{e}$ sur les $n$ premiers pas.

**Propriétés :**

1. $C_0(e_0) = \{\omega : \omega(0) = e_0\}$
2. $C_{n+1}(\mathbf{e}, e_{n+1}) \subseteq C_n(\mathbf{e})$ (hiérarchie)
3. $\bigcap_{n=0}^\infty C_n(\omega|_{[0,n]}) = \{\omega\}$ (séparation)

**Définition 4.2** (Cylindre local intrinsèque)

Dans un cadre strictement relationnel (classes d'isomorphisme), une "région" doit être définie sans identifiants absolus.
On introduit donc une région intrinsèque $\mathfrak{R}$ comme un couple :

- $P$ : un motif enraciné (un sous-hypergraphe fini avec éventuellement une frontière marquée),
- $\ell\in\mathbb{N}$ : une échelle intrinsèque (rayon) mesurée par distance de graphe / distance causale locale.

Pour une fenêtre d'indices $[n_1,n_2]$ (pas internes), une histoire locale $\sigma$ spécifie, à isomorphisme près, la restriction de l'histoire aux événements dont l'action (Read/Write) intersecte le voisinage intrinsèque $\mathcal{N}_\ell(P)$ au cours de $[n_1,n_2]$.

Le cylindre local intrinsèque est alors :

$$C_{\mathfrak{R},[n_1,n_2]}(\sigma)
= \{\omega\in\Omega_B : \omega\text{ induit la même histoire locale }\sigma\text{ sur }\mathfrak{R}\times[n_1,n_2]\}.$$

**Interprétation :** Histoires qui coïncident (à relabeling près) sur une fenêtre locale définie intrinsèquement.

> **Remarque (jauge étiquetée) :** Si l'on travaille temporairement dans une représentation avec un ensemble de sommets fixé $V$ (étiquettes), on peut retrouver une écriture du type $R\subseteq V$.
Les énoncés physiques doivent toutefois rester invariants sous isomorphisme / changement d'étiquetage.

#### 4.2.2 — Topologie cylindrique

**Définition 4.3** (σ-algèbre cylindrique)

La σ-algèbre cylindrique $\mathcal{F}_{\text{cyl}}$ sur $\Omega$ est la plus petite σ-algèbre contenant tous les cylindres :

$$\mathcal{F}_{\text{cyl}} = \sigma(\{C_n(\mathbf{e}) : n \in \mathbb{N}, \mathbf{e} \text{ suite finie}\})$$

**Proposition 4.1** ($\mathcal{F}_{\text{cyl}}$ est bien définie)

Par construction de σ-algèbre (théorème standard), $\mathcal{F}_{\text{cyl}}$ satisfait :

1. $\Omega \in \mathcal{F}_{\text{cyl}}$
2. $A \in \mathcal{F}_{\text{cyl}} \Rightarrow A^c \in \mathcal{F}_{\text{cyl}}$
3. $(A_n)_{n \in \mathbb{N}} \subseteq \mathcal{F}_{\text{cyl}} \Rightarrow \bigcup_n A_n \in \mathcal{F}_{\text{cyl}}$

**Définition 4.4** (Topologie cylindrique)

On munit $\Omega$ de la topologie cylindrique $\mathcal{T}_{\text{cyl}}$ engendrée par les cylindres :

Une partie $U \subseteq \Omega$ est ouverte si elle s'écrit comme union de cylindres :

$$U = \bigcup_{\alpha \in A} C_n(\mathbf{e}_\alpha)$$

**Base de la topologie :**

$$\mathcal{B} = \{C_n(\mathbf{e}) : n \in \mathbb{N}, \mathbf{e}\}$$

#### 4.2.3 — Propriétés topologiques

**Théorème 4.1** (Séparation)

L'espace $(\Omega, \mathcal{T}_{\text{cyl}})$ est séparé (Hausdorff) : pour tout $\omega \neq \omega'$, il existe des ouverts disjoints $U, V$ tels que $\omega \in U$ et $\omega' \in V$.

**Preuve :**

1. Soit $\omega \neq \omega'$. Il existe $n_0$ tel que $\omega|_{[0,n_0]} \neq \omega'|_{[0,n_0]}$.

2. Posons $U = C_n(\omega|_{[0,n_0]})$ et $V = C_n(\omega'|_{[0,n_0]})$.

3. Par définition, $\omega \in U$ et $\omega' \in V$.

4. $U \cap V = \varnothing$ car $\omega|_{[0,n_0]} \neq \omega'|_{[0,n_0]}$.

5. Donc $(\Omega, \mathcal{T}_{\text{cyl}})$ est séparé.

**Théorème 4.2** (Compacité conditionnelle)

Si on restreint $\Omega$ aux histoires satisfaisant :

- **Volume borné** : $|V_n| \leq Cn^d$ (croissance polynomiale)
- **Densité bornée** : nombre d'hyperarêtes par nœud $\leq D$

alors $\Omega_{\text{borné}} \subseteq \Omega$ est séquentiellement compact pour $\mathcal{T}_{\text{cyl}}$.

**Preuve (Esquisse via Tychonoff) :**

1. Chaque configuration $H_n$ appartient à un espace fini $\mathcal{H}_n$ (avec les bornes).

2. $\Omega_{\text{borné}} \subseteq \prod_n \mathcal{H}_n$ (produit d'espaces finis).

3. Chaque $\mathcal{H}_n$ est compact (fini).

4. Par Tychonoff, $\prod_n \mathcal{H}_n$ est compact.

5. $\Omega_{\text{borné}}$ est un sous-ensemble fermé (contraintes de cohérence).

6. Donc $\Omega_{\text{borné}}$ est compact. 

**Remarque :** Cette compacité sera cruciale pour prouver l'existence de phases stationnaires au niveau III.

#### 4.2.4 — Distance et voisinages

**Définition 4.5** (Distance de Fréchet discrète)

On définit une pseudo-distance sur $\Omega$ :

$$d_{\text{Fréchet}}(\omega, \omega') = \sum_{n=0}^\infty \frac{1}{2^n} \cdot \delta_n(\omega, \omega')$$

où :

$$\delta_n(\omega, \omega') = \begin{cases}
0 & \text{si } \omega|_{[0,n]} = \omega'|_{[0,n]} \\
1 & \text{sinon}
\end{cases}$$

**Proposition 4.2** (Métrisabilité partielle)

Sur $\Omega_{\text{borné}}$, la distance $d_{\text{Fréchet}}$ :

1. Est finie : $d_{\text{Fréchet}}(\omega, \omega') \leq 2$ par construction (série géométrique bornée)
2. Satisfait $d(\omega, \omega) = 0$
3. Est symétrique : $d(\omega, \omega') = d(\omega', \omega)$
4. Induit la topologie cylindrique car les boules $B(\omega, 1/2^n)$ coïncident avec les cylindres $C_n(\omega|_{[0,n]})$.

**Remarque :** La fonction $d$ ci-dessus est la métrique de préfixe (type Cantor) sur l'espace des suites : elle vérifie l'inégalité triangulaire (même sous forme d'ultramétrique).
En revanche, si l'on identifie des suites par une équivalence de jauge (commutations d'événements concurrents, relabelings / isomorphismes), $d$ descend naturellement en pseudo-métrique sur le quotient.


#### 4.2.5 — Alphabet des événements et cylindres de préfixes

Un événement élémentaire est un quadruplet $e = (H, r, \iota, H')$.

L'alphabet $\mathcal{E}_{\mathrm{adm}}$ est l'ensemble des événements pouvant apparaître dans au moins une histoire de $\Omega_B$.

Une histoire linéarisée est une suite :

$$\omega^{\mathrm{lin}} = (e_0, e_1, e_2, \ldots) \in \mathcal{E}_{\mathrm{adm}}^{\mathbb{N}}$$

satisfaisant les contraintes de chaînage et de crédit.

**Définition 4.6** (Cylindre de préfixe)

Pour un préfixe admissible $\mathbf{e}^{(n)} = (e_0, \ldots, e_{n-1})$, le cylindre associé est :

$$C[\mathbf{e}^{(n)}] := \{\omega \in \Omega_B \mid \omega_k = e_k \text{ pour } 0 \leq k < n\}$$

Les cylindres forment une base de la topologie produit restreinte à $\Omega_B$.

#### 4.2.6 — σ-algèbre mesurable

**Définition 4.7** (σ-algèbre cylindrique sur $\Omega_B$)

La σ-algèbre cylindrique $\Sigma_B$ est la plus petite σ-algèbre contenant tous les cylindres :

$$\Sigma_B := \sigma\bigl(\{C[\mathbf{e}^{(n)}] \mid n \in \mathbb{N}, \mathbf{e}^{(n)} \text{ admissible}\}\bigr)$$

**Propriétés :**

- $(\Omega_B, \Sigma_B)$ est un espace mesurable standard
- Tout événement dépendant d'un nombre fini d'événements est mesurable

------

### 4.3 — Construction de mesures par cohérence cylindrique

Cette section développe la construction rigoureuse de mesures de probabilité sur $\Omega_B$ via le théorème de Kolmogorov, puis construit explicitement des mesures de type Gibbs.

#### 4.3.1 — Distributions sur les préfixes

Pour chaque $n \in \mathbb{N}$, soit $\Omega_B^{(n)}$ l'ensemble des préfixes admissibles de longueur $n$.

Une distribution sur les préfixes est une famille $(\mu_n)_{n \geq 0}$ où :

$$\mu_n : \Omega_B^{(n)} \to [0, 1], \quad \sum_{\mathbf{e}^{(n)} \in \Omega_B^{(n)}} \mu_n(\mathbf{e}^{(n)}) = 1$$

#### 4.3.2 — Condition de cohérence

**Définition 4.8** (Cohérence cylindrique)

La famille $(\mu_n)$ est cylindriquement cohérente si :

$$\mu_n(\mathbf{e}^{(n)}) = \sum_{e_n} \mu_{n+1}(\mathbf{e}^{(n)}, e_n)$$

pour tout $n$ et tout préfixe $\mathbf{e}^{(n)}$, où la somme porte sur les extensions admissibles.

**Interprétation :** La loi à longueur $n$ est la marginale de la loi à longueur $n+1$.

#### 4.3.3 — Théorème d'extension (réalisation de 4.I.β)

**Théorème 4.3** (Théorème standard de théorie de la mesure de Kolmogorov, 1933)

Soit $(\mu_n)$ une famille cylindriquement cohérente. Il existe une unique mesure de probabilité $\mu$ sur $(\Omega_B, \Sigma_B)$ telle que :

$$\mu(C[\mathbf{e}^{(n)}]) = \mu_n(\mathbf{e}^{(n)})$$

pour tout $n$ et tout préfixe admissible.

Ce théorème garantit que la typicalité se construit bien à partir de propriétés locales (principe 4.I.β).

#### 4.3.4 — Mesures de Gibbs : construction rigoureuse (sur préfixes / spécifications)

Nous construisons une classe importante de mesures de typicalité, de type Gibbs, en veillant à rester dans un cadre bien défini sur des objets finis (cylindres), puis en discutant l'extension.

---

##### (i) Action combinatoire d'un préfixe

**Définition 4.9** (Action d'un préfixe)

Pour un préfixe admissible $\mathbf e^{(n)}=(e_0,\dots,e_{n-1})\in\Omega_B^{(n)}$, on définit l'action cumulée :

$$I_n[\mathbf e^{(n)}] := \sum_{k=0}^{n-1} \ell(e_k),$$

où $\ell(e)$ est le coût (longueur / coût local) de l'événement $e$.

> **Remarque :** Sur une histoire infinie, la somme $\sum_{k\ge 0}\ell(e_k)$ diverge typiquement. C'est pourquoi la construction se fait d'abord sur les cylindres (longueur finie), ou via une action par unité de temps interne (densité) lorsque cela a du sens.

---

##### (ii) Mesure de Gibbs à longueur finie

Soit $\mu_{0,n}$ une mesure de référence sur $\Omega_B^{(n)}$ (par exemple uniforme sur un ensemble tronqué, ou induite par un noyau markovien à $\beta=0$).

**Définition 4.10** (Gibbs sur préfixes)

Pour $\beta>0$, on définit la distribution de Gibbs sur les préfixes de longueur $n$ par :

$$\mu_{\beta,n}(\mathbf e^{(n)}) :=
\frac{1}{Z_{\beta,n}}\, e^{-\beta I_n[\mathbf e^{(n)}]}\, \mu_{0,n}(\mathbf e^{(n)}),$$

avec fonction de partition finie :

$$Z_{\beta,n} := \sum_{\mathbf e^{(n)}\in\Omega_B^{(n)}} e^{-\beta I_n[\mathbf e^{(n)}]}\, \mu_{0,n}(\mathbf e^{(n)}).$$

Cette définition est toujours bien posée dès que $\Omega_B^{(n)}$ est fini ou que la somme converge (en pratique : cutoff de complexité, voir niveau I.A).

---

##### (iii) Extension à une mesure sur $\Omega_B$

Pour obtenir une mesure $\mu_\beta$ sur $(\Omega_B,\Sigma_B)$, il faut une cohérence cylindrique de la famille $(\mu_{\beta,n})_{n\ge 0}$ (Définition 4.8), afin d'appliquer le théorème de Kolmogorov (Théorème 4.3).

Deux stratégies standard :

1. **Construction markovienne (préférée ici)** : choisir un noyau local $T_\beta(e\mid H)$ et définir
   $$\mu_{\beta,n}(\mathbf e^{(n)}) := \mu_{\beta,0}([H_0])\,\prod_{k=0}^{n-1} T_\beta(e_k\mid H_k).$$
   La cohérence est alors automatique (Section 4.4).

2. **Spécifications locales (DLR) / limite thermodynamique** : définir des lois de Gibbs sur des cylindres (ou boîtes locales) avec conditions au bord, puis prendre une limite lorsque la fenêtre s'élargit. Cette approche est utile lorsque l'on veut modéliser des phases et de la non-unicité de la mesure.

---

##### (iv) Concentration à basse "température" (énoncé à longueur finie)

**Proposition 4.4** (Concentration sur les préfixes minimaux)

Fixons $n$ et supposons $\Omega_B^{(n)}$ fini. Soit $I_{n,\min}:=\min\{I_n[\mathbf e^{(n)}]\}$ et
$$\Omega_{n,\epsilon}:=\{\mathbf e^{(n)} : I_n[\mathbf e^{(n)}]\le I_{n,\min}+\epsilon\}.$$
Alors, pour tout $\epsilon>0$ :
$$\mu_{\beta,n}(\Omega_{n,\epsilon}) \xrightarrow[\beta\to\infty]{} 1.$$

**Idée de preuve :** majoration par le rapport entre contributions $e^{-\beta(I_{n,\min}+\epsilon)}$ et $e^{-\beta I_{n,\min}}$ dans $Z_{\beta,n}$ (argument standard de Gibbs). 

> **Attention :** cet énoncé n'implique pas, à lui seul, l'existence ou l'unicité d'une mesure de Gibbs sur histoires infinies : cela dépend du passage à la limite / des spécifications et sera précisément ce qui encode l'existence de phases au niveau II.

------

### 4.4 — Mesures compatibles avec la dynamique locale

#### 4.4.1 — Noyaux de transition locaux

**Définition 4.11** (Noyau de transition local)

Un noyau de transition local est une application :

$$T : \mathcal{C} \to \mathrm{Prob}(\mathcal{E}_{\mathrm{adm}})$$

telle que, pour toute configuration $H$ :

- $T(\cdot | H)$ est une loi de probabilité sur $\mathcal{E}(H) = \{e = (H, r, \iota, H') \mid r \in \mathcal{R}, \iota \in \mathrm{Occ}(r, H)\}$
- $\sum_{e \in \mathcal{E}(H)} T(e | H) = 1$

**Interprétation :** $T(e | H)$ est le poids relatif de l'événement $e$ parmi tous ceux applicables à $H$.

#### 4.4.2 — Mesure markovienne induite

À partir d'un noyau $T$, on construit la famille $(\mu_n)$ par :

$$\mu_n(\mathbf{e}^{(n)}) := \prod_{k=0}^{n-1} T(e_k | H_k)$$

où $H_0 \xrightarrow{e_0} H_1 \xrightarrow{e_1} \cdots \xrightarrow{e_{n-1}} H_n$.

**Proposition 4.3** (Cohérence markovienne)

Cette famille est cylindriquement cohérente. La mesure $\mu_T$ associée est appelée mesure markovienne.

**Remarque :** La propriété markovienne signifie que le poids d'un événement ne dépend que de la configuration courante, pas de l'histoire passée.

------

### 4.5 — Mesures pondérées par la complexité

Le principe de coût combinatoire (niveau I) suggère de pondérer les événements par leur variation de complexité.

#### 4.5.1 — Poids locaux

Pour un événement $e = (H, r, \iota, H')$, on rappelle :

$$\Delta K(e) := K(H') - K(H)$$

On définit un fonctionnel de poids $W : \mathbb{R} \to (0, \infty)$, typiquement :

$$W(\Delta K) = \exp(-\alpha \cdot \Delta K)$$

avec $\alpha \in \mathbb{R}$ un paramètre.

La forme exponentielle de $W(\Delta K)$ est un choix de modélisation de type Gibbs, inspiré de la physique statistique.

#### 4.5.2 — Noyau de type Gibbs

On définit le poids non normalisé :

$$\tilde{T}(e | H) := W(\Delta K(e)) \cdot \mathbf{1}_{e \in \mathcal{E}(H)}$$

et la fonction de partition locale :

$$Z(H) := \sum_{e \in \mathcal{E}(H)} W(\Delta K(e))$$

Le noyau normalisé est :

$$T(e | H) := \frac{W(\Delta K(e))}{Z(H)}$$

**Interprétation selon $\alpha$ :**

| Valeur de $\alpha$ | Comportement                                    |
| ------------------ | ----------------------------------------------- |
| $\alpha > 0$       | Favorise les diminutions de complexité          |
| $\alpha = 0$       | Uniforme (toutes les règles équiprobables)      |
| $\alpha < 0$       | Favorise les augmentations de complexité        |

#### 4.5.3 — Lien avec la thermodynamique

L'analogie formelle avec la physique statistique :

| Thermodynamique       | Théorie hypergraphique                |
| --------------------- | ------------------------------------- |
| Énergie $E$           | Complexité $K(H)$                     |
| Température $T$       | $1/\alpha$ (température combinatoire) |
| Partition canonique   | Mesure $\mu_\alpha$                   |
| Minimum de $F = E-TS$ | Sélection d'histoires typiques        |

------

### 4.6 — Algèbres d'observables locales

Cette section introduit une structure algébrique sur les observables, permettant de définir rigoureusement les mesures et les corrélations.

#### 4.6.1 — Observables mesurables

**Définition 4.12** (Observable)

Un observable est une fonction mesurable :

$$A : \Omega_B \to \mathbb{R}$$

c'est-à-dire $A^{-1}(B) \in \Sigma_B$ pour tout borélien $B \subseteq \mathbb{R}$.

**Exemples :**

1. **Compteurs** : $N_r(\omega) = |\{n : e_n \text{ applique la règle } r\}|$
2. **Densités** : $\rho_T(\omega) = \frac{|V_T|}{T}$ (nombre de nœuds au temps $T$)
3. **Énergies** : $K_T(\omega) = K(H_T)$ (complexité à l'instant $T$)

#### 4.6.2 — Localité (intrinsèque) et corrélations

**Définition 4.13** (Observable local)

Un observable $A$ est $(\mathfrak R, T)$-local s'il ne dépend que d'une fenêtre locale intrinsèque $\mathfrak R$ (Définition 4.2) et d'un horizon temporel interne $T$.
Autrement dit, il existe une fonction mesurable $f$ telle que :

$$A(\omega)=f\big(\omega\vert_{\mathfrak R\times[0,T]}\big),$$

où la restriction est prise à isomorphisme près (relabeling).

**Notation :** On note $\mathcal{A}_{\mathfrak R,T}$ l'ensemble des observables $(\mathfrak R,T)$-locaux.

---

##### Localité n'implique pas indépendance

La localité (au sens : *support restreint*) ne suffit pas à garantir l'indépendance statistique :
en général, une mesure $\mu$ sur $\Omega_B$ peut induire des corrélations entre régions disjointes via des contraintes globales, des conditions initiales, ou la dynamique.

Deux formulations correctes (selon le degré d'hypothèses) :

1. **Indépendance exacte (cas particulier)** : si $\mu$ factorise effectivement entre deux régions (mesure produit ou découplage imposé), alors pour $A_i\in\mathcal A_{\mathfrak R_i,T_i}$ :
   $$\mathbb E_\mu[A_1A_2]=\mathbb E_\mu[A_1]\,\mathbb E_\mu[A_2].$$

2. **Décroissance des corrélations (hypothèse de phase)** : on peut postuler une propriété de *mixing* sous la forme :
   $$\big|\mathbb E_\mu[A_1A_2]-\mathbb E_\mu[A_1]\,\mathbb E_\mu[A_2]\big|
   \le \rho\big(d(\mathfrak R_1,\mathfrak R_2)\big)\,\|A_1\|\,\|A_2\|,$$
   où $d(\mathfrak R_1,\mathfrak R_2)$ est une distance intrinsèque (graphe/causal) et $\rho(t)\to 0$ quand $t\to\infty$.

Dans le cas markovien (Section 4.4), on peut aussi obtenir des formes d'indépendance conditionnelle : deux régions sont indépendantes conditionnellement aux données sur une frontière causale / un "bord" qui médie les dépendances.
#### 4.6.3 — C*-algèbre d'observables

**Définition 4.14** (Algèbre locale)

Pour une région intrinsèque $\mathfrak R$ (Définition 4.2), l'algèbre locale $\mathcal{A}_{\mathfrak R}$ est la C*-algèbre engendrée par les observables $(\mathfrak R, T)$-locaux pour tout $T$ :

$$\mathcal{A}_{\mathfrak R} = \overline{\bigcup_T \mathcal{A}_{\mathfrak R,T}}$$

où la clôture est prise pour la norme sup (ou, une fois $\mu$ fixée, pour la norme $L^\infty(\Omega_B,\mu)$).

> **Remarque :** À ce stade, $\mathcal{A}_{\mathfrak R}$ est une algèbre de fonctions avec multiplication ponctuelle : elle est donc commutative.

**Structure de C*-algèbre :**

1. **Addition** : $(A + B)(\omega) = A(\omega) + B(\omega)$
2. **Multiplication** : $(AB)(\omega) = A(\omega) \cdot B(\omega)$
3. **Involution** : $A^*(\omega) = \overline{A(\omega)}$
4. **Norme** : $\|A\| = \sup_\omega |A(\omega)|$

#### 4.6.4 — Commutation : statut au niveau II

**Proposition 4.5** (Commutation dans l'algèbre commutative)

Dans le cadre présent, les observables sont des fonctions mesurables $A: \Omega_B\to\mathbb R$ et l'algèbre est munie de la multiplication ponctuelle :
$$(AB)(\omega)=A(\omega)B(\omega).$$
Par conséquent, pour toutes $A,B$ (locales ou non), on a :
$$[A,B]=AB-BA=0.$$

**Remarque :** La commutation "microcausale" (les observables de régions spacelike séparées commutent *dans une algèbre non commutative*) est un fait non trivial en théorie quantique des champs. Dans notre architecture, la non-commutativité n'apparaît qu'au niveau III, lorsque l'on passe d'une description ontologique sur $\Omega_B$ à une description opérationnelle optimale pour un observateur interne.

------

### 4.7 — Stationnarité et invariances

#### 4.7.1 — Opérateur de décalage temporel

**Définition 4.15** (Translation causale)

L'opérateur de décalage $\Theta : \Omega_B \to \Omega_B$ est défini par :

$$(\Theta \omega)_n := \omega_{n+1}$$

c'est-à-dire qu'on "oublie" le premier événement et on décale tous les autres.

> **Remarque (jauge / condition initiale) :** Strictement, $\Theta$ agit sur les histoires linéarisées à jauge fixée (ou sur les classes modulo commutations). Elle transforme aussi la condition initiale : la queue de $\omega$ commence à la configuration $H_1$ au lieu de $H_0$. La stationnarité (définie ci-dessous) doit donc être comprise comme une propriété d'un régime où aucun instant interne n'est privilégié.

**Propriétés :**

- $\Theta$ préserve l'admissibilité (si $\omega \in \Omega_B$, alors $\Theta \omega \in \Omega_B$)
- $\Theta$ est mesurable pour $\Sigma_B$

#### 4.7.2 — Mesures stationnaires

**Définition 4.16** (Mesure stationnaire)

Une mesure $\mu$ sur $(\Omega_B, \Sigma_B)$ est stationnaire si elle est invariante par $\Theta$ :

$$\mu(\Theta^{-1}(A)) = \mu(A) \quad \forall A \in \Sigma_B$$

**Équivalent :** Pour tout observable $A$ :

$$\mathbb{E}_\mu[A \circ \Theta] = \mathbb{E}_\mu[A]$$

**Interprétation :** La statistique des histoires est homogène le long de la causalité (réalisation de 4.I.δ).

**Proposition 4.4** (Stationnarité des mesures de Gibbs)

Si la mesure de référence $\mu_0$ est stationnaire, alors la mesure de Gibbs $\mu_\beta$ est également stationnaire.

**Preuve :**

1. L'action est additive : $I[\omega] = \sum_n \ell(e_n)$

2. Donc : $I[\Theta \omega] = I[\omega] - \ell(e_0)$

3. Pour que $\mu_\beta$ soit stationnaire, il faut que $\mu_0$ le soit et que le facteur de Boltzmann soit invariant à un décalage près (absorbé dans la normalisation).

4. Ceci est garanti si $\mu_0$ est stationnaire. 
