# Niveau I - Chapitre 2

# I.C. Émergence

---

## Table des matières

- [Introduction](#introduction)
- [C0 — Qu’est-ce que l’émergence ?](#c0--quest-ce-que-lémergence-)
- [C1 — Couches émergentes (définition combinatoire)](#c1--couches-émergentes-définition-combinatoire)
- [C2 — Observables macroscopiques (sans géométrie présupposée)](#c2--observables-macroscopiques-sans-géométrie-présupposée)
- [C3 — Coarse-graining intrinsèque et "renormalisation" des règles](#c3--coarse-graining-intrinsèque-et-renormalisation-des-règles)
- [C4 — Phases et transitions](#c4--phases-et-transitions)
- [C5 — Nucléation dans le vide pré-géométrique](#c5--nucleation)
- [Récapitulatif et questions ouvertes](#récapitulatif-et-questions-ouvertes)

---

## Introduction

### Contexte

Les niveaux I.A–I.B fournissent :
- un substrat relationnel discret (hypergraphes / structures d’incidence) ;
- des règles locales de réécriture ;
- un graphe causal d’événements construit à partir des dépendances Read/Write ;
- une mesure (au moins régularisée par cutoff) sur configurations et/ou histoires, et des notions de fréquences.

Le présent document (I.C) a pour objectif de définir ce que signifie "émerger" dans ce cadre et de fournir les opérateurs (coarse-graining) et notions de phase nécessaires pour passer d’une description micro à une description macro, *sans* importer d’emblée le vocabulaire du continu.

### Le problème de l’émergence

On veut éviter deux écueils :
1. **Slogan sans critère** : "une géométrie apparaît" sans définition testable.
2. **Circularité** : utiliser des notions de métrique/position/dimension continue pour définir précisément… l’émergence de la métrique/position/dimension.

### Stratégie

- Formaliser l’émergence comme une propriété robuste (insensible à un nombre fini de perturbations microscopiques) ou comme un observable typique (au sens de la mesure sur histoires).
- Introduire des observables macroscopiques purement combinatoires.
- Définir des opérateurs de coarse-graining intrinsèques (paramètre d’échelle exprimé en distances de graphe/causales, pas en coordonnées).
- Définir les phases comme régimes stables (observables stables, composantes ergodiques, points fixes de coarse-graining).
- Définir la nucléation

---

# C0 — Qu’est-ce que l’émergence ?

## C0.1 — Définition formelle

Nous travaillons sur l’espace des histoires \(\Omega\) (ou sur des histoires tronquées) muni d’une mesure \(\mu\) (souvent \(\mu_{\beta,\Lambda}\) au cutoff \(\Lambda\)), et sur la filtration des cylindres \((\mathcal F_n)\)\.

### Propriété asymptotique (propriété de "queue")

Une propriété \(P\) est dite asymptotique (ou de "queue") si elle est inchangée par modification d’un nombre fini d’événements :

> \(P(\omega)=P(\omega')\) dès qu’il existe \(N\) tel que \(\omega_{>N}=\omega'_{>N}\).

Cette notion capture l’idée de "macro-propriété" indépendante des détails initiaux.

### Observable émergente

Une observable \(\mathcal O\)\ (définie sur les histoires ou sur la suite des configurations) est dite émergente si :
1. \(\mathcal O\)\ est (au moins) une limite de moyennes (temporelles/ensemble) définie par des objets micro ;
2. \(\mathcal O\)\ est robuste sous des perturbations finies (ou est typique au sens \(\mu\) : la propriété "\(\mathcal O\) existe et vaut telle valeur" est vraie p.s. sur un ensemble de mesure 1).

### Hiérarchie d’émergence

On distingue :
- **émergence descriptive** : la macro-description est plus courte/plus stable que la micro-description ;
- **émergence structurelle** : des relations nouvelles (symétries, invariants, causalités effectives) apparaissent ;
- **émergence dynamique** : la macro-description admet une dynamique fermée (approx.) à grande échelle.

## C0.2 — Critères d’émergence

Pour une propriété \(P\) ou une observable \(\mathcal O\), on propose les critères (statuts : définitionnels ou testables) :

1. **Échelle** : \(P\)\ n’est pas détectable sur de petits préfixes mais devient stable au-delà d’une échelle \(n\gg n_0\).
2. **Robustesse** : invariance sous perturbations finies, ou stabilité sous coarse-graining.
3. **Compressibilité** : la description de \(P\)\ (ou de \(\mathcal O\)\ ) est significativement plus courte que celle du micro-état.
4. **Universalité** : \(P\)\ dépend faiblement des détails micro (règles exactes, conditions initiales), au moins dans une classe.

## C0.3 — Types d’émergence (statut : terminologie)

- **Émergence faible** : \(P\)\ est déductible en principe, mais impraticable sans coarse-graining (ex. thermodynamique).
- **Émergence forte** : \(P\)\ requiert des principes additionnels (ex. mesure/typicalité) et n’est pas "visible" en micro sans ce choix.

Dans notre architecture, l’émergence "forte" sera principalement liée au choix de mesure / principe de sélection (niveau II). Ici, on se limite aux notions nécessaires pour décrire l’émergence.

---

# C1 — Couches émergentes (définition combinatoire)

Cette section formalise une stratification des "types" émergents, sans supposer d’espace-temps continu. Le mot "géométrique" signifie ici "relatif à la structure d’adjacence/causalité", pas "métrique lorentzienne".

## C1.1 — Stratification des types émergents

### Hypothèse de stratification (statut : hypothèse de travail)

Dans une phase macroscopique stable, les éléments (nœuds, hyperarêtes, motifs, régions) se regroupent en un petit nombre de types \(T\) robustes, définis via :
- des profils fréquentiels (I.B) ;
- des invariants locaux (degré, motifs) ;
- des profils informationnels (entropies, flux).

### Trois couches fondamentales (définition)

On introduit trois familles de variables macroscopiques :

- Couche structurelle / "géométrique" \(L_{\text{geo}}\) : invariants de voisinage et de causalité (dimension effective, localité, homogénéité…).
- Couche informationnelle \(L_{\text{info}}\) : variables de traitement/stockage/transmission d’information (mémoire, corrélations, compressibilité…).
- Couche de couplage \(L_{\text{coupl}}\) : relations statistiques entre \(L_{\text{geo}}\) et \(L_{\text{info}}\) (corrélations, réponses, "backreaction" combinatoire).

## C1.2 — Couche structurelle \(L_{\text{geo}}\)

### Définition (intrinsèque)

On dit qu’une région \(R\) (dans le graphe causal d’événements ou dans l’hypergraphe) est structurellement quasi-régulière à l’échelle \(\ell\) si les statistiques de voisinage dans des boules de rayon \(\ell\)\ sont approximativement stationnaires :

- **Homogénéité statistique** : la distribution des invariants locaux (degrés, motifs) varie peu d’un centre à l’autre ;
- **Isotropie statistique** : absence de directions privilégiées mesurées par anisotropie des chemins/voisinages (définis intrinsèquement via distances de graphe/causales) ;
- **Dimension effective stable** : le volume des boules \(B(v,r)\)\ croît comme \(r^{d_{\text{eff}}}\)\ sur un intervalle de \(r\).

Ces critères n’utilisent ni coordonnées \(x\) ni métrique continue.

### Exemples de "types" structurels (non exhaustif)

- régions "crumpled" (forte densité de connexions, faible dimension effective) ;
- régions "branching" (arborescentes, dimension proche de 1) ;
- régions "quasi-locales" (voisinages stables, dimension effective > 1).

### Observables structurelles (exemples)

- **Volume** : \(|V|,|E|\) ou densité d’événements par profondeur causale ;
- **Croissance de boules** : \(|B(v,r)|\)\ ;
- **Spectral dimension** (option) : dimension estimée par retour de marche aléatoire sur la structure (définition combinatoire).

## C1.3 — Couche informationnelle \(L_{\text{info}}\)

### Définition (intrinsèque)

La couche informationnelle est définie par des observables construites à partir :
- des étiquettes/états internes (s’il y en a),
- des motifs de lecture/écriture (Read/Write),
- des corrélations entre régions (au sens de partitions intrinsèques).

On dit qu’une région possède un état informationnel stable si certaines distributions (types, symboles, motifs) et entropies associées convergent en moyenne et sont robustes au coarse-graining.

### Exemples

- motifs "avec mémoire" : régions dont l’activité présente des corrélations longues en profondeur causale ;
- "modules" informationnels : sous-structures à forte information mutuelle interne mais faible couplage externe.

### Observables informationnelles (exemples)

- entropie de Shannon d’une distribution de types/motifs ;
- information mutuelle entre deux régions (définies intrinsèquement via une partition) ;
- flux d’information : corrélations orientées le long des liens causaux d’événements.

## C1.4 — Couche de couplage \(L_{\text{coupl}}\)

### Définition

La couche de couplage capture la façon dont les variables structurelles et informationnelles se co-influencent.

Exemples d’observables de couplage (sans interprétation "physique" imposée) :
- corrélation entre taux d’événements et densité/structure locale ;
- réponse de la structure (degré, dimension effective) à une augmentation du flux informationnel ;
- "backreaction" combinatoire : changement des statistiques structurelles conditionné par des états informationnels.

## C1.5 — Diagramme de stratification (schéma)

Micro (réécriture)  
→ types locaux (motifs, degrés, profils)  
→ variables structurelles \(L_{\text{geo}}\)  
→ variables informationnelles \(L_{\text{info}}\)  
→ couplage \(L_{\text{coupl}}\)

## C1.6 — Cohérence des couches

### Principe de compatibilité (statut : principe)

Une macro-description est dite cohérente si :
1. les observables retenues sont invariantes sous relabeling/isomorphisme ;
2. elles sont stables sous permutations d’événements concurrents (commutation) ;
3. elles sont stables sous coarse-graining dans une phase.

### Test de cohérence (procédure)

- choisir une famille d’opérateurs de coarse-graining \(\pi_{\ell}\) ;
- vérifier que les distributions des observables changent peu quand \(\ell\) varie dans un intervalle ;
- vérifier l’absence de dépendance au choix de linéarisation du poset d’événements.

---

# C2 — Observables macroscopiques (sans géométrie présupposée)

## C2.1 — Définition générale

### Observable

Une observable macroscopique est une application \(\mathcal O\)\ construite à partir d’un état \(H\) ou d’un préfixe d’histoire \(\omega_{1:n}\) et qui :
- est invariant sous isomorphisme,
- est stable au coarse-graining (dans une phase),
- admet une interprétation statistique (moyennes/corrélations).

### Classification

- **structurelles** : volumes, degrés, motifs, dimensions effectives, invariants causaux ;
- **informationnelles** : entropies, informations mutuelles, compressibilités ;
- **couplage** : réponses/corrélations croisées.

## C2.2 — Moyennes et corrélations

### Moyenne d’ensemble vs moyenne temporelle

Au cutoff \(\Lambda\) :
- moyenne d’ensemble : \(\langle \mathcal O\rangle_{\mu_{\beta,\Lambda}}\)\ ;
- moyenne temporelle (sur une histoire) : \(\overline{\mathcal O}(\omega)=\lim_{n\to\infty}\frac1n\sum_{k=1}^n \mathcal O(H_k)\)\ (si elle existe).

**Statut** : l’égalité "ensemble = temps" requiert stationnarité + ergodicité (voir I.B).

### Fonctions de corrélation (intrinsèques)

On définit une notion de distance intrinsèque \(d\) :
- distance de graphe sur \(H\) ou sur le graphe causal d’événements ;
- ou distance "causale" (longueur d’une chaîne minimale).

Une corrélation à distance \(r\) peut être définie par :
\[
C_{\mathcal O}(r)=\mathbb E\big[\mathcal O(u)\,\mathcal O(v)\ \big|\ d(u,v)=r\big]-\mathbb E[\mathcal O]^2.
\]

### Susceptibilité (réponse)

Pour un paramètre \(\theta\)\ (ex : \(\beta\)\ ou un couplage effectif dans \(K\)), on définit :
\[
\chi_{\mathcal O}=\frac{\partial}{\partial\theta}\langle \mathcal O\rangle.
\]
Les pics de \(\chi\) signalent des transitions.

## C2.3 — Exemples d’observables structurelles (sans "métrique" continue)

- **densité locale** : taille de voisinage à rayon \(r\)\ ;
- **profil de degrés** : distribution \(P(\deg)\)\ ;
- **dimension effective** : pente de \(\log |B(v,r)|\)\ vs \(\log r\) dans une fenêtre de \(r\).

## C2.4 — Exemples d’observables informationnelles

- entropie \(H(\mathcal T)\)\ d’une distribution de types locaux \(\mathcal T\)\ ;
- information mutuelle entre régions \(A,B\) :
\[
I(A;B)=H(A)+H(B)-H(A,B).
\]
- flux d’information (version minimale) : corrélation orientée entre symboles/états le long des arcs causaux.

## C2.5 — Exemples d’observables de couplage

- \(\mathrm{Cov}(\text{activité},\text{densité})\)\ ;
- réponse de la dimension effective à une contrainte informationnelle ;
- corrélations entre profils Read/Write et invariants structurels.

## C2.6 — Symétries émergentes (version Niveau I)

Une symétrie émergente au niveau I signifie : invariance (approximative) des *statistiques* d’observables sous une famille de transformations intrinsèques (automorphismes, relabelings, permutations de classes concurrentes, etc.).

On peut mesurer :
- l’écart à l’invariance (distance entre distributions),
- l’échelle à partir de laquelle l’invariance devient bonne.

---

# C3 — Coarse-graining intrinsèque et "renormalisation" des règles

## C3.1 — Principe du coarse-graining

Le coarse-graining est une application :
\[
\pi_{\ell}:\ H\ \mapsto\ \bar H_{\ell},
\]
où \(\ell\)\ est une échelle intrinsèque (rayon de graphe, profondeur causale, taille de communauté, etc.).

Objectifs :
1. produire une description \(\bar H_{\ell}\) plus compacte ;
2. préserver certaines observables macroscopiques ;
3. définir des dynamiques effectives (règles émergentes) à l’échelle \(\ell\).

## C3.2 — Familles d’opérateurs de partition (Étape 1)

On propose trois constructions (à choisir selon le modèle) :

### (A) Couverture par boules (graph distance)

- choisir un ensemble de centres \(S\) ;
- définir des cellules \(C_s=B(s,\ell)\) ;
- résoudre les recouvrements (règle de priorité, Voronoï discret, etc.).

### (B) Partition par communautés

- construire un graphe d’adjacence \(G\) induit par l’hypergraphe ;
- appliquer un algorithme de détection de communautés (modularité, SBM, etc.) avec paramètre d’échelle.

### (C) Partition causale (événements)

- regrouper les événements par blocs de profondeur causale \(\ell\) ou par "diamètre causal".

## C3.3 — Agrégation (Étape 2) et configuration effective (Étape 3)

Pour chaque cellule \(C_i\) on définit :
- un super-nœud \(\bar v_i\) ;
- des super-hyperarêtes \(\bar e\) reliant les cellules qui interagissent (au sens des incidences/Read/Write).

On associe aux cellules des variables agrégées :
- tailles, densités, histogrammes de motifs ;
- profils informationnels (entropies, corrélations internes) ;
- taux d’activité (compteurs d’événements).

La configuration coarse-grainée \(\bar H_{\ell}\) est la structure quotient + ses variables.

## C3.4 — Règles émergentes et description minimale

On définit une grammaire effective \(\bar{\mathcal R}_{\ell}\) qui approxime l’évolution de \(\bar H_{\ell}\).

Idée (statut : procédure) :
- observer, sur une fenêtre, les transformations \(\bar H_{\ell}\to\bar H'_{\ell}\) induites par les micro-événements ;
- inférer un petit ensemble de règles \(\bar r\) expliquant ces transitions avec un compromis "erreur + complexité" (principe MDL).

Cette étape est l’ancêtre direct de l’idée que "des règles émergent à chaque transition de phase" : au niveau I, on ne postule pas l’émergence de nouvelles lois, on définit comment les extraire.

## C3.5 — Flot d’échelle et points fixes (RG combinatoire)

On voit \(\ell\)\ comme un paramètre d’échelle et on définit un flot :
\[
(\mathcal R, K, \beta)\ \xrightarrow{\ \pi_{\ell}\ }\ (\bar{\mathcal R}_{\ell},\ \bar K_{\ell},\ \bar\beta_{\ell}).
\]

- un point fixe correspond à une phase où la description se stabilise (mêmes observables, grammaire effective stable) ;
- l’universalité correspond au fait que plusieurs microscopiques mènent au même point fixe.

---

# C4 — Phases et transitions

## C4.1 — Définition des phases

On peut définir une phase de deux manières compatibles :

### (i) Par mesures (statut : définition)

Une phase est une classe de mesures stationnaires (ou de composantes ergodiques) pour lesquelles un ensemble d’observables macroscopiques possède des valeurs typiques stables.

### (ii) Par points fixes de coarse-graining (statut : définition)

Une phase est un régime où \(\pi_{\ell}\) envoie la dynamique vers une description effective stable (point fixe ou cycle court).

## C4.2 — Paramètres d’ordre (intrinsèques)

Un paramètre d’ordre est une observable \(M\) telle que :
- \(\langle M\rangle\) prend des valeurs distinctes selon les phases,
- \(\chi_M\) (susceptibilité) présente une signature de transition.

Exemples plausibles au Niveau I :
- dimension effective \(d_{\text{eff}}\) ;
- densité d’événements ;
- entropie de distribution des types ;
- longueur de corrélation d’un motif.

## C4.3 — Transition de phase

Un point critique (ou région critique) apparaît quand :
- les corrélations deviennent longues (divergence de longueur de corrélation),
- les distributions changent brutalement,
- les temps de relaxation explosent (critical slowing down).

Les notions d’exposants critiques/universalité sont importables telles quelles, mais doivent être formulées avec des distances intrinsèques.

## C4.4 — Conjecture de classification "minimaliste" des phases (statut : conjecture)

Sans s’engager sur une cosmologie, on peut conjecturer des régimes génériques :

1. **Phase crumpled** : forte connectivité, faible dimension effective, faible localité ;
2. **Phase branching** : structure arborescente, corrélations courtes ;
3. **Phase quasi-locale** : voisinages stables, dimension effective > 1, émergence de descriptions à longue portée.

Cette classification est volontairement "agnostique" : elle sert de cadre pour lire les simulations/toy models.

## C4.5 — Stabilité et métastabilité

On définit le temps de vie d’une phase comme :
- temps moyen de sortie d’un bassin d’attraction (coarse-graining),
- ou temps de passage entre composantes métastables.

---

# C5 — Nucléation dans le vide pré-géométrique

### C5.1 : Principes structurels

##### C5.1.α — Principe de localité des structures

> **Toute structure émerge localement avant de s'étendre.**

Une région de grande complexité ne peut apparaître instantanément. Elle doit croître à partir d'un germe local, événement par événement, en respectant la causalité.

La taille d'une structure à un "instant" donné est bornée par le nombre d'événements dans son passé causal.

------

##### C5.1.β — Principe de dichotomie subcritique/supercritique

> **Un motif local est soit confiné, soit capable de croissance illimitée.**

Pour chaque type de motif, deux comportements sont possibles :

- **Subcritique** : le futur causal reste borné dans toutes les histoires
- **Supercritique** : il existe au moins une histoire où le futur causal croît sans limite

Il n'y a pas d'état intermédiaire : un motif est soit dynamiquement confiné, soit potentiellement divergent.

------

##### C5.1.γ — Principe de nucléation

> **L'apparition d'un germe supercritique constitue un événement de nucléation.**

La nucléation est le moment causal où une structure capable de croissance illimitée apparaît pour la première fois. C'est une transition qualitative : avant, la région était subcritique ou inexistante ; après, elle peut diverger.

------

##### C5.1.δ — Principe de viabilité potentielle

> **Tout germe supercritique définit un "univers potentiel".**

Un germe dont le futur causal peut croître indéfiniment constitue le noyau d'une structure macroscopique émergente. Au niveau I, on ne dit pas si cet univers est "réalisé" ou "probable" — seulement qu'il est possible.

La question de la sélection (quels germes donnent des univers "viables") relève du niveau II.

------

##### C5.1.ε — Principe de multiplicité des nucléations

> **Une même histoire peut contenir plusieurs événements de nucléation indépendants.**

Si deux régions causalement disjointes nucléent chacune un germe supercritique, elles évoluent indépendamment. Une histoire peut ainsi contenir plusieurs "univers" en développement parallèle.

------

### C5.2 — Régions d'une configuration

**Définition.** Soit $H$ une configuration. Une *région* de $H$ est un sous-hypergraphe :

$$\mathcal{R} \subseteq H$$

obtenu en sélectionnant un sous-ensemble de nœuds $V(\mathcal{R}) \subseteq V(H)$ et d'hyperarêtes $E(\mathcal{R}) \subseteq E(H)$, avec les incidences induites.

**Définition (connexité).** Une région $\mathcal{R}$ est *connexe* si son 1-squelette est connexe : pour tous nœuds $u, v \in V(\mathcal{R})$, il existe un chemin d'hyperarêtes dans $\mathcal{R}$ reliant $u$ à $v$.

**Définition (taille).** La *taille* d'une région est le nombre total d'objets :

$$|\mathcal{R}| := |V(\mathcal{R})| + |E(\mathcal{R})|$$

------

### C5.2 — Motifs

**Définition.** Un *motif* est une classe d'isomorphisme de régions finies connexes.

Deux régions $\mathcal{R}, \mathcal{R}'$ (possiblement dans des configurations différentes) représentent le même motif si elles sont isomorphes comme hypergraphes étiquetés.

**Notation.** On note $[\mathcal{P}]$ la classe d'isomorphisme d'une région $\mathcal{P}$.

**Définition (occurrence).** Une *occurrence* du motif $[\mathcal{P}]$ dans une configuration $H$ est une région $\mathcal{R} \subseteq H$ telle que $\mathcal{R} \simeq \mathcal{P}$.

**Notation.** On note $\mathrm{Occ}([\mathcal{P}], H)$ l'ensemble des occurrences de $[\mathcal{P}]$ dans $H$.

------

### C5.3 — Futur causal d'une région

**Définition.** Soit $\omega$ une histoire avec événements $E(\omega)$ et configurations $(H_n)$. Soit $\mathcal{R}*0 \subseteq H*{n_0}$ une région dans une configuration de $\omega$.

Le *futur causal* de $\mathcal{R}_0$ dans $\omega$, noté $\mathcal{F}(\mathcal{R}_0, \omega)$, est le plus petit ensemble contenant :

1. Tous les objets de $\mathcal{R}_0$
2. Tous les événements $e \in E(\omega)$ tels que $\mathrm{Read}(e) \cap \mathcal{F} \neq \varnothing$ ou $\mathrm{Write}(e) \cap \mathcal{F} \neq \varnothing$
3. Tous les objets créés ou modifiés par ces événements

**Construction itérative :**

$$\mathcal{F}_0 := \mathcal{R}_0$$

$$\mathcal{F}_{k+1} := \mathcal{F}_k \cup {e \in E(\omega) : \mathrm{Read}(e) \cap \mathcal{F}_k \neq \varnothing \text{ ou } \mathrm{Write}(e) \cap \mathcal{F}_k \neq \varnothing} \cup {\text{objets affectés}}$$

$$\mathcal{F}(\mathcal{R}*0, \omega) := \bigcup*{k \in \mathbb{N}} \mathcal{F}_k$$

------

### C5.4 — Trace instantanée du futur causal

**Définition.** Pour chaque configuration $H_n$ le long de $\omega$, la *trace* du futur causal à l'instant $n$ est :

$$\mathcal{R}_n := \mathcal{F}(\mathcal{R}_0, \omega) \cap H_n$$

C'est l'ensemble des objets de $H_n$ appartenant au futur causal de $\mathcal{R}_0$.

**Interprétation.** La suite $(\mathcal{R}*n)*{n \geq n_0}$ décrit l'évolution de la région initiale : comment elle grandit, se transforme, ou disparaît.

**Propriétés :**

- $\mathcal{R}_{n_0} = \mathcal{R}_0$ (condition initiale)
- $|\mathcal{R}_n|$ est une fonction de $n$ (croissante, décroissante, ou fluctuante selon la dynamique)

------

### C5.5 — Futur causal global

**Définition.** Le *futur causal global* d'une région $\mathcal{R}_0$ est l'union sur toutes les histoires où elle apparaît :

$$\mathcal{F}^*(\mathcal{R}*0) := \bigcup*{\omega \ni \mathcal{R}_0} \mathcal{F}(\mathcal{R}_0, \omega)$$

**Interprétation :**

- $\mathcal{F}(\mathcal{R}_0, \omega)$ : ce qui arrive à $\mathcal{R}_0$ dans une histoire donnée
- $\mathcal{F}^*(\mathcal{R}_0)$ : l'ensemble de tous les futurs possibles de $\mathcal{R}_0$ dans le multivers $\Omega$

------

### C5.6 — Motifs subcritiques

**Définition.** Un motif $[\mathcal{P}]$ est *subcritique* (pour un système $(H_0, \mathcal{R})$) s'il existe une constante $M < \infty$ telle que :

$$\forall \omega \in \Omega, \ \forall H_n \in \omega, \ \forall \mathcal{R}_0 \subseteq H_n \text{ avec } \mathcal{R}_0 \simeq \mathcal{P}, \ \forall k \geq n : \quad |\mathcal{R}_k| \leq M$$

**Interprétation.** Un motif subcritique est *dynamiquement confiné* : aucune de ses occurrences, dans aucune histoire, ne peut engendrer une région de taille arbitrairement grande.

**Exemples typiques :**

- Motifs instables qui se désintègrent rapidement
- Motifs stables mais inertes (pas de règle applicable)
- Motifs oscillants entre quelques configurations bornées

------

### C5.7 — Germes supercritiques

**Définition.** Un motif $[\mathcal{G}]$ est un *germe supercritique* s'il existe :

- Une histoire $\omega \in \Omega$
- Un indice $n_0$
- Une région $\mathcal{R}*0 \subseteq H*{n_0}$ avec $\mathcal{R}_0 \simeq \mathcal{G}$

tels que :

1. **Connexité maintenue** : pour tout $n \geq n_0$, la trace $\mathcal{R}_n$ contient une composante connexe incluant l'image de $\mathcal{R}_0$
2. **Croissance non bornée** : $$\sup_{n \geq n_0} |\mathcal{R}_n| = +\infty$$

**Interprétation.** Un germe supercritique peut — dans au moins une histoire — engendrer une région connexe de taille arbitrairement grande. C'est un "noyau de Big Bang" potentiel.

------

### C5.8 — Dichotomie

**Proposition.** Pour tout motif $[\mathcal{P}]$ accessible depuis $H_0$, exactement un des cas suivants se produit :

| Cas               | Caractérisation                                              |
| ----------------- | ------------------------------------------------------------ |
| **Trivial**       | $[\mathcal{P}]$ n'apparaît dans aucune configuration accessible |
| **Subcritique**   | $[\mathcal{P}]$ apparaît, mais satisfait la borne uniforme (§3.6) |
| **Supercritique** | $[\mathcal{P}]$ est un germe au sens de §3.7                 |

**Convention.** Dans ce chapitre, *germe* désigne exclusivement un motif supercritique.

------

### C5.9 — Création d'une occurrence de motif

**Définition.** Soit $\omega$ une histoire et $e = (H, r, \iota, H')$ un événement. On dit que $e$ *crée une occurrence* du motif $[\mathcal{G}]$ si :

1. Il existe $\mathcal{R}' \subseteq H'$ avec $\mathcal{R}' \simeq \mathcal{G}$
2. Pour toute région $\mathcal{R} \subseteq H$, on a $\mathcal{R} \not\simeq \mathcal{G}$

Autrement dit : le motif $[\mathcal{G}]$ est absent juste avant $e$, et présent juste après.

**Remarque.** Un événement peut créer plusieurs occurrences du même motif, ou des occurrences de motifs différents.

------

### C5.10 — Événement de nucléation

**Définition.** Soit $[\mathcal{G}]$ un germe supercritique. Un événement $e \in E(\omega)$ est un *événement de nucléation de type* $[\mathcal{G}]$ s'il satisfait :

1. **Création** : $e$ crée une occurrence $\mathcal{R}_0 \subseteq H'$ avec $\mathcal{R}_0 \simeq \mathcal{G}$
2. **Divergence** : le futur causal de $\mathcal{R}_0$ dans $\omega$ satisfait : $$\sup_n |\mathcal{R}_n| = +\infty$$
3. **Minimalité causale** : il n'existe pas $e' \prec e$ dans $\omega$ qui soit un événement de nucléation de type $[\mathcal{G}]$

**Interprétation.** La nucléation est le *premier* événement (au sens causal) où apparaît un germe dont le futur diverge effectivement dans cette histoire.

------

### C5.11 — Propriétés des nucléations

**Proposition (absence pour motifs subcritiques).** Si $[\mathcal{P}]$ est subcritique, alors il n'existe aucun événement de nucléation de type $[\mathcal{P}]$ dans aucune histoire.

*Preuve.* Par définition, le futur causal de toute occurrence d'un motif subcritique est borné. La condition de divergence (§3.10.2) ne peut donc jamais être satisfaite. ∎

**Proposition (invariance par isomorphisme).** Si $e$ est une nucléation de type $[\mathcal{G}]$ et $[\mathcal{G}'] = [\mathcal{G}]$, alors $e$ est aussi une nucléation de type $[\mathcal{G}']$.

*Preuve.* Tautologique : la nucléation est définie sur les classes d'isomorphisme. ∎

**Proposition (multiplicité).** Une histoire $\omega$ peut contenir :

- Zéro nucléation (si aucun germe n'apparaît ou ne diverge)
- Une nucléation
- Plusieurs nucléations de même type (régions causalement disjointes)
- Plusieurs nucléations de types différents

------

### C5.12 — Régions causalement disjointes

**Définition.** Deux régions $\mathcal{R}_1, \mathcal{R}_2$ dans une histoire $\omega$ sont *causalement disjointes* si :

$$\mathcal{F}(\mathcal{R}_1, \omega) \cap \mathcal{F}(\mathcal{R}_2, \omega) = \varnothing$$

Autrement dit : leurs futurs causaux n'interagissent jamais.

**Proposition.** Si deux nucléations $e_1, e_2$ produisent des germes dans des régions causalement disjointes, alors les "univers" résultants évoluent indépendamment.

**Interprétation.** Une histoire peut contenir plusieurs "Big Bangs" simultanés (au sens causal) donnant naissance à des univers parallèles sans interaction.

------

### C5.13 — Complexité et coût des germes

Bien que ce chapitre reste au niveau I (sans probabilités), on peut relier la nucléation à la complexité combinatoire $K$.

**Définition (complexité d'un motif).** Pour un motif $[\mathcal{P}]$, on définit :

$$K([\mathcal{P}]) := K(\mathcal{P})$$

où $\mathcal{P}$ est un représentant quelconque (bien défini par invariance de $K$).

**Définition (coût de formation).** Le *coût de formation* d'un motif $[\mathcal{P}]$ depuis le vide est :

$$K_{\mathrm{form}}([\mathcal{P}]) := K([\mathcal{P}]) - K(\varnothing) = K([\mathcal{P}])$$

C'est la complexité minimale à "payer" pour créer une occurrence de $[\mathcal{P}]$.

------

### C5.14 — Principe de crédit combinatoire

**Rappel (trajectoire de crédit).** Pour une histoire $\omega$ avec configurations $(H_n)$ :

$$S_n(\omega) := K(H_n) - K(H_0)$$

**Définition (histoire admissible).** Une histoire $\omega$ est *$B$-admissible* si :

$$\forall n : \quad S_n(\omega) \geq -B$$

où $B \geq 0$ est le *budget de crédit*.

**Notation.** On note $\Omega_B := {\omega \in \Omega : \omega \text{ est } B\text{-admissible}}$.

**Interprétation.** Le principe de crédit limite les "fluctuations négatives" de complexité. Une histoire ne peut pas emprunter plus de $B$ unités de complexité au vide.

------

### C5.15 — Crédit minimal de formation

**Définition.** Pour un motif $[\mathcal{P}]$, le *crédit minimal de formation* est :

$$B_{\mathrm{form}}([\mathcal{P}]) := \inf_{\omega, n} \left \{-\min_{0 \leq k \leq n} S_k(\omega) \ \Big| \ [\mathcal{P}] \text{ apparaît dans } H_n(\omega) \right\}$$

C'est le crédit minimal nécessaire pour qu'une histoire puisse faire apparaître $[\mathcal{P}]$.

**Proposition.** Si $B < B_{\mathrm{form}}([\mathcal{P}])$, alors $[\mathcal{P}]$ n'apparaît dans aucune histoire de $\Omega_B$.

**Interprétation.** Le budget $B$ agit comme un filtre : seuls les motifs avec $B_{\mathrm{form}} \leq B$ peuvent exister dans $\Omega_B$.

------

### C5.16 — Contraintes sur les germes supercritiques

**Corollaire.** Soit $[\mathcal{G}]$ un germe supercritique.

1. **Si $B < B_{\mathrm{form}}([\mathcal{G}])$** : aucune nucléation de type $[\mathcal{G}]$ n'est possible dans $\Omega_B$. Le germe est exclu par la contrainte de crédit.
2. **Si $B \geq B_{\mathrm{form}}([\mathcal{G}])$** : le germe n'est pas exclu a priori. Sa nucléation effective dépend alors uniquement de la dynamique locale (règles $\mathcal{R}$) et de la structure causale.

**Interprétation.** Le budget $B$ sélectionne quels germes sont "accessibles". Parmi ceux-ci, la distinction subcritique/supercritique reste une propriété purement dynamique.

------

### C5.17 — Structure locale de la complexité

Pour affiner l'analyse, on peut supposer que $K$ est une somme de contributions locales.

**Hypothèse (localité de $K$).** Il existe un rayon $R_K \geq 0$ et une fonction $\kappa$ sur les voisinages locaux telle que :

$$K(H) = \sum_{x \in V(H) \sqcup E(H)} \kappa([N_{R_K}(H, x)])$$

où $[N_{R_K}(H, x)]$ est la classe d'isomorphisme du voisinage de rayon $R_K$ autour de $x$.

**Hypothèse (bornes sur $\kappa$).** Il existe $\kappa_{\min}, \kappa_{\max} \in \mathbb{R}$ tels que :

$$\kappa_{\min} \leq \kappa(\nu) \leq \kappa_{\max} \quad \forall \nu$$

**Proposition (croissance linéaire).** Sous ces hypothèses :

$$\kappa_{\min} \cdot |\mathcal{R}| \leq K(\mathcal{R}) \leq \kappa_{\max} \cdot |\mathcal{R}|$$

pour toute région $\mathcal{R}$.

------

### C5.18 — Variation de complexité par événement

**Proposition.** Sous les hypothèses de localité (§3.17) et de localité bornée des règles (A1.δ), il existe une constante $C_K \geq 0$ telle que :

$$|\Delta K(e)| \leq C_K \quad \forall e \in \mathcal{E}$$

*Idée de preuve.*

- Un événement $e$ modifie au plus $O(R_{\max})$ objets
- Chaque modification affecte les contributions $\kappa$ dans un voisinage de rayon $R_K$
- Le nombre de contributions affectées est borné par $O(R_{\max} \cdot R_K)$
- Chaque contribution change d'au plus $|\kappa_{\max} - \kappa_{\min}|$

**Corollaire.** La trajectoire de crédit $S_n(\omega)$ est Lipschitzienne en $n$ :

$$|S_{n+1}(\omega) - S_n(\omega)| \leq C_K$$

------

### C5.19 — Exemple : complexité linéaire par type

**Construction.** Supposons $T_V$ et $T_E$ finis. On choisit des poids :

- $w_V : T_V \to \mathbb{R}$
- $w_E : T_E \to \mathbb{R}$

et on définit :

$$K(H) := \sum_{v \in V(H)} w_V(\sigma(v)) + \sum_{e \in E(H)} w_E(\tau(e))$$

**Propriétés :**

- C'est un cas particulier de §3.17 avec $R_K = 0$
- La variation $\Delta K(e)$ est la somme des poids créés moins les poids détruits
- Si tous les poids sont positifs, alors $K(H) \geq 0$ et $K(\varnothing) = 0$

**Interprétation.** Ce modèle simple suffit pour :

- Définir un principe de crédit
- Filtrer les motifs "trop coûteux"
- Relier la dynamique locale à un coût global

---

### C5.20 — Nucléation et Big Bang

La nucléation au niveau I est l'analogue combinatoire du Big Bang :

- Un germe supercritique est un "noyau" à partir duquel un univers peut croître
- La nucléation est l'événement fondateur, le "temps zéro" de cet univers
- Le futur causal du germe définit l'extension spatio-temporelle de l'univers

Cependant, au niveau I :

- Aucune nucléation n'est privilégiée (pas de probabilité)
- Plusieurs nucléations peuvent coexister (multivers)
- La "viabilité" d'un univers n'est pas encore définie

---

# Récapitulatif et questions ouvertes

## Ce qui est accompli dans I.C (CORE)

1. Définition claire de l’émergence (robustesse / typicalité).
2. Définition de couches émergentes sans circularité géométrique.
3. Catalogue d’observables macroscopiques intrinsèques.
4. Définition d’opérateurs de coarse-graining et de règles émergentes (grammaires effectives).
5. Deux définitions compatibles des phases (mesures / points fixes).
6. Principe de nucléation

## Conjectures principales (statut : conjectures de programme)

- existence de phases macroscopiques stables pour des familles larges de \((\mathcal R,K,\beta)\) ;
- existence de points fixes universels sous coarse-graining ;
- possibilité d’une phase quasi-locale permettant une description géométrique effective.

## Questions ouvertes

- Quelles conditions minimales sur \(\mathcal R\) garantissent non-explosion / stabilité statistique ?
- Comment choisir \(K\) (ou une famille de coûts) compatibles avec l’universalité ?
- Quels coarse-grainings sont "physiquement naturels" (intrinsèques, peu arbitraires) ?
- Comment détecter automatiquement les phases (clustering de mesures, apprentissage de règles effectives) ?
- Classification des germes : Peut-on classifier les germes supercritiques par leur "type d'univers" résultant ?
- Germe minimal : Existe-t-il un germe supercritique de complexité minimale ?
- Unicité : Un germe donné produit-il toujours le "même" univers (à isomorphisme près), ou des univers radicalement différents selon l'histoire ?
- Interaction entre univers : Deux régions initialement disjointes peuvent-elles fusionner causalement plus tard ?

