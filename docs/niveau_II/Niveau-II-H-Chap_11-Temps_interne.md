# Chapitre 11 — Temps interne d'un observateur

---

## Introduction

Le niveau I ne contient pas de temps fondamental — seulement un ordre causal partiel. Le niveau II introduit des mesures et des phases, mais toujours sans temps absolu.

Ce chapitre montre comment un temps émergent apparaît pour un observateur :
- Le "temps interne" est défini par les changements d'état de mémoire de l'observateur
- C'est une paramétrisation monotone des événements internes
- Il n'est unique qu'à reparamétrisation près (pas d'unité absolue)

> **Point clé :** Le temps n'est pas une donnée primitive. Il émerge de la structure causale vue par un observateur — c'est la succession de ses expériences qui définit son "horloge".

---

## Partie I : Noyau ontologique

### 11.I.α — Principe de temps comme changement interne

> **Le temps d'un observateur est défini par les changements de son état de mémoire.**

Un "instant" pour l'observateur correspond à un état de sa mémoire interne. Le "passage du temps" correspond à la transition d'un état de mémoire à un autre.

Sans changement de mémoire, il n'y a pas de temps vécu.

---

### 11.I.β — Principe d'ordre causal interne

> **Les événements internes de l'observateur héritent de l'ordre causal global.**

La relation causale $\prec$ de l'univers induit une relation $\prec_{\mathrm{int}}$ sur les événements qui modifient la mémoire de l'observateur. Cette relation est un ordre partiel.

---

### 11.I.γ — Principe de linéarisation

> **Le temps interne est une extension linéaire (non canonique) de l'ordre causal interne.**

L'ordre causal interne $\prec_{\mathrm{int}}$ est en général un ordre partiel : il peut exister des événements internes concurrents (non comparables). Pour qu’un observateur vive une succession d’expériences, on choisit une extension linéaire (un ordre total compatible) de cet ordre partiel.

**Remarque (jauge de codage).** Lorsque deux événements internes sont concurrents, leur ordre dans une linéarisation est un choix de représentation. Les quantités opérationnelles doivent être :

- invariantes sous la permutation d’événements concurrents qui commutent sur le support de la mémoire, ou
- définies par agrégation/moyennage sur l’ensemble des linéarisations admissibles.

**Hypothèse optionnelle (sérialité interne).** Dans de nombreuses phases stables, on postulera que les événements qui modifient effectivement la mémoire d’un même observateur sont toujours comparables par $\prec_{\mathrm{int}}$. Dans ce cas, l’ordre vécu est essentiellement unique (à reparamétrisation près).

---

### 11.I.δ — Principe de liberté de paramétrisation

> **Le temps interne n'est défini qu'à reparamétrisation monotone près.**

Il n'existe pas de "valeur absolue" du temps. Toute bijection strictement croissante entre deux paramétrisations donne une horloge également valide.

L'unité de temps, l'origine, et l'échelle sont des conventions.

---

### 11.I.ε — Principe d'horloge interne

> **Certains sous-systèmes de l'observateur peuvent servir d'horloge.**

Si un sous-ensemble de la mémoire évolue de manière strictement monotone (compteur, oscillateur...), il fournit une paramétrisation naturelle du temps interne.

---

## Partie II : Choix de représentation

### 11.1 — Cadre : observateur dans un univers

On se place dans :
- Un système $(H_0, \mathcal{R}, K, B)$ de niveau I
- Un vide sélectionné $(\Omega_B, \Sigma_B, \mu_\beta, \Theta)$
- Un type d'univers émergent $u \in \mathcal{M}_{\mathrm{univ}}$
- La mesure size-biased $\mu_\beta^{\{u\}}$

Dans un univers microscopique $U = U_n(\omega)$ de type $u$, on considère un motif observateur :

$$\mathcal{O} = (R, s_{C_\Sigma(R)})$$

avec :
- $R$ : région structurale dans $\mathcal{U}(e_n, \omega)$
- $M \subseteq C_\Sigma(R)$ : mémoire interne
- $\pi_M : \mathcal{S}_{C_\Sigma(R)} \to \mathcal{S}_M$ : projection sur la mémoire
- $m := \pi_M(s_{C_\Sigma(R)}) \in \mathcal{S}_M$ : état de mémoire

**Lien avec le Chapitre 10.** La mémoire $M$ est une sous-structure informationnelle (cellules + dynamique de copie) ; son existence et sa stabilité seront, au niveau II, soumises à un compromis sélectionnel (coût informationnel dans le principe S), afin d’éviter une “mémoire gratuite”.


---

### 11.2 — Événements internes et trace

#### 11.2.1 — Évolution de la mémoire

L'évolution augmentée de l'univers :

$$\widehat{H}_0, \widehat{H}_1, \widehat{H}_2, \ldots$$

induit une suite d'états de mémoire :

$$m_k := \pi_M(s^{(k)}_{C_\Sigma(R)}) \in \mathcal{S}_M$$

La suite $(m_k)_{k \geq 0}$ est la trace interne brute de l'observateur. Les indices $k$ sont définis par rapport à une linéarisation fixée du poset causal global. Les propriétés internes ne dépendent pas du choix de cette linéarisation.

**Remarque (concurrence et invariance).** Si deux événements globaux sont concurrents et n’affectent pas la mémoire $M$, permuter leur ordre ne change pas la trace $(m_k)$. Si des événements concurrents affectent $M$, l’ordre vécu dépend d’une résolution (arbitrage) : on exigera alors soit la sérialité interne, soit une définition des observables internes robuste sous changement de linéarisation (voir 11.3).



#### 11.2.2 — Événements de mise à jour

La trace brute $(m_k)$ contient beaucoup d’étapes où la mémoire ne change pas. On isole donc les instants où l’observateur met effectivement à jour sa mémoire.

**Définition (Indices de mise à jour).** On définit l’ensemble des indices de mise à jour :
$$
E_{\mathrm{int}}(U,\mathcal O) := \{\,k\ge 0\; :\; m_{k+1}\neq m_k\,\}.
$$
Autrement dit, $k\in E_{\mathrm{int}}$ si et seulement si la transition globale $\widehat e_k: \widehat H_k\to \widehat H_{k+1}$ induit une modification de l’état de mémoire.

**Définition (Événements internes).** L’ensemble des événements internes (au sens “événements vécus”) est :
$$
E_{\mathrm{int}}^{\mathrm{ev}}(U,\mathcal O) := \{\,\widehat e_k\in E(U) : k\in E_{\mathrm{int}}\,\}.
$$

**Remarque (localité).** Dans les constructions usuelles (Chapitre 10), le fait que $m_{k+1}\neq m_k$ dépend d’un voisinage causal borné autour de la région $R$ et des cellules $M\subseteq C_\Sigma(R)$.

#### 11.2.3 — Trace réduite

**Définition 11.1 (Trace interne réduite).** On énumère les indices de mise à jour :

$$E_{\mathrm{int}} = \{k_0 < k_1 < k_2 < \cdots\}$$

La **trace réduite** est :

$$m^\#_j := m_{k_j}, \quad j \geq 0$$

C'est la suite des états internes successifs distincts vus par l'observateur.

**Interprétation :** L'indice $j$ compte les "moments d'expérience" — chaque changement de mémoire correspond à un événement vécu.

---

### 11.3 — Ordre causal interne (réalisation de 11.I.β)

#### 11.3.1 — Restriction de la causalité

Soit $E(U)$ l'ensemble des événements de l'univers $U$, muni de la relation causale globale $\prec$ (définie au niveau I à partir des dépendances Write/Read).

On restreint cette causalité aux seuls événements internes :
$$
E_{\mathrm{int}}^{\mathrm{ev}}(U, \mathcal{O}) := \{\widehat{e}_k \in E(U) : k \in E_{\mathrm{int}}\}.
$$

**Définition (Causalité interne).** On définit la relation causale interne par restriction :
$$
\prec_{\mathrm{int}} \, :=\, \prec\;\cap\;\bigl(E_{\mathrm{int}}^{\mathrm{ev}}\times E_{\mathrm{int}}^{\mathrm{ev}}\bigr).
$$

**Proposition 11.2.** $(E_{\mathrm{int}}^{\mathrm{ev}},\prec_{\mathrm{int}})$ est un poset (ordre partiel strict), hérité de la causalité globale.

**Choix d’une linéarisation interne.** L’énumération $E_{\mathrm{int}}=\{k_0<k_1<\dots\}$ induit un ordre total de jauge sur $E_{\mathrm{int}}^{\mathrm{ev}}$ via $j\mapsto \widehat e_{k_j}$. Cet ordre total est une extension linéaire de $\prec_{\mathrm{int}}$ dès lors que la linéarisation globale utilisée pour indexer les $\widehat e_k$ respecte la causalité (extension linéaire du poset global).

**Hypothèse optionnelle (sérialité interne).** On dira que $\mathcal O$ est *sériel* si, pour toute paire d’événements internes $e,f\in E_{\mathrm{int}}^{\mathrm{ev}}$ qui modifient la mémoire, on a $e\prec_{\mathrm{int}} f$ ou $f\prec_{\mathrm{int}} e$. Dans ce cas, l’ordre vécu ne dépend pas du choix de linéarisation (à reparamétrisation près).

#### 11.3.2 — Chronologie interne

**Définition 11.3 (Chronologie interne).** La chronologie interne de $\mathcal{O}$ dans $U$ est le triplet :
$$
\Bigl((m^\#_j)_{j\ge 0},\; (E_{\mathrm{int}}^{\mathrm{ev}},\prec_{\mathrm{int}}),\; \iota\Bigr),
$$
où $\iota:\mathbb N\to E_{\mathrm{int}}^{\mathrm{ev}}$ envoie $j$ sur l’événement $\widehat e_{k_j}$ (ordre de jauge induit par l’énumération).

**Interprétation.**
- La suite $(m^\#_j)$ est la succession des états de mémoire distincts (“instants vécus”).
- Le poset $(E_{\mathrm{int}}^{\mathrm{ev}},\prec_{\mathrm{int}})$ encode les contraintes causales internes (certaines mises à jour peuvent être concurrentes).
- Le choix $\iota$ fixe une résolution linéaire de ces contraintes (une manière de raconter l’expérience comme une suite).

**Cas sérialisé.** Si l’hypothèse de sérialité interne est satisfaite, alors $\prec_{\mathrm{int}}$ ordonne déjà les mises à jour : la chronologie interne est essentiellement unique (l’extension linéaire n’ajoute pas d’arbitraire).

Dans la suite, nous considérons principalement le cas où l’observateur subit une infinité de mises à jour (sinon la chronologie interne est simplement finie).

---
---

### 11.4 — Temps interne (réalisation de 11.I.γ et 11.I.δ)

#### 11.4.1 — Définition abstraite

**Définition 11.4 (Temps interne).** Un temps interne pour l'observateur $\mathcal{O}$ dans l'univers $U$ est :

1. Un ensemble totalement ordonné $(T_\mathcal{O}, \leq_\mathcal{O})$
2. Une application strictement croissante :
   $$\tau_\mathcal{O} : E_{\mathrm{int}}^{\mathrm{ev}} \to T_\mathcal{O}$$
   telle que :
   $$e \prec_{\mathrm{int}} f \implies \tau_\mathcal{O}(e) <_\mathcal{O} \tau_\mathcal{O}(f)$$

La valeur $\tau_\mathcal{O}(e)$ est le "moment interne" de l'événement $e$.

#### 11.4.2 — Temps canonique

L'indexation $j \mapsto \widehat{e}_{k_j}$ définit un temps interne canonique :

$$T_\mathcal{O} = \mathbb{N}, \quad \tau_\mathcal{O}(\widehat{e}_{k_j}) := j$$

C'est le "comptage des expériences" — le temps le plus simple possible.

#### 11.4.3 — Liberté de reparamétrisation

**Proposition 11.5 (Reparamétrisation).** Si $\tau_\mathcal{O}$ et $\tau'_\mathcal{O}$ sont deux temps internes pour le même observateur, alors il existe une bijection strictement croissante :

$$f : \tau_\mathcal{O}(E_{\mathrm{int}}^{\mathrm{ev}}) \to \tau'_\mathcal{O}(E_{\mathrm{int}}^{\mathrm{ev}})$$

telle que $\tau'_\mathcal{O} = f \circ \tau_\mathcal{O}$.

**Interprétation :**
- Pas de "valeur absolue" du temps
- Seulement une classe d'équivalence de paramétrisations monotones
- Changement d'unité, d'origine, d'échelle = changement de $f$

---

### 11.5 — Horloges internes (réalisation de 11.I.ε)

#### 11.5.1 — Définition

**Définition 11.6 (Horloge interne).** Une horloge interne pour $\mathcal{O}$ est :

1. Un sous-ensemble $C_{\mathrm{clk}} \subseteq M$ de cellules de mémoire
2. Une fonction de lecture :
   $$\mathrm{clk} : \mathcal{S}_{C_{\mathrm{clk}}} \to T_\mathcal{O}$$
   

telle que la suite :

$$t_j := \mathrm{clk}\bigl(\text{restriction de } m^\#_j \text{ à } C_{\mathrm{clk}}\bigr)$$

soit strictement croissante dans $T_\mathcal{O}$.

#### 11.5.2 — Exemples d'horloges

| Type d'horloge | Description |
|----------------|-------------|
| **Compteur** | Cellules encodant un entier incrémenté à chaque événement |
| **Oscillateur** | Motif périodique avec comptage de cycles |
| **Accumulation** | Mesure d'une quantité croissante (entropie, volume...) |

**Remarque :** L'horloge peut dépendre de l'environnement, mais elle doit rester monotone pour définir un temps cohérent.

---

### 11.6 — Processus observés et stationnarité

#### 11.6.1 — Suite d'observations

Du point de vue de l'observateur, l'évolution de son environnement est perçue comme une suite de photographies indexées par le temps interne.

Formellement, l'univers $U$ + observateur $\mathcal{O}$ + procédure de mesure définissent une suite :

$$X_0, X_1, X_2, \ldots$$

où $X_j \in \mathcal{Y}$ (espace des observations possibles) est l'observation à l'"instant" $j$.

#### 11.6.2 — Stationnarité interne

La stationnarité de $\mu_\beta^{\{u\}}$ sous le décalage global $\Theta$ ne suffit pas, à elle seule, à garantir la stationnarité de la sous-suite indexée par les mises à jour internes (car le choix des indices $k_j$ dépend de l’histoire).

On distinguera donc deux niveaux :

1) **Stationnarité globale (jauge).** $\mu_\beta^{\{u\}}$ est stationnaire pour $\Theta$ (Chapitre 4–6).

2) **Stationnarité du processus pointé (mises à jour).** On suppose que le processus des mises à jour internes admet une intensité stationnaire et une espérance de pas finie :
$$
\rho^{-1} := \mathbb E_{\mu_\beta^{\{u\}}}[k_{j+1}-k_j] < \infty.
$$
Sous cette hypothèse (et des conditions techniques standard), on peut définir une dynamique induite “de mise à jour en mise à jour” :
$$
\Theta_{\mathrm{int}}(\omega) := \Theta^{\tau(\omega)}(\omega),
$$
où $\tau(\omega)=\min\{n\ge 1:\; n\in E_{\mathrm{int}}(\omega)\}$ est le premier temps de mise à jour après 0. La mesure “vue depuis une mise à jour typique” (type Palm/induite) est alors stationnaire pour $\Theta_{\mathrm{int}}$.

Dans ce cas, le processus $(X_j)$ peut être stationnaire :
$$
\mathcal{L}(X_0, \ldots, X_n) = \mathcal{L}(X_k, \ldots, X_{k+n}) \quad \forall k,
$$
dès que chaque $X_j$ dépend d’un voisinage causal borné autour de l’événement interne $\widehat e_{k_j}$ et d’une procédure de lecture fixée.

**Conséquence.** L’observateur voit des régularités invariantes dans son temps interne — base opérationnelle des “lois effectives” (Chapitre 12).

---

## Résumé de la structure

```
CHAPITRE 11 — TEMPS INTERNE
│
├── Partie I : NOYAU ONTOLOGIQUE (5 principes)
│   ├── 11.I.α  Temps = changement interne    [m_k → m_{k+1}]
│   ├── 11.I.β  Ordre causal interne          [≺_int sur E_int]
│   ├── 11.I.γ  Linéarisation                 [ordre total]
│   ├── 11.I.δ  Liberté de paramétrisation    [unique mod f croissante]
│   └── 11.I.ε  Horloge interne               [sous-système dédié]
│
└── Partie II : REPRÉSENTATION (6 sections)
    ├── 11.1  Cadre                           [O dans U de type u]
    ├── 11.2  Trace interne                   [(m_k), (m^#_j)]
    ├── 11.3  Ordre causal interne            [(E_int, ≺_int)]
    ├── 11.4  Temps interne                   [τ_O : E_int → T_O]
    ├── 11.5  Horloges                        [clk : S_C_clk → T_O]
    └── 11.6  Processus observés              [(X_j), stationnarité]
```

---

## Remarques critiques

### Sur la nature du temps émergent

Le temps interne défini ici est relationnel — il n'existe que par rapport à l'observateur. Différents observateurs dans le même univers peuvent avoir des temps internes différents (et non synchronisables a priori).

**Question ouverte :** Comment définir une notion de "temps commun" pour plusieurs observateurs ? Cela nécessiterait une procédure de synchronisation basée sur des signaux causaux.

### Sur la liberté de reparamétrisation

Le principe 11.I.δ affirme que le temps n'est défini qu'à bijection monotone près. C'est plus faible que la relativité générale, qui permet des difféomorphismes sur l'espace-temps.

**Lien possible :** Si l'espace émergent (chapitre 12) est également défini à reparamétrisation près, on retrouve une forme de "covariance" émergente.

### Sur l'absence de flèche du temps fondamentale

L'ordre causal $\prec$ impose une orientation *passé → futur* au sens des dépendances (Write/Read). En revanche, le cadre ne fournit aucune métrique temporelle fondamentale : pas d’unité absolue, pas de “durée” primitive.

Il faut toutefois distinguer deux idées :

- Inverser $\prec$ (échanger passé/futur dans le graphe) n’est pas, en général, une symétrie de la théorie.
- Une véritable symétrie de renversement du temps exigerait une structure de réversibilité (règles inversibles, ou paires de règles, et une mesure compatible — type balance détaillée / “detailed balance” au niveau II).

La “flèche du temps” au sens thermodynamique (croissance d’entropie) et au sens informationnel (accumulation de traces et de témoins) devrait émerger de :
- conditions initiales (faible entropie effective) et/ou
- sélection par $\mu_\beta$ / principe S (favorisant certains régimes) et/ou
- irréversibilité pratique liée à la redondance des enregistrements (Chapitre 10).

Ce chapitre se limite à définir le temps interne comme paramétrisation monotone des mises à jour de mémoire ; la dérivation d’une flèche macroscopique est reportée.

---

## Lien avec les autres chapitres

| Chapitre | Relation avec Ch.11 |
|----------|---------------------|
| Ch.10 (Information) | Définit la mémoire $M$ et les témoins |
| Ch.9 (Univers) | Fournit l'univers $U$ et la mesure $\mu_\beta^{\{u\}}$ |
| Ch.12 (Lois) | Utilise le temps interne pour définir les processus $(X_j)$ |

---

## Glossaire du chapitre

| Terme | Définition |
|-------|------------|
| **Trace interne brute** | $(m_k)_{k \geq 0}$ |
| **Événement interne** | $\widehat{e}_k$ avec $m_k \neq m_{k-1}$ |
| **Trace réduite** | $(m^\#_j)_{j \geq 0}$ |
| **Chronologie interne** | Structure $(m^\#_j, E_{\mathrm{int}}, \iota)$ |
| **Temps interne** | $\tau_\mathcal{O} : E_{\mathrm{int}}^{\mathrm{ev}} \to T_\mathcal{O}$ |
| **Horloge interne** | Sous-système donnant une paramétrisation |
| **Reparamétrisation** | Bijection monotone entre temps |

