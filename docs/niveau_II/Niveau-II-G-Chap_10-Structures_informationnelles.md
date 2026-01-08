# Chapitre 10 — Structures informationnelles, témoins et observateurs

---

## Introduction

Les chapitres précédents ont défini les univers comme des structures causales émergentes. Mais une structure causale "nue" ne contient pas de notion d'information ou d'observation.

Ce chapitre ajoute une couche informationnelle au formalisme :
- Chaque "cellule" de la structure peut porter un état d'information discret
- Les règles de réécriture incluent des mises à jour informationnelles
- Des témoins enregistrent des faits sur l'environnement
- Des observateurs sont des motifs capables de maintenir des enregistrements stables

> **Point clé :** L'information est classique (ensembles finis d'états, pas de superposition). La "décohérence" apparaît comme redondance des témoins, non comme effondrement quantique.

---

## Partie I : Noyau ontologique

### 10.I.α — Principe de couche informationnelle

> **La structure combinatoire peut porter de l'information.**

Au-delà de la structure topologique (hypergraphe), chaque élément de la configuration peut être associé à un état d'information discret. Cette couche est distincte de la structure : elle se superpose sans la modifier.

---

### 10.I.β — Principe de localité informationnelle

> **L'information est stockée localement et se propage localement.**

L'information est attachée à des "cellules" (sommets, arêtes, incidences...) de la configuration. Les mises à jour informationnelles ne dépendent que des cellules locales impliquées dans un événement.

---

### 10.I.γ — Principe de dynamique augmentée

> **Les règles de réécriture incluent des transformations informationnelles.**

Une "règle augmentée" spécifie non seulement comment la structure change, mais aussi comment l'information est copiée, transformée ou initialisée lors de ce changement.

---

### 10.I.δ — Principe de témoignage

> **L'état informationnel d'une région peut témoigner d'un fait structurel.**

Un ensemble de cellules est un "témoin" d'un motif si son état informationnel encode de manière fiable la présence ou l'absence de ce motif. Le témoignage peut être persistant (stable dans le temps) ou transitoire.

---

### 10.I.ε — Principe de redondance et objectivité

> **Un fait devient "objectif" lorsqu'il est témoigné de manière redondante.**

Si de nombreuses régions disjointes contiennent des témoins cohérents du même fait, ce fait devient pratiquement irréversible : une perturbation locale ne peut effacer tous les témoins. C'est la version combinatoire de la "décohérence classique".

---

### 10.I.ζ — Principe d'observateur

> **Un observateur est un motif informationnel capable d'enregistrer son environnement.**

Un observateur est une région structurelle + informationnelle satisfaisant :
1. Capacité de mémoire suffisante
2. Couplage avec l'environnement (acquisition de témoins)
3. Stabilité interne (persistance des enregistrements)

Cette définition est purement structurelle — elle ne présuppose ni conscience ni interprétation.

---

## Partie II : Choix de représentation

### 10.1 — Couche d'information sur les configurations

#### 10.1.1 — Cellules informationnelles

Pour une configuration structurelle $H$, on définit un ensemble de cellules informationnelles $C_\Sigma(H)$.

**Schémas possibles :**

| Schéma | Définition de $C_\Sigma(H)$ |
|--------|---------------------------|
| Nœuds | $C_\Sigma(H) = V(H)$ |
| Hyperarêtes | $C_\Sigma(H) = E(H)$ |
| Mixte | $C_\Sigma(H) = V(H) \cup E(H)$ |
| Enrichi | $C_\Sigma(H) = V(H) \cup E(H) \cup I(H)$ |

où $I(H)$ désigne les incidences (paires $(v, e)$ avec $v \in S(e)$).

**Hypothèse 10.1 (Foncteur de cellules).** L'application $H \mapsto C_\Sigma(H)$ est fonctorielle : un isomorphisme structurel induit une bijection correspondante entre cellules.

**Invariance (relabeling).** Toutes les notions définies dans ce chapitre (cellules, témoins, redondance, observateurs) sont entendues au niveau des classes d’isomorphisme : un isomorphisme structural entre $H$ et $H'$ transporte canoniquement les cellules et les états, et les prédicats sont invariants sous ce transport.


#### 10.1.2 — Espaces d'information locaux

**Définition 10.2 (Espace d'information).** Pour chaque cellule $c \in C_\Sigma(H)$, on associe un espace d'information local $\mathcal{S}_c$ (ensemble fini).

La capacité informationnelle de $c$ est :

$$\kappa(c) := |\mathcal{S}_c| \in \mathbb{N}$$

**Convention (État neutre).** Chaque $\mathcal{S}_c$ contient un élément distingué $\omega_0^{(c)}$ — l'état par défaut des cellules nouvellement créées.

##### Option : fibre octonionique comme espace d'information local

Cette section propose un choix de représentation (optionnel) pour les espaces d'information locaux $\mathcal{S}_c$, compatible avec l'objectif du niveau I : simplicité + ouverture, puis enrichissement progressif par filtres.

L'idée est d'utiliser la couche informationnelle pour porter une structure interne de type octonionique, sans modifier la dynamique structurelle de niveau I : si l'on "oublie" l'information, on retrouve exactement l'évolution du substrat.

###### (a) Version minimale (strictement finie) : directions octonioniques

On fixe un alphabet interne :

$$\mathcal{U} := \{0, \pm e_1, \ldots, \pm e_7\}$$

où $0$ est l'état neutre, et $\pm e_i$ sont des "directions imaginaires" (symboliques).  
On prend alors, pour certaines cellules $c$ (par exemple les nœuds) :

$$\mathcal{S}_c^{(\mathbb{O})} := \mathcal{S}_c^{(\mathrm{base})} \times \mathcal{U} \times \mathcal{G},$$

où :

- $\mathcal{S}_c^{(\mathrm{base})}$ est l'information déjà prévue (témoin, tag, registre, etc.),
- $\mathcal{U}$ code un axe interne visible (utile pour définir une projection complexe),
- $\mathcal{G}$ est un petit ensemble fini d'automorphismes/discrétisations de repère (permutations + signes compatibles avec le plan de Fano), servant à comparer/transport­er des directions internes entre cellules.

Cette version est volontairement frugale : elle ne contient pas des "réels" ni des coefficients continus ; elle fournit un socle combinatoire pour l'émergence de secteurs observables.

###### (b) Version enrichie (toujours finie) : coefficients bornés

Si l'on veut une information interne plus expressive, on peut remplacer $\mathcal{U}$ par un ensemble fini de "petits octonions" à coefficients bornés :

$$\mathcal{O}_{M} := \left\{a_0 + \sum_{i=1}^7 a_i e_i \;:\; a_j \in \{-M,\ldots,M\}\right\}$$

et poser $\mathcal{S}_c^{(\mathbb{O})} := \mathcal{S}_c^{(\mathrm{base})}\times \mathcal{O}_M \times \mathcal{G}$.

Ici, $M$ joue le rôle de cutoff informationnel. Les limites vers des structures continues (si nécessaires plus tard) relèvent d'un coarse-graining / d'une limite d'échelle, et non d'un choix micro.

###### (c) Mise à jour locale : règles augmentées compatibles

Pour une règle structurelle $r$, une règle augmentée $\widehat r=(r,U_r)$ met à jour les états internes en restant locale. Exemples typiques de $U_r$ :

- **Copie/propagation de témoins** : duplication d'une partie de $\mathcal{S}_c^{(\mathrm{base})}$ vers des cellules voisines (mécanisme de redondance).
- **Alignement d'axes** : si une interaction locale favorise un secteur observable stable, on peut mettre à jour $u\in\mathcal{U}$ par règle de majorité (ou par minimisation d'un coût local) entre cellules adjacentes.
- **Transport de repère** : mise à jour de l'élément $\mathcal{G}$ pour préserver la cohérence d'identification des directions internes.

**Point crucial :** cette couche interne n'a pas vocation à fournir des amplitudes fondamentales ; elle fournit une mémoire interne / structure de symétrie qui pourra être partiellement "vue" via une projection d'observation (chapitre 12).

#### 10.1.3 — Configurations informationnelles

**Définition 10.3 (Espace régional).** Pour $U \subseteq C_\Sigma(H)$ fini :

$$\mathcal{S}_U := \prod_{c \in U} \mathcal{S}_c, \quad \kappa(U) := |\mathcal{S}_U| = \prod_{c \in U} \kappa(c)$$

Une configuration informationnelle sur $U$ est un élément $s_U = (s_c)_{c \in U} \in \mathcal{S}_U$.

**Définition 10.4 (Configuration augmentée).** Une configuration augmentée est un couple :

$$\widehat{H} := (H, s)$$

où $H$ est la structure et $s \in \mathcal{S}_{C_\Sigma(H)}$ est la configuration informationnelle globale.

L'espace des configurations augmentées est noté $\mathcal{C}_{\mathrm{aug}}$.

---

### 10.2 — Dynamique augmentée (réalisation de 10.I.γ)

#### 10.2.1 — Règles augmentées

Rappel : une règle structurale $r \in \mathcal{R}$ spécifie un motif gauche $L_r$, un motif droit $R_r$, et leur relation.

**Définition 10.5 (Règle augmentée).** Une règle augmentée $\widehat{r}$ associée à $r$ consiste en :

1. La règle structurale $r$
2. Une application de mise à jour :
   $$U_r : \mathcal{S}_{C_\Sigma(L_r)} \to \mathcal{S}_{C_\Sigma(R_r)}$$

#### 10.2.2 — Application d'une règle augmentée

Pour appliquer $\widehat{r}$ à $\widehat{H} = (H, s)$ :

1. **Partie structurelle** : Appliquer $r$ à une occurrence de $L_r$ dans $H$, produisant $H'$
2. **Partie informationnelle** :
   - Cellules hors du support : information conservée
   - Cellules de $R_r$ : mise à jour via $U_r$
   - Cellules nouvellement créées : initialisées à $\omega_0^{(c)}$ (sauf si $U_r$ spécifie autrement)

#### 10.2.3 — Évolution augmentée

On obtient une dynamique sur $\mathcal{C}_{\mathrm{aug}}$ :

$$\widehat{H}_0 \xrightarrow{\widehat{e}_0} \widehat{H}_1 \xrightarrow{\widehat{e}_1} \widehat{H}_2 \xrightarrow{\widehat{e}_2} \cdots$$

où chaque événement augmenté est :

$$\widehat{e}_n = (\widehat{H}_n, r_n, \iota_n, \widehat{H}_{n+1})$$

**Remarque importante :** La couche informationnelle n'affecte pas le crédit $B$ ni la complexité $K$. Elle est une structure auxiliaire du niveau II. Par construction, nous imposons que la dynamique structurelle et la fonction de complexité $K$ ne dépendent pas des états informationnels. La couche info ne rétroagit pas sur le niveau I.

**Remarque (coût informationnel et sélection).** Le choix d’introduire une couche informationnelle sans rétroaction signifie : les contraintes de possibilité du niveau I (règles structurales, causalité, budget combinatoire) ne dépendent pas de l’état informationnel. Cela n’implique pas que la mémoire soit « gratuite » au niveau II : le principe de sélection (Ch.8) pourra pénaliser explicitement les configurations où l’information prolifère (taille de l’alphabet, densité de cellules actives, redondance excessive), afin d’éviter une inflation triviale de bits.


---

### 10.3 — Témoins et enregistrements (réalisation de 10.I.δ)

#### 10.3.1 — Témoins de motifs

**Définition 10.6 (Témoin de motif).** Soit $[\mathcal{P}]$ une classe de motifs structuraux. Un témoin de $[\mathcal{P}]$ dans $\widehat{H} = (H, s)$ est un couple $(U, f)$ où :

- $U \subseteq C_\Sigma(H)$ est une région de cellules
- $f : \mathcal{S}_U \to \{0, 1\}$ est une fonction

tel que :
1. $\widehat{H}$ contient au moins une occurrence de $[\mathcal{P}]$
2. $f(s_U) = 1$ ssi une condition spécifiée sur $[\mathcal{P}]$ est satisfaite

**Généralisation (témoin multi-états) :** $f : \mathcal{S}_U \to \mathcal{Y}$ où $\mathcal{Y}$ est un ensemble fini de valeurs.



**Condition de fiabilité (recommandée).** Pour éviter que « tout » puisse être déclaré témoin a posteriori, on introduit un critère de corrélation : on dit que $(U,f)$ est un témoin $\varepsilon$‑fiable de la propriété $\mathcal P$ (dans une phase ou un type d’univers $u$), si, sous la mesure conditionnée $\mu_\beta^{\{u\}}$,
\[
\mathbb P\big(f(s_U)=1\mid \mathcal P\big)\ge 1-\varepsilon,
\qquad
\mathbb P\big(f(s_U)=1\mid \neg\mathcal P\big)\le \varepsilon.
\]
On peut aussi exiger que $f$ provienne d’un protocole de copie implémenté par les mises à jour $U_r$ (témoignage *mécanistique*), plutôt que d’un choix arbitraire.
#### 10.3.2 — Témoins persistants

**Définition 10.7 (Témoin persistant — version conditionnelle).** Un témoin $(U,f)$ est persistant sur l'intervalle $[n_0,n_1]$ si :

1. (**Survie / transport du support**) il existe, pour tout $n\in[n_0,n_1]$, une région de cellules $U^{(n)}\subseteq C_\Sigma(H_n)$ telle que :
   - $U^{(n_0)}=U$ ;
   - $U^{(n)}$ est obtenue de $U^{(n-1)}$ par le transport canonique induit par l’événement (restriction à l’identité sur les cellules conservées, suppression des cellules détruites, éventuellement ajout de cellules “remplaçantes” si le schéma le prévoit).
   - si ce transport n’existe pas (cellules supprimées sans correspondance), le témoin cesse d’exister à ce temps.

2. (**Stabilité du contenu**) la valeur enregistrée reste inchangée le long de cet intervalle :
\[
f\big(s_{U^{(n)}}^{(n)}\big)=f\big(s_{U}^{(n_0)}\big),\qquad \forall n_0\le n\le n_1.
\]

Un enregistrement est dit stabilisé si $n_1-n_0$ est grand (échelle causale large) et si la persistance est robuste à des perturbations locales (cf. 10.4).

**Remarque.** Cette définition est volontairement *faible* : elle ne demande pas que la mémoire soit parfaite, mais seulement qu’un bit (ou un petit alphabet) reste stable sur une longue durée interne. Dans les applications (Niveau II–III), on utilisera souvent une version probabiliste : persistance avec probabilité $\ge 1-\delta$.


---

### 10.4 — Redondance et objectivité (réalisation de 10.I.ε)

#### 10.4.1 — Familles de témoins redondants

**Définition 10.8 (Famille redondante).** Une famille de témoins de $[\mathcal{P}]$ est une collection :

$$\mathcal{W} = \{(U_i, f_i)\}_{i \in I}$$

telle que :
1. Les régions $U_i$ sont disjointes (ou faiblement recouvrantes)
2. Toutes les fonctions donnent la même valeur :
   $$f_i(s_{U_i}) = f_j(s_{U_j}), \quad \forall i, j$$

Le degré de redondance est $|I|$.

#### 10.4.2 — Redondance typique

Pour un motif $[\mathcal{P}]$ dans un univers $U_n(\omega)$, la redondance effective $R_{[\mathcal{P}]}(U_n(\omega))$ est la taille maximale d'une famille de témoins redondants.

Sous la mesure $\mu_\beta^{\{u\}}$, $R_{[\mathcal{P}]}$ devient une variable aléatoire. En supposant un alphabet d’états info fini et une famille dénombrable de schémas de témoins (ou une σ-algèbre adaptée), la fonction $R_{[\mathcal{P}]}$ est mesurable.

#### 10.4.3 — Motifs objectivés

**Définition 10.9 (Motif objectivé).** Dans un type d'univers $u$, un motif $[\mathcal{P}]$ est objectivé par redondance si, pour tout $\delta>0$, il existe un seuil fini $R_0<\infty$ tel que :
\[
\mu_\beta^{\{u\}}\big(R_{[\mathcal{P}]}\ge R_0\big)\ge 1-\delta.
\]

Autrement dit, la redondance est arbitrairement grande avec probabilité arbitrairement proche de 1 (sans exiger une limite asymptotique littérale).  
*(Version forte — optionnelle : on peut imposer la condition asymptotique $\lim_{R_0\to\infty}\mu_\beta^{\{u\}}(R_{[\mathcal{P}]}\ge R_0)=1$ si l’univers est infini et si l’on vise une objectivité « parfaite ».)*

**Interprétation :**
- De nombreuses régions disjointes contiennent des témoins cohérents
- Une perturbation locale ne peut effacer tous les témoins
- Pour un observateur interne, $[\mathcal{P}]$ est un fait robuste

C'est la décohérence classique : l'irréversibilité émerge de la multiplication redondante des témoins, non d'un mécanisme quantique.

Nous prenons ici une condition forte : non seulement le motif est redondamment enregistré, mais la redondance est typiquement non bornée. On pourrait aussi considérer des notions plus faibles d’objectivation (redondance finie mais très grande), mais nous adoptons une forme asymptotique pour simplifier.

---

### 10.5 — Observateurs (réalisation de 10.I.ζ)

Au sens du chapitre 10, un observateur est tout motif apte à enregistrer et conserver de l’information. Cela inclut des systèmes très simples. Le raffinement vers des observateurs capables d’inférer des lois viendra plus tard (chap. 12).

#### 10.5.1 — Motifs observateurs

**Définition 10.10 (Motif observateur).** Dans un univers microscopique $U_n(\omega)$, un motif observateur est un sous-système :

$$\mathcal{O} = (R, s_{C_\Sigma(R)})$$

(structure $R$ + configuration informationnelle) satisfaisant :

1. **Capacité interne** : Il existe $M \subseteq C_\Sigma(R)$ tel que :
   $$\kappa(M) = \prod_{c \in M} |\mathcal{S}_c| \geq \kappa_{\min}$$
   (nombre minimal de bits d'information)

2. **Couplage à l'environnement** : Des règles augmentées permettent à $M$ de devenir témoin de motifs dans $\mathcal{U}(e_n, \omega) \setminus R$

3. **Stabilité interne** : L'état de $M$ reste inchangé sous les événements n'affectant pas directement $R$

**Remarque fondamentale :** Cette définition est purement structurelle. Elle ne parle pas de conscience, d'interprétation, ou de subjectivité — uniquement de capacité à maintenir des enregistrements sélectifs. 

#### 10.5.2 — Critères minimaux explicites

Un motif $\mathcal{O}$ est un observateur s'il satisfait :

| Critère | Description |
|---------|-------------|
| **Mémoire suffisante** | $\log_2 \kappa(M) \geq k_{\min}$ bits |
| **Couplage informatif** | Acquisition de témoins sur l'environnement |
| **Persistance** | Mémoire stable sur de longues échelles causales |

**Comptage et point de vue typique.** Pour parler d’« observateur typique », il faut préciser un schéma de comptage afin d’éviter le double comptage de motifs qui se recouvrent. Deux choix standards (souvent équivalents en grande taille sous hypothèses de mélange) :
- **Densité par volume combinatoire** : compter, dans une grande fenêtre (volume) $A$, un ensemble maximal de copies d’observateurs disjointes (packing) et définir une densité $\rho_{\mathcal O} = \lim_{A\uparrow \mathcal U} N_A(\mathcal O)/V(A)$.
- **Point de vue Palm / size-biased** (Ch.9) : échantillonner un univers proportionnellement à son “poids” (volume, complexité, nombre d’instances), puis étudier la distribution conditionnelle des observateurs à l’intérieur.

Dans ce chapitre, on se limite à ces schémas classiques ; l’extension vers une théorie opérationnelle complète (non‑commutativité, Born, etc.) relève du niveau III.

Un sous-système complexe ne satisfaisant pas ces critères n'est pas un observateur au sens du formalisme.

#### 10.5.3 — Observateurs typiques

Dans un type d'univers $u$, sous $\mu_\beta^{\{u\}}$, on peut définir :
- Comptage du nombre de motifs observateurs
- Distribution de leurs propriétés (capacité, profondeur des témoins...)

**Définition 10.11 (Univers informationnellement habité).** Un type $u$ est informationnellement habité si :

$$\mu_\beta^{\{u\}}(\exists \text{ au moins un observateur } \mathcal{O}) > 0$$

ou, plus fortement, si cette probabilité est proche de 1.

---

## Résumé de la structure

```
CHAPITRE 10 — STRUCTURES INFORMATIONNELLES
│
├── Partie I : NOYAU ONTOLOGIQUE (6 principes)
│   ├── 10.I.α  Couche informationnelle    [info sur structure]
│   ├── 10.I.β  Localité                   [info locale]
│   ├── 10.I.γ  Dynamique augmentée        [règles + info]
│   ├── 10.I.δ  Témoignage                 [encodage de faits]
│   ├── 10.I.ε  Redondance/objectivité     [décohérence classique]
│   └── 10.I.ζ  Observateur                [motif enregistreur]
│
└── Partie II : REPRÉSENTATION (5 sections)
    ├── 10.1  Couche d'information         [C_Σ(H), S_c, config augmentée]
    ├── 10.2  Dynamique augmentée          [règles augmentées, U_r]
    ├── 10.3  Témoins                      [(U,f), persistance]
    ├── 10.4  Redondance                   [familles, objectivation]
    └── 10.5  Observateurs                 [O = (R, s), critères]
```

---

## Remarques critiques

### Sur le statut de la couche informationnelle


> **Note de statut.** La construction de ce chapitre produit, à partir d’une mesure sur histoires, une théorie probabiliste classique (algèbre commutative d’observables). La non‑commutativité et la structure hilbertienne n’apparaissent qu’au niveau III, lorsque la description est contrainte par l’optimalité opérationnelle.

> **Note sur le coût de mémoire.** Même si la couche info ne modifie pas le niveau I, le principe de sélection peut (et devra souvent) inclure un terme de coût informationnel pour éviter une inflation triviale des enregistrements.

La couche d'information est ajoutée au niveau II — elle n'est pas dérivée du niveau I. C'est un enrichissement du formalisme, pas une conséquence.

**Question :** La couche informationnelle est-elle vraiment distincte de la structure, ou peut-elle être encodée dans la structure elle-même (par exemple via des sous-hypergraphes spéciaux) ?

**Réponse possible :** En principe, oui — on pourrait encoder l'information dans la structure. Mais la séparation est conceptuellement utile pour distinguer "ce qui existe" (structure) de "ce qui est enregistré" (information).

### Sur la définition d'observateur

La définition 10.10 est minimaliste : elle ne requiert que capacité + couplage + stabilité. Elle inclut donc potentiellement des systèmes très simples (thermomètres, cristaux...).

Pour une notion plus riche d'observateur (capable d'inférer des lois, de faire des prédictions...), des critères supplémentaires sont nécessaires — ils sont introduits implicitement au chapitre 12.

### Sur la décohérence classique

Le mécanisme de "décohérence" proposé (redondance des témoins) est différent de la décohérence quantique standard. Il ne requiert pas :
- D'espace de Hilbert
- De trace partielle sur l'environnement
- De superposition

C'est une notion classique d'irréversibilité pratique. La question de savoir si la décohérence quantique peut être dérivée de ce mécanisme reste ouverte.

---

## Lien avec les autres chapitres

| Chapitre           | Relation avec Ch.10                                          |
| ------------------ | ------------------------------------------------------------ |
| Ch.5 (Observables) | Les lectures/projections des observateurs définissent O_{\mathrm{obs}} et donc les macrostates |
| Ch.9 (Univers)     | Fournit U_n(\omega) comme support des observateurs           |
| Ch.11 (Temps)      | Utilise la mémoire M pour définir le temps interne           |
| Ch.12 (Lois)       | La reconstruction des lois s'appuie sur la projection $\mathbf{X}$ et sur les lectures $\Pi_{\mathcal{O}}$ (secteurs observables) |

---

## Glossaire du chapitre

| Terme | Définition |
|-------|------------|
| **Cellule informationnelle** | Élément de $C_\Sigma(H)$ portant un état |
| **Configuration augmentée** | $\widehat{H} = (H, s)$ |
| **Règle augmentée** | $\widehat{r} = (r, U_r)$ |
| **Témoin** | $(U, f)$ encodant un fait |
| **Témoin persistant** | Témoin stable dans le temps |
| **Redondance** | Nombre de témoins disjoints cohérents |
| **Motif objectivé** | Redondance typiquement grande |
| **Observateur** | Motif avec mémoire + couplage + stabilité |
| **Univers habité** | Type avec observateurs typiques |

