# Niveau II - Chapitre 5

# B. Observables et états macroscopiques

------

## Introduction

Le chapitre 4 a doté l'espace des histoires $\Omega_B$ d'une structure mesurable et d'une classe de mesures de typicalité. Ce chapitre introduit les observables — fonctions qui extraient de l'information des histoires — et le coarse-graining — mécanisme qui regroupe les histoires microscopiquement distinctes en classes macroscopiquement équivalentes.

> **Point clé :** À ce niveau, "observable" est un concept purement mathématique (fonction mesurable), sans référence à un observateur physique. Les observateurs internes apparaîtront au chapitre 10.

Le coarse-graining est l'outil fondamental pour passer de la description microscopique (histoires individuelles) à la description macroscopique (phases, univers émergents).

------

## Partie I : Noyau ontologique

### 5.I.α — Principe d'extractibilité de l'information

> **Toute propriété mesurable (sous-ensemble de $\Omega_B$ dans $\Sigma_B$) définit un observable.**

Une histoire $\omega \in \Omega_B$ contient potentiellement une quantité infinie d'information. On peut extraire de cette information n'importe quelle propriété formulable : présence d'un motif, comptage, densité asymptotique, structure globale, etc.

Formellement : toute fonction mesurable $O : \Omega_B \to X$ est un observable admissible.

------

### 5.I.β — Principe de localité des observables physiques

> **Les observables physiquement significatifs sont locaux.**

Parmi tous les observables possibles, seuls ceux qui dépendent d'une région causale finie ont une signification physique directe. Un observable qui dépendrait de toute l'histoire serait inaccessible à tout sous-système fini.

Ce principe contraint les observables pertinents pour la physique émergente.

**Précision (localité intrinsèque).** Ici, "local" signifie : il existe un rayon causal fini $R$ tel que $O(\omega)$ ne dépende que de la classe d’isomorphisme d’un voisinage causal fini (cf. §5.4), et qu’il soit invariant sous relabeling des identifiants et sous permutation d’événements concurrents (commutations). Toute dépendance à un index de codage ("$n$-ième événement") n’est admise que comme jauge technique (cf. §5.3).

### 5.I.γ — Principe de réduction (coarse-graining)

> **L'information peut être compressée de façon exacte relativement aux observables retenues.**

Plusieurs histoires microscopiquement distinctes peuvent être indiscernables au regard d’une famille d’observables (ou d’un protocole   descriptif). On modélise cette compression par un coarse-graining (une projection mesurable) : 

$$\Gamma : \Omega_B \longrightarrow \mathcal{M}$$

où $\mathcal{M}$ est l’espace des macrostates. Deux histoires $\omega,\omega'$ sont alors macro-indiscernables si $\Gamma(\omega)=\Gamma(\omega')$.

Le passage micro → macro n’est pas une approximation : c’est une réduction exacte relativement à la $\sigma$-algèbre $\sigma(\Gamma)$ engendrée par $\Gamma$  (ou, plus généralement, par la famille d’observables retenue). Il est donc "sans perte" pour ces observables, mais il perd en général de l’information au niveau micro.

------

### 5.I.δ — Principe de typicalité macroscopique

> **La typicalité se transfère du niveau micro au niveau macro.**

Si $\mu$ est une mesure de typicalité sur $\Omega_B$ et $\Gamma$ un coarse-graining, alors la mesure image $\mu^\Gamma$ définit une typicalité sur les macrostates.

Un macrostate est "typique" s'il contient la grande majorité des histoires au sens de $\mu$.

------

### 5.I.ε — Principe d'indépendance du coarse-graining

> **Le choix du coarse-graining est une convention, pas une donnée ontologique.**

Différents coarse-grainings correspondent à différents "points de vue" sur le même espace d'histoires. Aucun n'est privilégié a priori.

Cependant, certains coarse-grainings peuvent être distingués par des propriétés structurelles (respect de la causalité, stabilité sous la dynamique, etc.).


Nous introduirons le principe de sélection informationnelle (principe S) qui peut, entre autres, privilégier certaines familles d’observables / coarse-grainings $\Gamma$ par des critères d’optimalité (invariance, stabilité, compromis complexité–entropie, etc.).

------

## Partie II : Choix de représentation

### 5.1 — Cadre général

On fixe :

- Un système de niveau I $(H_0, \mathcal{R}, K, B)$
- L'espace des histoires $\Omega_B$ avec sa σ-algèbre $\Sigma_B$
- Une mesure de probabilité $\mu$ sur $(\Omega_B, \Sigma_B)$

**Rappel :** Une histoire $\omega$ est codée comme une suite linéarisée $(e_0, e_1, e_2, \ldots)$ d'événements, ce codage étant un outil technique sans signification physique.

------

### 5.2 — Observables mesurables

#### 5.2.1 — Définition générale

**Définition 5.1 (Observable).** Un observable est une application mesurable :

$$O : \Omega_B \longrightarrow X$$

où $(X, \mathcal{X})$ est un espace mesurable (typiquement $\mathbb{R}$, $\mathbb{N}$, ou un espace de structures plus complexe).

**Mesurabilité :** Pour tout $A \in \mathcal{X}$, on a $O^{-1}(A) \in \Sigma_B$.

**Distribution de l'observable :** Sous la mesure $\mu$, l'observable $O$ a pour distribution la mesure image :

$$\mu_O := \mu \circ O^{-1}$$

définie par $\mu_O(A) = \mu(O^{-1}(A))$.

**Remarque importante :** À ce stade, "observable" n'a pas de connotation physique d'instrument de mesure. C'est une fonction sur l'espace des histoires, rien de plus.

#### 5.2.2 — Exemples d'observables

| Observable                            | Espace cible |
| ------------------------------------- | ------------ |
| Nombre total de sommets à l'étape $n$ | $\mathbb{N}$ |
| Présence d'un motif $[\mathcal{P}]$   | ${0, 1}$     |
| Densité asymptotique d'un type        | $[0, 1]$     |
| Complexité à l'étape $n$              | $\mathbb{R}$ |

------

### 5.3 — Observables cylindriques

Les observables les plus simples sont ceux qui ne dépendent que d'un préfixe fini de l'histoire.

#### 5.3.1 — Définition

**Définition 5.2 (Observable cylindrique).** Un observable $O : \Omega_B \to X$ est cylindrique de profondeur $n$ s'il existe une fonction :

$$\phi : \Omega_B^{(n)} \to X$$

telle que :

$$O(\omega) = \phi(e_0, \ldots, e_{n-1})$$

où $(e_k)$ est le codage linéarisé de $\omega$.

**Proposition.** Tout observable cylindrique est mesurable pour $\Sigma_B$.

*Preuve.* La σ-algèbre $\Sigma_B$ est engendrée par les cylindres de préfixes. Un observable dépendant du préfixe de longueur $n$ est mesurable pour la sous-σ-algèbre finie générée par ces cylindres.

#### 5.3.2 — Interprétation

Un observable cylindrique de profondeur $n$ "voit" les $n$ premiers événements du codage linéarisé, mais ignore le reste de l'histoire.

**Limitation :** La profondeur $n$ dépend du codage (choix d'extension linéaire), pas de la structure causale intrinsèque.

------

### 5.4 — Observables localement causaux (réalisation de 5.I.β)

Pour respecter la structure causale du niveau I, on introduit des observables qui dépendent d'une région causale finie plutôt que d'un index linéaire.

#### 5.4.1 — Voisinages causaux

Pour un événement $e \in E(\omega)$ et un rayon $R \geq 0$, le voisinage causal $N_R(e)$ est défini par récurrence :

- $N_0(e) = {e}$
- $N_{R+1}(e) = N_R(e) \cup {f \in E(\omega) \mid \exists g \in N_R(e), f \prec g \text{ ou } g \prec f}$

**Hypothèse (LF — localement fini).** On suppose que, pour tout $\omega$, $e$, $R$, l'ensemble $N_R(e)$ est fini.

Cette propriété est garantie dans les modèles à cutoff (taille/complexité bornée) et, plus généralement, lorsque la dynamique de réécriture induit un graphe causal des événements localement fini (degré entrant/sortant fini), ce qui est compatible avec la localité bornée des règles.

#### 5.4.2 — Définition

On veut définir des observables qui ne dépendent que d’une portion finie du graphe causal des événements, et qui soient invariants sous relabeling.

**Définition 5.3 (Observable localement causal).** Un observable $O : \Omega_B \to X$ est localement causal de rayon $R$ s’il existe :

- une application $\Phi : \mathcal{D}_R \to X$, où $\mathcal{D}_R$ est l’ensemble des classes d’isomorphisme de voisinages causaux de rayon $R$,
- et un mécanisme de “référence” satisfaisant l’un des deux schémas suivants.

**(A) Référence par jauge (sélection mesurable).** 

Il existe une règle (au moins mesurable) $\omega\mapsto e_{\mathrm{ref}}(\omega)\in E(\omega)$ telle que :

$$O(\omega)=\Phi\bigl([N_R(e_{\mathrm{ref}}(\omega))]\bigr).$$

Dans ce cas, $e_{\mathrm{ref}}$ peut dépendre d’un choix de codage/linéarisation : on interprète alors ce choix comme une jauge, et l’on considère comme physiquement pertinents les observables (ou statistiques d’observables) robustes sous changement de jauge (invariance ou stabilité à $\varepsilon$).

**(B) Référence intrinsèque (agrégation sur un ensemble canonique).** 

Il existe une règle mesurable associant à $\omega$ un ensemble fini non vide $E_{\mathrm{ref}}(\omega)\subset E(\omega)$ (par exemple : une couche d’une foliation, un ensemble d’événements satisfaisant un critère local, etc.) et une opération d’agrégation $\mathrm{Agg}$ (moyenne, histogramme, quantile, vote majoritaire…) telles que :

$$O(\omega)=\mathrm{Agg}\Big(\{\,\Phi([N_R(e)])\ :\ e\in E_{\mathrm{ref}}(\omega)\,\}\Big).$$

**Interprétation :** un observable localement causal lit un “patch” causal fini (à isomorphisme près), soit autour d’un événement de référence choisi (A), soit via une statistique intrinsèque (B).

#### 5.4.3 — Exemples

- **Densité locale de motifs** : Nombre d'occurrences d'un motif $[\mathcal{P}]$ dans $N_R(e_{\mathrm{ref}})$
- **Degré causal** : Nombre de prédécesseurs/successeurs immédiats de $e_{\mathrm{ref}}$
- **Coût local** : $\ell(e_{\mathrm{ref}})$ (action de l'événement de référence)

------

### 5.5 — Coarse-graining et macrostates (réalisation de 5.I.γ)

Le coarse-graining est le mécanisme fondamental pour passer de la description microscopique à la description macroscopique.

#### 5.5.1 — Définition

**Définition 5.4 (Coarse-graining).** Un coarse-graining est une application mesurable :

$$\Gamma : \Omega_B \longrightarrow \mathcal{M}$$

où $(\mathcal{M}, \mathcal{M}_\sigma)$ est un espace mesurable appelé espace des macrostates.

**Commentaire : ** L'espace $\mathcal{M}$ a une structure de plus faible information et doit avoir un "niveau de détail" inférieur à $\Omega_B$.

#### 5.5.2 — Macrostates comme classes d'équivalence

Le coarse-graining $\Gamma$ induit une relation d'équivalence :

$$\omega \sim_\Gamma \omega' \quad \Longleftrightarrow \quad \Gamma(\omega) = \Gamma(\omega')$$

Chaque macrostate est une classe d'équivalence :

$$[\omega]_\Gamma := {\omega' \in \Omega_B \mid \Gamma(\omega') = \Gamma(\omega)}$$

L'espace des macrostates s'identifie au quotient :

$$\mathcal{M} \simeq \Omega_B / \sim_\Gamma$$

#### 5.5.3 — Construction par observables

Un coarse-graining peut être défini par une famille d'observables $(O_i)_{i \in I}$ :

$$\Gamma(\omega) := (O_i(\omega))_{i \in I}$$

Dans ce cas, deux histoires sont équivalentes ssi elles ont les mêmes valeurs pour tous les observables de la famille.

------

### 5.6 — Mesure induite et typicalité macroscopique (réalisation de 5.I.δ)

#### 5.6.1 — Mesure macroscopique

**Définition 5.5 (Mesure macroscopique).** La mesure macroscopique induite par $\Gamma$ est :

$$\mu^\Gamma := \mu \circ \Gamma^{-1}$$

définie sur $(\mathcal{M}, \mathcal{M}_\sigma)$ par :

$$\mu^\Gamma(A) = \mu(\Gamma^{-1}(A)) = \mu({\omega \in \Omega_B \mid \Gamma(\omega) \in A})$$

#### 5.6.2 — Typicalité

**Définition 5.6 (Macrostates typiques).** Un ensemble $T \subseteq \mathcal{M}$ est typique (pour $\mu$ et $\Gamma$) si :

$$\mu^\Gamma(T) = 1 \quad \text{ou} \quad \mu^\Gamma(\mathcal{M} \setminus T) = 0$$

**Interprétation :** Une histoire tirée selon $\mu$ appartient presque sûrement à un macrostate de $T$.

#### 5.6.3 — Concentration macroscopique

Dans de nombreuses situations, la mesure $\mu^\Gamma$ se concentre sur un petit sous-ensemble de $\mathcal{M}$ :

$$\exists m^* \in \mathcal{M} : \mu^\Gamma({m^*}) \approx 1$$

C'est l'analogue de la concentration thermodynamique : presque toutes les histoires partagent le même profil macroscopique.

------

### 5.7 — Coarse-graining causal et profils le long des foliations

Pour préparer l'étude des phases et de la dynamique émergente, on combine coarse-graining et structure causale.

#### 5.7.1 — Foliation causale

Soit $\omega$ une histoire. Une foliation causale est une décomposition :

$$\mathcal{F}(\omega) = (S_k(\omega))_{k \in K}$$

où :

- Chaque $S_k$ est un pas causal (antichaîne)
- Les $S_k$ sont disjoints et couvrent $E(\omega)$
- $K$ est totalement ordonné (typiquement $\mathbb{N}$ ou $\mathbb{Z}$)

**Remarque (existence, non-unicité, et foliations admissibles).** Une histoire peut admettre de nombreuses foliations, et certaines foliations peuvent être pathologiques vis-à-vis des observables considérées. On introduit donc un ensemble $\mathfrak{F}(\omega)$ de foliations admissibles (par exemple : satisfaisant des bornes de taille de couches, ou une régularité statistique), et l’on qualifiera de physiquement robustes les quantités invariantes (ou stables à $\varepsilon$) sous changement $\mathcal{F}\in\mathfrak{F}(\omega)$.

**Rappel :** Le choix de foliation est une convention (principe d'indépendance du choix de représentation). Les quantités définies à partir d’une foliation ne seront interprétées comme physiquement significatives que si elles sont foliation-invariantes (ou au moins stables à $\varepsilon$) sur $\mathfrak{F}(\omega)$.

#### 5.7.2 — Profil macro-causal

On définit un observable de profil :

$$\Gamma^{\mathcal{F}} : \Omega_B \longrightarrow \mathcal{M}^K$$

par :

$$\Gamma^{\mathcal{F}}(\omega) = (m_k)_{k \in K}$$

où $m_k = \Gamma_{\mathrm{loc}}(S_k(\omega))$ est le macrostate local de la couche $S_k$.

**Interprétation :** Le profil $\Gamma^{\mathcal{F}}(\omega)$ est la "trajectoire macroscopique" de l'histoire $\omega$ le long de la foliation.

#### 5.7.3 — Distribution des profils

La mesure $\mu$ induit une distribution sur les profils macro-causaux. On pourra parler de :

- **Profils typiques** : ceux de mesure proche de 1
- **Profils stationnaires** : invariants statistiquement le long de $k$
- **Transitions de profil** : changements qualitatifs du macrostate le long de $k$

------

## Résumé de la structure

```
CHAPITRE 5 — OBSERVABLES ET MACROSTATES
│
├── Partie I : NOYAU ONTOLOGIQUE (5 principes)
│   ├── 5.I.α  Extractibilité           [toute propriété → observable]
│   ├── 5.I.β  Localité physique        [observables à support fini]
│   ├── 5.I.γ  Réduction                [micro → macro par équivalence]
│   ├── 5.I.δ  Typicalité macro         [μ induit μ^Γ]
│   └── 5.I.ε  Indépendance du Γ        [pas de Γ privilégié]
│
└── Partie II : REPRÉSENTATION (7 sections)
    ├── 5.1  Cadre général              [rappels]
    ├── 5.2  Observables mesurables     [fonctions O : Ω_B → X]
    ├── 5.3  Observables cylindriques   [dépendance en préfixe fini]
    ├── 5.4  Observables causaux        [dépendance en N_R(e)]
    ├── 5.5  Coarse-graining            [Γ : Ω_B → M, macrostates]
    ├── 5.6  Mesure induite             [μ^Γ et typicalité]
    └── 5.7  Profils macro-causaux      [Γ le long des foliations]
```

------

## Remarques critiques

### Sur le statut du coarse-graining

Le principe 5.I.ε affirme qu'aucun coarse-graining n'est privilégié a priori. C'est une position de neutralité, mais elle pose un problème pratique :

**Question ouverte :** Comment choisir $\Gamma$ pour définir les "phases" ou les "univers" ?

Deux approches possibles :

1. **Approche physique** : Le coarse-graining est déterminé par les capacités d'un observateur interne (chapitre 10). Seuls les macrostates distinguables par l'observateur sont pertinents.
2. **Approche structurelle** : Certains $\Gamma$ sont distingués par des propriétés mathématiques (invariance sous $\Theta$, respect de la causalité, minimalité).

### Sur la relation cylindrique/causal

Les observables cylindriques (§5.3) et les observables causaux (§5.4) ne coïncident pas en général :

| Propriété                     | Cylindrique    | Causal                 |
| ----------------------------- | -------------- | ---------------------- |
| Dépend du codage linéaire     | Oui            | Non                    |
| Respecte la structure causale | Non garanti    | Oui (par construction) |
| Profondeur bornée             | Oui ($n$ fixé) | Oui ($R$ fixé)         |

Pour la physique émergente, les observables causaux sont plus fondamentaux (ils ne dépendent pas de la convention de linéarisation).

### Sur la concentration macroscopique

La concentration de $\mu^\Gamma$ sur un petit ensemble de macrostates est une propriété non triviale qui dépend de :

- La structure de $\mu$ (mesure de sélection vs mesure de référence)
- Le choix de $\Gamma$
- La "taille" de l'histoire (limite thermodynamique)

C'est cette concentration qui permettra de parler de "phases" bien définies au chapitre 6.

------

## Lien avec les autres chapitres

| Chapitre             | Relation avec Ch.5                                           |
| -------------------- | ------------------------------------------------------------ |
| Ch.4 (Probabilités)  | Fournit $(\Omega_B, \Sigma_B, \mu)$ comme espace de base     |
| Ch.6 (Phases)        | Utilise $\Gamma$ pour définir les phases macroscopiques      |
| Ch.7 (Nucléation)    | Les taux $\lambda_{[\mathcal{G}]}$ sont des observables sur $\Omega_B$ |
| Ch.9 (Univers)       | $\Gamma^{\mathrm{univ}}$ est un coarse-graining spécifique   |
| Ch.10 (Observateurs) | L'observateur définit implicitement un $\Gamma$              |

------

## Note terminologique

| Terme      | Signification dans ce chapitre                               |
| ---------- | ------------------------------------------------------------ |
| Observable | Fonction mesurable $O : \Omega_B \to X$ (sans connotation physique) |
| Macrostate | Classe d'équivalence $[\omega]_\Gamma$ sous un coarse-graining |
| Typique    | De mesure 1 (ou proche de 1)                                 |
| Profil     | Suite de macrostates le long d'une foliation                 |

Le terme "observable" prendra une signification plus physique au chapitre 10, lorsqu'il sera relié aux structures informationnelles accessibles à un observateur interne.