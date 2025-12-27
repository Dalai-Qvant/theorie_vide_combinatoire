# Niveau I.C — Émergence

---

## Table des matières

- [Introduction](#introduction)
- [C0 — Qu’est-ce que l’émergence ?](#c0--quest-ce-que-lémergence-)
- [C1 — Couches émergentes (définition combinatoire)](#c1--couches-émergentes-définition-combinatoire)
- [C2 — Observables macroscopiques (sans géométrie présupposée)](#c2--observables-macroscopiques-sans-géométrie-présupposée)
- [C3 — Coarse-graining intrinsèque et "renormalisation" des règles](#c3--coarse-graining-intrinsèque-et-renormalisation-des-règles)
- [C4 — Phases et transitions](#c4--phases-et-transitions)
- [Encadrés Preview (vers les Niveaux II–IV)](#encadrés-preview-vers-les-niveaux-iiiv)
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

# Vers les niveaux II–IV

> Ces encadrés donnent la feuille de route. Ils sont volontairement formulés comme objectifs / conjectures / programmes, pas comme résultats acquis ici.

## Preview A — Limite quasi-lisse et notions métriques (vers niveau IV)

À ce stade, le niveau I fournit surtout :
- des indicateurs de quasi-régularité,
- des opérateurs de coarse-graining,
- et des observables de type "dimension effective".

Objectif : définir, à partir de \(L_{\text{geo}}\),

- une notion de métrique effective,
- une signature lorentzienne (si pertinente),
- puis une action effective.

## Preview B — Symétries continues et Noether (vers niveau IV)

Idée : si, à grande échelle, les statistiques deviennent invariantes sous une famille continue de transformations effectives, alors une description actionnelle (si elle existe) devrait exhiber des quantités conservées.

Au niveau I, on se limite à mesurer l’émergence statistique des invariances ; l’énoncé "Noether" appartient au cadre effectif.

## Preview C — Observateurs et quantique (vers niveau III)

Au niveau I, on peut seulement définir un observateur minimal comme :
- un sous-système avec mémoire finie,
- accédant à une interface \(\partial R\) via des opérations de lecture,
- et construisant des résumés compressés de son flux d’expérience.

La reconstruction "états convexes → Hilbert/Born/contextualité" sera traitée au niveau III.

## Preview D — Prédictions et tests (vers niveau IV)

Les signatures observables (violations de Lorentz, corrections de dispersion, signatures cosmologiques…) nécessitent :
- un modèle effectif explicite,
- une identification précise des observables physiques,
- et un couplage aux données.

Le niveau I ne vise pas ces prédictions directement ; il prépare les outils pour y arriver.

---

# Récapitulatif et questions ouvertes

## Ce qui est accompli dans I.C (CORE)

1. Définition claire de l’émergence (robustesse / typicalité).
2. Définition de couches émergentes sans circularité géométrique.
3. Catalogue d’observables macroscopiques intrinsèques.
4. Définition d’opérateurs de coarse-graining et de règles émergentes (grammaires effectives).
5. Deux définitions compatibles des phases (mesures / points fixes).

## Conjectures principales (statut : conjectures de programme)

- existence de phases macroscopiques stables pour des familles larges de \((\mathcal R,K,\beta)\) ;
- existence de points fixes universels sous coarse-graining ;
- possibilité d’une phase quasi-locale permettant une description géométrique effective.

## Questions ouvertes

- quelles conditions minimales sur \(\mathcal R\) garantissent non-explosion / stabilité statistique ?
- comment choisir \(K\) (ou une famille de coûts) compatibles avec l’universalité ?
- quels coarse-grainings sont "physiquement naturels" (intrinsèques, peu arbitraires) ?
- comment détecter automatiquement les phases (clustering de mesures, apprentissage de règles effectives) ?

