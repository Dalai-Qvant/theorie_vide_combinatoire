# Niveau I.A — Axiomes fondamentaux

### **Vide pré-géométrique et structure minimale**

---

## Table des matières

- [Préambule](#préambule)
- [A0 — Substrat combinatoire](#a0--substrat-combinatoire)
  - [Partie I : Noyau ontologique](#partie-i--noyau-ontologique)
  - [Partie II : Choix de représentation](#partie-ii--choix-de-représentation)
- [A1 — Règles locales de réécriture](#a1--règles-locales-de-réécriture)
  - [Partie I : Principes fondamentaux](#partie-i--principes-fondamentaux-1)
  - [Partie II : Formalisation mathématique](#partie-ii--formalisation-mathématique)
- [A2 — Structure causale locale](#a2--structure-causale-locale)
  - [Partie I : Principes de causalité](#partie-i--principes-de-causalité)
  - [Partie II : Propriétés et conséquences](#partie-ii--propriétés-et-conséquences)
- [A3 — Espace des histoires](#a3--espace-des-histoires)
  - [Partie I : Construction de Ω](#partie-i--construction-de-ω)
  - [Partie II : Mesure statistique](#partie-ii--mesure-statistique)
- [Récapitulatif et notations](#récapitulatif-et-notations)

---

## Préambule

### Philosophie générale

Les axiomes A0-A3 constituent le noyau minimal universel de la théorie. Ils définissent la classe la plus générale d'hypergraphes dynamiques avec évolution locale exhaustive, sans référence à :

- **La géométrie** : pas de métrique, pas de dimension présupposée
- **La mécanique quantique** : pas d'espace de Hilbert, pas de règle de Born
- **Les symétries** : pas de groupe d'invariance imposé
- **La réversibilité** : perte d'information autorisée à ce niveau
- **Les probabilités** : pas de mesure de probabilité (avant A3)

Ces axiomes décrivent tous les univers possibles : réversibles ou non, quantiques ou classiques, symétriques ou asymétriques, infinis ou finis.

### Stratégie de construction

Chaque axiome suit une structure en deux parties :

**Partie I — Noyau ontologique** : Énoncés qualitatifs minimaux, indépendants de toute représentation mathématique particulière. Ce sont les principes fondamentaux qui définissent la nature du système.

**Partie II — Choix de représentation** : Conventions mathématiques choisies pour représenter les principes. Ces choix sont utiles mais non uniques : d'autres représentations pourraient être utilisées tant qu'elles respectent les principes de la Partie I.

Cette distinction permet de séparer clairement :
- Ce qui est nécessaire (ontologie)
- Ce qui est choisi (représentation)

### Principe directeur : Le vide comme potentialité

L'intuition fondamentale est que le vide pré-géométrique n'est pas le "néant absolu" (∅), mais un état de potentialités. Il n'est pas "rien", mais plutôt "tout ce qui peut se produire". Cette idée sera formalisée progressivement :

1. **A0** : Le vide possède une structure relationnelle minimale
2. **A1** : Il est soumis à des transformations locales
3. **A2** : Ces transformations génèrent une structure causale
4. **A3** : Le vide "est" l'espace Ω de toutes les histoires possibles

---

# A0 — Substrat combinatoire

**Le vide comme ensemble de relations entre entités indiscernables**

---

## Partie I : Noyau ontologique

Les cinq principes suivants définissent la nature minimale de la réalité dans ce cadre. Ils sont **irréductibles** : retirer l'un d'eux détruirait la cohérence du système.

### A0.α — Principe du substrat relationnel

> **Le vide pré-géométrique est un ensemble fini de relations entre entités indiscernables.**

**Énoncé détaillé** :

La réalité fondamentale consiste en :
1. **Entités** : un ensemble $V$ (possiblement vide) d'éléments sans structure interne
2. **Relations** : un ensemble $E$ (possiblement vide) de liens entre entités
3. **Configuration** : la donnée de quelles entités sont liées par quelles relations

**Justification philosophique** :

Ce principe rejette deux ontologies classiques :
- **Substantialisme** : "La réalité consiste en substances dotées de propriétés intrinsèques"
- **Platonisme** : "Les entités possèdent une identité absolue"

Au contraire, il adopte une **ontologie strictement relationnelle** : seule la structure des relations a un sens. Les "entités" ne sont que des nœuds d'un réseau ; elles n'ont pas de "nature propre" en dehors des relations dans lesquelles elles participent.

**Analogie** : Pensez à un réseau social. Les personnes (entités) n'ont de sens que par leurs connexions (relations). Deux réseaux avec la même structure de connexions sont identiques, même si les "noms" des personnes diffèrent.

**Conséquence** : Il n'y a pas d'"espace" ou de "temps" à ce niveau. L'espace-temps émergera plus tard comme propriété statistique de la dynamique relationnelle.

---

### A0.β — Principe d'indiscernabilité (relationalité pure)

> **Seule la structure relationnelle a un sens. L'identité des entités n'en a pas.**

**Énoncé détaillé** :

Deux configurations qui ne diffèrent que par un **renommage** (permutation) des entités et des relations représentent le **même état physique**.

L'état physique est une **classe d'équivalence sous permutation**, non une configuration particulière.

**Justification philosophique** :

Ce principe est l'analogue pré-géométrique du **principe d'identité des indiscernables** de Leibniz, mais radicalisé :

- **Leibniz** : "Deux objets avec exactement les mêmes propriétés sont identiques"
- **Ici** : "Les entités n'ont aucune propriété intrinsèque, donc elles sont toutes indiscernables"

**Conséquence mathématique** :

Si on représente une configuration comme un tuple $(V, E, \text{données})$, deux tuples liés par une permutation
$$\pi : V \to V', \quad \phi : E \to E'$$
représentent le **même état**.

**Exemple** :

Considérons deux configurations :
- $H_1$ : Trois entités $\{a, b, c\}$ avec une relation liant $\{a, b\}$
- $H_2$ : Trois entités $\{x, y, z\}$ avec une relation liant $\{x, y\}$

Ces configurations sont **physiquement identiques** (isomorphes). Le choix des "noms" $a, b, c$ vs $x, y, z$ est sans signification physique.

**Implication profonde** :

Ce principe élimine toute notion d'**haeccéité** (l'identité particulière d'une entité au-delà de ses propriétés). C'est une forme extrême de **réalisme structural** : la structure est tout, les "porteurs" de la structure ne sont rien.

---

### A0.γ — Principe du vide

> **L'état fondamental est l'absence de structure.**

**Énoncé détaillé** :

Il existe une configuration distinguée $\varnothing = (V = \varnothing, E = \varnothing)$, appelée **vide**, qui ne contient ni entité ni relation.

**Justification** :

Le vide n'est pas un "état parmi d'autres" mais l'**état de référence** : celui qui ne possède aucune structure. C'est l'analogue du zéro en mathématiques : le point neutre par rapport à l'ajout de structure.

**Propriétés du vide** :

1. **Unicité** : À isomorphisme près, il n'existe qu'un seul vide (la classe d'équivalence de $\varnothing$)
2. **Neutralité** : Le vide est invariant sous toute permutation (il n'y a rien à permuter)
3. **Minimalité** : Toute autre configuration possède "plus de structure" que le vide

**Note subtile** : Le vide $\varnothing$ (configuration sans structure) n'est **pas** le néant absolu. C'est un **état possible** du système. La différence sera cruciale en A0.δ.

---

### A0.δ — Principe de potentialité

> **Le vide n'est pas un état déterminé, mais l'ensemble de toutes les histoires possibles.**

**Énoncé détaillé** :

Le vide pré-géométrique n'est **pas** identifié à la configuration $\varnothing$, mais à l'**espace $\Omega$** de toutes les évolutions compatibles avec les règles de transformation (définies en A1).

Toute configuration accessible apparaît dans au moins une histoire.

**Justification philosophique** :

Ce principe est le cœur de la **distinction entre acte et puissance** :
- **Configuration $\varnothing$** : un état particulier (acte)
- **Vide pré-géométrique $\Omega$** : toutes les potentialités (puissance)

Le vide n'est pas "rien en acte", mais "tout en puissance".

**Analogie quantique** :

En mécanique quantique, un état n'est pas un point de l'espace de Hilbert, mais une superposition. Ici, l'univers n'est pas une configuration $H$, mais une **superposition de toutes les histoires** $\omega \in \Omega$.

**Formulation mathématique (anticipée)** :

Le vide pré-géométrique est :
$$\text{Vide} = \Omega = \{ \omega : \omega \text{ est une histoire compatible avec les règles} \}$$

**Conséquence fondamentale** :

Ce principe transforme la question "Quel est l'état initial de l'univers ?" en "Quelles histoires sont possibles ?". C'est un passage d'une **ontologie d'objets** à une **ontologie d'histoires**.

**Lien avec A3** : Ce principe sera rigoureusement capturé en A3, où nous construirons explicitement l'espace $\Omega$.

---

### A0.ε — Principe de coût

> **Toute structure a un coût combinatoire relatif au vide.**

**Énoncé détaillé** :

Il existe une fonction $K$ sur les configurations (classes d'isomorphisme) telle que :

1. **Normalisation** : $K(\varnothing) = 0$ (le vide a un coût nul)
2. **Invariance** : $K$ ne dépend que de la classe d'équivalence sous permutation (cohérence avec A0.β)
3. **Additivité** : Sur des composantes déconnectées, $K(H_1 \sqcup H_2) = K(H_1) + K(H_2)$
4. **Non-bornitude** : $K$ n'est pas bornée supérieurement (les configurations peuvent avoir un coût arbitrairement grand)

**Justification** :

Ce principe introduit une **proto-thermodynamique** : certaines configurations "coûtent" plus que d'autres. Le coût mesure "combien de structure" existe par rapport au vide.

**Nature du coût** :

À ce stade, nous ne spécifions **pas** ce que "coût" signifie physiquement. Il pourrait s'agir de :
- Complexité de Kolmogorov (information minimale pour décrire $H$)
- Nombre de relations et d'entités
- Une mesure plus sophistiquée dépendant des voisinages locaux

Le principe A0.ε affirme simplement qu'une **telle fonction existe**. Sa forme explicite sera un **choix de modèle** (Partie II).

**Lien avec la thermodynamique** :

Le coût $K$ joue un rôle analogue à l'**énergie** en thermodynamique. Plus tard (A3), nous introduirons une température $\beta^{-1}$ et une mesure $\mu_\beta \propto e^{-\beta K}$, faisant de ce cadre une **mécanique statistique combinatoire**.

**Lien avec le principe S** (Niveau II) :

Le principe S sélectionnera des univers pour lesquels une action locale $I$ est stationnaire. Le coût $K$ sera lié à cette action, permettant de dériver les équations du mouvement.

---

## Résumé de la Partie I

Les cinq principes ontologiques forment un système cohérent :

| Principe | Rôle |
|----------|------|
| **A0.α (Substrat)** | Définit la nature de la réalité : relations entre entités |
| **A0.β (Indiscernabilité)** | Élimine toute identité intrinsèque : structure pure |
| **A0.γ (Vide)** | Pose un état de référence : absence de structure |
| **A0.δ (Potentialité)** | Redéfinit le vide : espace des histoires possibles |
| **A0.ε (Coût)** | Introduit une hiérarchie : certaines structures "coûtent" plus |

**Statut épistémologique** : Ces principes sont des **axiomes**. On ne les dérive pas, on les **pose** comme fondements. Leur justification est :
1. **Cohérence interne** (ils ne se contredisent pas)
2. **Minimalité** (retirer l'un d'eux affaiblit le cadre)
3. **Fécondité** (ils permettent de dériver la physique connue)

---

## Partie II : Choix de représentation

Nous choisissons maintenant une **représentation mathématique** des principes de la Partie I. Ces choix sont **conventionnels mais utiles** : d'autres représentations pourraient être employées.

### A0.1 — Représentation par hypergraphes étiquetés

**Définition formelle** :

Une **configuration** est un quintuplet $H = (V, E, S, \tau, \sigma)$ où :

- $V$ : ensemble fini d'**entités** (nœuds)
- $E$ : ensemble fini de **relations** (hyperarêtes)
- $S : E \to \mathcal{P}_{\text{fin}}(V) \setminus \{\varnothing\}$ : **support** de chaque relation
  - $\mathcal{P}_{\text{fin}}(V)$ = ensemble des sous-ensembles finis de $V$
  - $S(e)$ est l'ensemble des entités liées par la relation $e$
- $\tau : E \to T_E$ : **type** de chaque relation (étiquette)
- $\sigma : V \to T_V$ : **type** de chaque entité (étiquette)

où $T_E$ et $T_V$ sont des ensembles finis de **types** (étiquettes possibles).

**Motivation du choix** :

| Aspect | Justification |
|--------|---------------|
| **Hyperarêtes** (vs arêtes binaires) | Permet des relations d'arité arbitraire (un $e$ peut lier 1, 2, 3... entités). Les graphes classiques (arêtes binaires) sont un cas particulier. |
| **Étiquettes/types** | Permet d'encoder des degrés de liberté internes (spin, charge, etc.) sans multiplier le nombre d'entités. |
| **Finitude** | Assure que chaque configuration est un objet combinatoire bien défini. L'infini potentiel émerge de l'**espace des histoires** $\Omega$, pas des configurations individuelles. |

**Exemple concret** :

Soit une configuration avec :
- $V = \{v_1, v_2, v_3\}$ (trois entités)
- $T_V = \{\text{spin-up}, \text{spin-down}\}$ (types d'entités)
- $\sigma(v_1) = \text{spin-up}$, $\sigma(v_2) = \text{spin-down}$, $\sigma(v_3) = \text{spin-up}$
- $E = \{e_1, e_2\}$ (deux relations)
- $T_E = \{\text{attraction}, \text{répulsion}\}$ (types de relations)
- $S(e_1) = \{v_1, v_2\}$ (relation binaire)
- $S(e_2) = \{v_1, v_2, v_3\}$ (relation ternaire)
- $\tau(e_1) = \text{attraction}$, $\tau(e_2) = \text{répulsion}$

Cette configuration représente "trois entités avec spins, liées par une attraction binaire et une répulsion ternaire".

**Remarque importante** : Les étiquettes $\tau, \sigma$ sont des **conventions de représentation**. À ce stade, elles n'ont pas de signification physique : ce sont juste des "noms" pour distinguer différents types de relations/entités.

---

### A0.2 — Convention minimale (cas canonique)

Le **vide strictement minimal** correspond au choix :
$$T_V = T_E = \{\star\}$$

Dans ce cas :
- Toutes les entités sont du même type $\star$
- Toutes les relations sont du même type $\star$
- Les fonctions $\tau$ et $\sigma$ sont triviales (constantes)
- La configuration se réduit à $(V, E, S)$

**Interprétation** :

Ce choix représente un univers **complètement homogène** : il n'y a qu'un seul "type" d'entité et un seul "type" de relation. C'est le cas le plus simple possible.

**Extensions** :

Tout enrichissement $(T_V, T_E) \neq (\{\star\}, \{\star\})$ est une **extension** du modèle minimal, introduite pour des raisons de modélisation physique ultérieure.

Exemples d'extensions :
- $T_V = \{\text{quark}, \text{lepton}, \text{boson}\}$ (types de particules)
- $T_E = \{\text{électromagnétique}, \text{forte}, \text{faible}, \text{gravitationnelle}\}$ (types d'interactions)

**Stratégie** : Commencer par le cas minimal $(T_V = T_E = \{\star\})$ et introduire progressivement des étiquettes seulement si la dynamique observée le nécessite.

---

### A0.3 — Isomorphisme (réalisation technique de A0.β)

**Définition** :

Deux configurations $H = (V, E, S, \tau, \sigma)$ et $H' = (V', E', S', \tau', \sigma')$ sont **isomorphes** s'il existe des bijections :
$$\phi_V : V \to V', \quad \phi_E : E \to E'$$

préservant :
1. **Supports** : $S'(\phi_E(e)) = \phi_V[S(e)]$ pour tout $e \in E$
   - où $\phi_V[S(e)] = \{\phi_V(v) : v \in S(e)\}$
2. **Types d'hyperarêtes** : $\tau'(\phi_E(e)) = \tau(e)$ pour tout $e \in E$
3. **Types d'entités** : $\sigma'(\phi_V(v)) = \sigma(v)$ pour tout $v \in V$

**Notation** : On écrit $H \cong H'$ si $H$ et $H'$ sont isomorphes.

**Classe d'équivalence** :

Pour une configuration $H$, on note $[H]$ la **classe d'isomorphisme** :
$$[H] = \{H' : H' \cong H\}$$

**Espace des états** :

L'espace physique des états est :
$$\mathcal{C} = \{[H] : H \text{ configuration finie}\}$$

C'est l'ensemble des classes d'isomorphisme, non l'ensemble des configurations individuelles.

**Réalisation de A0.β** :

Cela formalise le principe d'indiscernabilité : deux configurations isomorphes représentent le **même état physique**. Le choix d'un représentant particulier $H \in [H]$ est arbitraire.

**Exemple** :

Les deux configurations suivantes sont isomorphes (donc identiques physiquement) :
- $H_1 : V = \{a, b\}, E = \{e\}, S(e) = \{a, b\}$
- $H_2 : V = \{x, y\}, E = \{f\}, S(f) = \{x, y\}$

La bijection $\phi_V(a) = x$, $\phi_V(b) = y$, $\phi_E(e) = f$ établit l'isomorphisme.

---

### A0.4 — Complexité combinatoire (réalisation de A0.ε)

Nous choisissons maintenant une **forme explicite** pour la fonction de coût $K$. Plusieurs choix sont possibles selon les objectifs de modélisation.

#### Option (a) : Complexité linéaire par type (cas simple)

$$K(H) = \sum_{v \in V} w_V(\sigma(v)) + \sum_{e \in E} w_E(\tau(e))$$

où :
- $w_V : T_V \to \mathbb{R}_+$ : **poids** associé à chaque type d'entité
- $w_E : T_E \to \mathbb{R}_+$ : **poids** associé à chaque type de relation

**Interprétation** :

Chaque entité de type $t$ "coûte" $w_V(t)$, chaque relation de type $r$ "coûte" $w_E(r)$. Le coût total est la somme.

**Cas minimal** : Si $T_V = T_E = \{\star\}$, alors :
$$K(H) = w_V \cdot |V| + w_E \cdot |E|$$

Le coût est proportionnel au nombre total d'entités et de relations.

**Avantages** : Simple, additif, facile à calculer.

**Limitations** : Ne prend pas en compte la structure locale (voisinages, connectivité).

#### Option (b) : Complexité locale (cas général)

$$K(H) = \sum_{x \in V \sqcup E} \kappa([N_R(H, x)])$$

où :
- $N_R(H, x)$ : **voisinage de rayon $R$** autour de $x$ (entités et relations à distance $\leq R$)
- $[N_R(H, x)]$ : classe d'isomorphisme du voisinage
- $\kappa : \{\text{voisinages possibles}\} \to \mathbb{R}_+$ : **densité de coût** définie sur les types de voisinages

**Interprétation** :

Le coût est déterminé par les **patterns locaux** : chaque configuration locale $[N_R(H, x)]$ contribue un coût $\kappa([N_R(H, x)])$.

**Exemple** : Si $R = 1$, on considère les voisinages immédiats. Une entité isolée coûte $\kappa(\text{isolé})$, une entité liée à deux autres coûte $\kappa(\text{degré-2})$, etc.

**Avantages** : Capture la structure locale, permet de favoriser/pénaliser certains motifs.

**Paramètre** : Le rayon $R$ est un hyperparamètre du modèle. $R = 0$ correspond au cas (a). $R \to \infty$ prendrait en compte la structure globale (non local).

#### Option (c) : Complexité descriptive (option théorique)

$$K(H) \approx \text{longueur minimale d'une description de } [H]$$

**Interprétation** :

Le coût est la **complexité de Kolmogorov** : le nombre minimal de bits nécessaires pour encoder $H$ dans un langage fixé.

**Lien avec l'information** :

Cette approche identifie coût et **information** (au sens de Shannon-Kolmogorov). Une configuration complexe requiert plus de bits, donc a un coût plus élevé.

**Problème pratique** : La complexité de Kolmogorov est **non calculable** en général. Cette option est donc principalement conceptuelle.

**Avantage théorique** : Indépendante de la représentation choisie (invariance universelle).

---

### Choix du modèle

Le choix de $K$ fait partie des **données du modèle**, au même titre que le choix ultérieur des règles $\mathcal{R}$ (A1) et du paramètre $\beta$ (A3).

**Stratégie recommandée** :

1. Commencer par l'option (a) pour des études analytiques (simplicité)
2. Passer à l'option (b) pour des simulations numériques (réalisme)
3. Utiliser l'option (c) comme référence conceptuelle (universalité)

**Remarque fondamentale** : Le choix de $K$ influence la **mesure statistique** $\mu_\beta \propto e^{-\beta K}$ (A3) et donc les configurations les plus probables. C'est un degré de liberté essentiel du modèle.

---

## Résumé de la structure A0

```
A0 — SUBSTRAT COMBINATOIRE
│
├── Partie I : NOYAU ONTOLOGIQUE (5 principes)
│   ├── A0.α  Substrat relationnel     [existence]
│   ├── A0.β  Indiscernabilité         [relationalité]
│   ├── A0.γ  Vide                     [état fondamental]
│   ├── A0.δ  Potentialité             [ontologie modale]
│   └── A0.ε  Coût                     [proto-thermodynamique]
│
└── Partie II : CHOIX DE REPRÉSENTATION (4 conventions)
    ├── A0.1  Hypergraphes étiquetés   [structure de données]
    ├── A0.2  Convention minimale      [cas T = {⋆}]
    ├── A0.3  Isomorphisme             [réalisation de A0.β]
    └── A0.4  Forme de K               [réalisation de A0.ε]
```

**Ce qui est accompli** :

Nous avons défini un **cadre statique** : ce qu'est une configuration, comment on les compare, comment on mesure leur coût. Il manque encore :
- **La dynamique** : comment les configurations évoluent (A1)
- **La causalité** : comment ordonner les événements (A2)
- **Les histoires** : comment décrire les évolutions complètes (A3)

Passons à la dynamique.

---

# A1 — Règles locales de réécriture

**Le vide évolue par transformations locales compatibles avec sa structure**

---

## Partie I : Principes fondamentaux

### A1.α — Principe de transformation locale

> **Le substrat évolue uniquement par modifications locales.**

**Énoncé détaillé** :

Toute transformation du système :
1. Affecte un nombre **fini** d'entités et de relations
2. Laisse le **reste** de la configuration inchangé
3. Ne dépend que de la structure **locale** au voisinage de la modification

Il n'existe **pas** de transformation "globale" ou "à distance".

**Justification** :

Ce principe est analogue à la **localité en physique** : les interactions se produisent en un lieu, pas simultanément partout. C'est une condition de **causalité primitive**.

**Conséquence** :

Une transformation ne peut pas "savoir" ce qui se passe à distance arbitraire. Elle ne "voit" que son voisinage immédiat.

**Formalisation** (anticipée) :

Une règle de transformation sera spécifiée par :
- Un **motif local** $L$ (une petite configuration)
- Un **remplacement local** $R$ (une autre petite configuration)
- La règle dit : "Si tu trouves $L$ quelque part dans $H$, remplace-le par $R$"

**Exemple** :

Règle : "Deux entités liées par une relation se transforment en trois entités"
- Motif $L$ : $\{v_1, v_2\}$ liés par $e$
- Remplacement $R$ : $\{w_1, w_2, w_3\}$ avec nouvelles relations

Cette règle est **locale** : elle ne dépend pas du reste de la configuration.

---

### A1.β — Principe de reconnaissance de motif

> **Une transformation s'applique par reconnaissance d'un motif local.**

**Énoncé détaillé** :

Une transformation est déclenchée lorsqu'un certain **agencement local** (motif) est présent dans la configuration. L'application de la transformation :
1. Identifie une **occurrence** du motif dans la configuration
2. Remplace cette occurrence par un **autre motif**
3. Préserve l'**interface** avec le reste de la configuration

**Principe clé** : Il n'y a **pas** d'agent externe qui "décide" d'appliquer une règle. La **présence du motif suffit**.

**Justification** :

Ce principe élimine toute forme de **téléologie** ou d'**intentionnalité**. Les transformations ne sont pas "choisies" par un observateur externe, elles sont **intrinsèques** au système.

**Analogie** : Pensez aux réactions chimiques. Quand deux molécules compatibles se rencontrent, elles réagissent automatiquement. Pas besoin d'un "chimiste cosmique" pour décider si la réaction doit avoir lieu.

**Formalisation** :

Un motif $L$ est une petite configuration $(V_L, E_L, S_L, \tau_L, \sigma_L)$. Une **occurrence** de $L$ dans $H$ est un plongement (injection) $\iota : V_L \to V$ préservant la structure locale.

**Exemple** :

Motif : "Deux entités de type $\star$ liées par une relation de type $\star$"

Ce motif peut avoir plusieurs occurrences dans une grande configuration $H$. Chaque occurrence peut potentiellement être transformée.

**Question ouverte à ce stade** : Si plusieurs occurrences existent, laquelle est transformée ? Cette question sera résolue en A2 (structure causale) et A3 (exploration exhaustive).

---

### A1.γ — Principe de finitude des règles

> **L'ensemble des types de transformations possibles est fini.**

**Énoncé détaillé** :

Le système admet un **catalogue fini** $\mathcal{R}$ de règles de transformation. Ce catalogue est une **donnée du modèle**, non dérivée des autres axiomes.

**Clarification** :

- L'ensemble $\mathcal{R}$ est **fini** : $|\mathcal{R}| < \infty$
- Mais chaque règle $r \in \mathcal{R}$ peut avoir une **infinité d'occurrences** possibles

**Exemple** :

$\mathcal{R} = \{r_1, r_2, r_3\}$ avec trois règles :
- $r_1$ : "Créer une paire entité-relation"
- $r_2$ : "Fusionner deux entités voisines"
- $r_3$ : "Supprimer une relation isolée"

Ce catalogue contient 3 règles (fini), mais chaque règle peut s'appliquer en de nombreux endroits différents.

**Justification** :

Ce principe garantit que le système est **spécifiable de manière finie**. Si $\mathcal{R}$ était infini, il faudrait une description infinie pour définir le modèle (problème de complexité de Kolmogorov).

**Lien avec les lois de la physique** :

En physique, les "lois" (gravitation, électromagnétisme, etc.) forment un ensemble fini. Chaque loi peut s'appliquer en une infinité de situations, mais il n'y a qu'un nombre fini de lois fondamentales.

**Remarque** : Ce principe exclut des systèmes pathologiques avec une infinité de règles distinctes, mais n'exclut pas qu'une même règle produise une richesse infinie de comportements.

---

### A1.δ — Principe de localité bornée

> **Chaque règle affecte un voisinage de rayon fini.**

**Énoncé détaillé** :

Pour chaque règle $r \in \mathcal{R}$, il existe un rayon $R_r < \infty$ tel que :
1. La règle ne **lit** que des informations dans un voisinage de rayon $R_r$
2. La règle ne **modifie** que des éléments dans un voisinage de rayon $R_r$

**Définition du voisinage** :

Le voisinage de rayon $R$ autour d'un point (entité ou relation) $x$ est l'ensemble :
$$N_R(H, x) = \{y \in V \sqcup E : d_H(x, y) \leq R\}$$

où $d_H(x, y)$ est la distance dans le graphe d'incidence (nombre minimal de sauts entité-relation-entité).

**Exemple** :

Une règle avec $R_r = 1$ ne peut voir que :
- Une entité et ses relations immédiatement incidentes
- Une relation et ses entités immédiatement incidentes

Elle ne peut pas "savoir" ce qui se passe à deux sauts de distance.

**Justification** :

Ce principe formalise rigoureusement la **localité**. Il garantit que :
- Pas d'action instantanée à distance
- Les transformations sont **causalement locales**

**Lien avec la relativité** :

En relativité, la localité causale impose que les interactions se propagent à vitesse finie ($c$). Ici, au niveau pré-géométrique, la localité est **combinatoire** : une règle ne peut affecter qu'un voisinage fini dans le graphe.

**Conséquence** : Le rayon maximal $R_{\max} = \max_{r \in \mathcal{R}} R_r$ est une **échelle caractéristique** du système. C'est l'analogue d'une "longueur de Planck combinatoire".

---

### A1.ε — Principe de compatibilité avec le coût

> **Les règles respectent une cohérence avec la fonction de coût $K$.**

**Énoncé détaillé** :

Pour toute règle $r : L \to R$, il existe une fonction $\Delta K_r : \text{Contexte} \to \mathbb{R}$ qui mesure le **changement de coût** induit par l'application de $r$ :

$$\Delta K_r(\text{contexte}) = K(H') - K(H)$$

où $H'$ est la configuration après application de $r$ sur $H$.

**Propriété clé** : $\Delta K_r$ ne dépend que du **contexte local** (le voisinage de $L$ dans $H$), pas de la configuration globale.

**Justification** :

Ce principe garantit que le coût $K$ est **localement bien défini** : on peut calculer la variation de coût sans connaître la configuration entière.

**Cas particuliers** :

1. **Règles conservatives** : $\Delta K_r = 0$ (le coût est conservé)
   - Analogie : transformations unitaires en mécanique quantique
   
2. **Règles créatrices** : $\Delta K_r > 0$ (création de structure)
   - Analogie : paire création en physique des particules
   
3. **Règles destructrices** : $\Delta K_r < 0$ (annihilation de structure)
   - Analogie : annihilation matière-antimatière

**Lien avec A3** :

La variation de coût $\Delta K_r$ jouera un rôle crucial dans la mesure statistique :
$$\mu_\beta(H \to H') \propto e^{-\beta \Delta K_r}$$

Les transformations qui augmentent beaucoup le coût seront moins probables (pour $\beta > 0$).

**Remarque subtile** :

Ce principe **ne contraint pas** le signe de $\Delta K_r$. Il permet :
- La création de structure (univers en expansion)
- L'annihilation de structure (univers en contraction)
- La conservation de structure (univers stationnaire)

Le comportement effectif dépendra de la mesure $\mu_\beta$ (A3) et du principe S (Niveau II).

---

## Partie II : Formalisation mathématique

### A1.1 — Règles de réécriture (définition formelle)

**Définition** :

Une **règle de réécriture** est un quadruplet $r = (L, R, \iota_{\text{int}}, c)$ où :

1. **Motif gauche** $L = (V_L, E_L, S_L, \tau_L, \sigma_L)$ : configuration à reconnaître
2. **Motif droit** $R = (V_R, E_R, S_R, \tau_R, \sigma_R)$ : configuration de remplacement
3. **Interface** $\iota_{\text{int}} : V_{\text{int}} \to V_L \cap V_R$ : entités préservées
   - $V_{\text{int}}$ sont les entités "frontalières" qui connectent $L/R$ au reste de $H$
4. **Condition** $c : \text{Contexte} \to \{\text{vrai}, \text{faux}\}$ : prédicat optionnel

**Interprétation** :

- $L$ : "Si tu vois cette configuration..."
- $R$ : "...remplace-la par celle-ci"
- $\iota_{\text{int}}$ : "...en préservant ces entités d'interface"
- $c$ : "...mais seulement si cette condition est satisfaite"

**Catalogue de règles** :

L'ensemble $\mathcal{R} = \{r_1, r_2, \ldots, r_n\}$ est fini (A1.γ).

**Exemple concret** :

Règle de "paire-création" :
- $L = (\{v_0\}, \emptyset, \ldots)$ (un nœud isolé)
- $R = (\{v_1, v_2\}, \{e\}, S(e) = \{v_1, v_2\}, \ldots)$ (deux nœuds liés)
- $\iota_{\text{int}} = \emptyset$ (pas de préservation)
- $c = \text{vrai}$ (toujours applicable)

Cette règle remplace un nœud isolé par une paire de nœuds liés.

---

### A1.2 — Application d'une règle (occurrence et match)

**Match** :

Soit $H = (V, E, S, \tau, \sigma)$ une configuration et $r = (L, R, \iota_{\text{int}}, c)$ une règle.

Un **match** de $r$ dans $H$ est un plongement (injection) :
$$\mu : V_L \to V$$

préservant :
1. Les supports : $S(\mu(e_L)) = \mu[S_L(e_L)]$ pour tout $e_L \in E_L$
2. Les types : $\tau(\mu(e_L)) = \tau_L(e_L)$ et $\sigma(\mu(v_L)) = \sigma_L(v_L)$
3. La condition : $c(\text{contexte}(\mu)) = \text{vrai}$

**Contexte** :

Le contexte d'un match $\mu$ est le voisinage de rayon $R_r$ autour de $\mu[V_L]$ dans $H$.

**Application** :

Appliquer la règle $r$ selon le match $\mu$ produit une nouvelle configuration $H'$ où :
1. Les éléments de $L$ (image de $\mu$) sont **retirés** de $H$
2. Les éléments de $R$ sont **insérés** à leur place
3. Les connexions via $\iota_{\text{int}}$ sont **préservées**

**Notation** :

On écrit $H \xrightarrow{r, \mu} H'$ pour indiquer que $H'$ est obtenue en appliquant $r$ via le match $\mu$ sur $H$.

**Ensemble des successeurs** :

Pour une configuration $H$ et une règle $r$, l'ensemble des configurations successeurs est :
$$\text{Succ}_r(H) = \{H' : \exists \mu, H \xrightarrow{r, \mu} H'\}$$

L'ensemble total des successeurs (toutes règles) est :
$$\text{Succ}(H) = \bigcup_{r \in \mathcal{R}} \text{Succ}_r(H)$$

---

### A1.3 — Propriétés des règles

#### Rayon d'action

Le **rayon** d'une règle $r$ est :
$$R_r = \max\left(\text{diam}(L), \text{diam}(R)\right)$$

où $\text{diam}(X)$ est le diamètre de la configuration $X$ (distance maximale entre deux éléments).

Le rayon maximal est :
$$R_{\max} = \max_{r \in \mathcal{R}} R_r < \infty$$

#### Variation de coût

Pour une règle $r$ et un match $\mu$ dans $H$, la variation de coût est :
$$\Delta K_{r,\mu}(H) = K(H') - K(H)$$

où $H \xrightarrow{r, \mu} H'$.

**Propriété de localité** : $\Delta K_{r,\mu}$ ne dépend que de $N_{R_{\max}}(H, \mu[V_L])$.

#### Classification des règles

On peut classer les règles selon leur effet sur le coût :

| Type | Propriété | Exemple |
|------|-----------|---------|
| **Conservative** | $\Delta K = 0$ toujours | Rotation d'une paire |
| **Créatrice** | $\Delta K > 0$ toujours | Paire-création |
| **Destructrice** | $\Delta K < 0$ toujours | Annihilation |
| **Mixte** | $\Delta K$ dépend du contexte | Fusion conditionnelle |

---

### A1.4 — Espace de configurations accessibles

**Définition** :

Soit $H_0$ une configuration initiale. L'espace des configurations **accessibles** depuis $H_0$ est :
$$C(H_0, \mathcal{R}) = \{H : \exists \text{ séquence } H_0 \xrightarrow{r_1} H_1 \xrightarrow{r_2} \cdots \xrightarrow{r_n} H\}$$

**Propriétés** :

1. **Fermeture** : Si $H \in C(H_0, \mathcal{R})$ alors $\text{Succ}(H) \subseteq C(H_0, \mathcal{R})$
2. **Connexité** : $C(H_0, \mathcal{R})$ forme un graphe dirigé où $H \to H'$ si $H' \in \text{Succ}(H)$

**Questions fondamentales** :

1. $C(H_0, \mathcal{R})$ est-il **fini** ou **infini** ?
2. Toute configuration dans $C$ est-elle **accessible** depuis toute autre ?
3. Existe-t-il des **configurations absorbantes** (sans successeurs) ?

Ces questions dépendent crucialement du choix de $\mathcal{R}$.

**Exemple** :

Si $\mathcal{R}$ contient uniquement des règles créatrices, alors $|C(H_0, \mathcal{R})| = \infty$ (expansion infinie).

Si $\mathcal{R}$ contient uniquement des règles destructrices, alors $C(H_0, \mathcal{R})$ est fini et contient $\varnothing$ comme état absorbant.

---

## Résumé A1

**Ce qui est accompli** :

Nous avons défini :
1. **Les principes** de transformation locale (Partie I)
2. **Les règles** formelles de réécriture (Partie II)
3. **L'espace** des configurations accessibles

**Ce qui manque** :

- **L'ordre temporel** : si $H \to H'$ et $H \to H''$, quel événement se produit "avant" ?
- **La résolution des conflits** : si plusieurs règles sont applicables, laquelle s'applique ?

Ces questions seront résolues en A2 (structure causale) et A3 (exploration exhaustive).

---

# A2 — Structure causale locale

**Les transformations génèrent un ordre de précédence causale**

---

## Partie I : Principes de causalité

### A2.α — Principe de précédence locale

> **Les événements locaux génèrent un ordre partiel de précédence.**

**Énoncé détaillé** :

Lorsque deux transformations locales $e_1$ et $e_2$ sont appliquées, il existe une relation de **précédence** $e_1 \prec e_2$ si :
- $e_2$ **lit** des informations **écrites** par $e_1$, ou
- $e_2$ **modifie** des éléments **créés** par $e_1$

La relation $\prec$ est un **ordre partiel** : réflexif, transitif, antisymétrique.

**Justification** :

Ce principe capture l'idée intuitive de **causalité** : un événement peut influencer un autre seulement si :
1. Il se produit "avant" (précédence temporelle)
2. Ils partagent un élément commun (proximité spatiale)

**Différence avec l'ordre total** :

Contrairement au temps newtonien (ordre total), ici deux événements peuvent être **incomparables** : $e_1 \not\prec e_2$ et $e_2 \not\prec e_1$. Cela signifie qu'ils sont **causalement indépendants** (type espace en relativité).

**Formalisation** (anticipée) :

On dira que $e_1 \prec e_2$ si :
$$\text{Write}(e_1) \cap \text{Read}(e_2) \neq \emptyset$$

où :
- $\text{Write}(e)$ : ensemble des éléments créés/modifiés par $e$
- $\text{Read}(e)$ : ensemble des éléments lus par $e$

---

### A2.β — Principe de compatibilité causale

> **Deux événements incompatibles ne peuvent pas se produire simultanément.**

**Énoncé détaillé** :

Deux événements $e_1, e_2$ sont **en conflit** si :
$$\text{Write}(e_1) \cap \text{Write}(e_2) \neq \emptyset$$

(ils veulent modifier les mêmes éléments).

Dans ce cas, **au plus un** des deux peut se produire.

**Justification** :

Ce principe garantit la **cohérence** : on ne peut pas modifier simultanément le même objet de deux façons incompatibles.

**Analogie informatique** :

C'est l'analogue du problème de **concurrence** en programmation parallèle : deux threads ne peuvent pas écrire simultanément dans la même variable.

**Résolution** :

La résolution des conflits sera traitée en A3 : l'espace $\Omega$ contient toutes les résolutions possibles (toutes les histoires compatibles).

**Exemple** :

Soient deux règles applicables sur la même entité $v$ :
- $e_1$ : supprimer $v$
- $e_2$ : ajouter une relation incidente à $v$

Ces événements sont en conflit (ils modifient tous deux $v$). Deux histoires sont possibles :
1. $e_1$ se produit (suppression), puis $e_2$ devient inapplicable
2. $e_2$ se produit (ajout), puis $e_1$ supprime $v$ avec sa nouvelle relation

---

### A2.γ — Principe de non-circularité

> **L'ordre de précédence ne contient pas de cycles.**

**Énoncé détaillé** :

Il n'existe **pas** de suite d'événements $e_1 \prec e_2 \prec \cdots \prec e_n \prec e_1$.

**Justification** :

Les boucles causales ("je suis mon propre ancêtre") sont exclues. C'est une condition de **cohérence logique** minimale.

**Conséquence** :

L'ordre $\prec$ est un **ordre partiel acyclique**, c'est-à-dire un **DAG** (directed acyclic graph) dans le graphe des événements.

**Lien avec le temps** :

Ce principe garantit l'existence d'une **notion de temps** (au moins partielle) : on peut dire "avant" et "après" de manière cohérente.

**Remarque** : Dans certains modèles de gravité quantique (boucles causales en relativité générale), ce principe pourrait être relaxé. Ici, nous l'imposons comme axiome.

---

### A2.δ — Principe de propagation causale

> **L'influence causale se propage localement, pas instantanément.**

**Énoncé détaillé** :

Si deux événements $e_1, e_2$ vérifient $e_1 \prec e_2$, alors il existe une **chaîne** d'événements intermédiaires :
$$e_1 = e'_0 \prec e'_1 \prec \cdots \prec e'_k = e_2$$

où chaque $e'_i \prec e'_{i+1}$ est une précédence **immédiate** (distance combinatoire finie).

**Justification** :

L'influence causale ne "saute" pas arbitrairement loin. Elle se propage de proche en proche.

**Conséquence** :

La structure $\prec$ est la **clôture transitive** des précédences immédiates. On peut reconstruire $\prec$ à partir de l'information locale.

**Lien avec la vitesse de la lumière** :

En relativité, la causalité se propage à vitesse $c$. Ici, au niveau combinatoire, la propagation se fait "saut par saut" dans le graphe.

**Échelle causale** :

La longueur typique d'une chaîne causale sera reliée à une notion de "distance causale" qui, dans la limite continue, deviendra la métrique d'espace-temps.

---

## Partie II : Propriétés et conséquences

### A2.1 — Événements élémentaires

**Définition formelle** :

Un **événement élémentaire** est un quadruplet :
$$e = (H, r, \mu, H')$$

où :
- $H$ : configuration avant l'événement
- $r \in \mathcal{R}$ : règle appliquée
- $\mu$ : match de $r$ dans $H$
- $H'$ : configuration après l'événement ($H \xrightarrow{r, \mu} H'$)

**Interprétation** :

Un événement est une **transformation instantanée** : $H$ disparaît, $H'$ apparaît.

---

#### Ensembles Read/Write (version complète)

Soit une règle de réécriture $r : L \Rightarrow R$ avec une **interface** (partie conservée) :
$$I = L \cap R.$$

Sous un match $\mu$, on note :
- $L_\mu \subset H$ : occurrence (image) du motif gauche dans $H$,
- $I_\mu \subset L_\mu$ : partie conservée,
- $C_\mu \subset H$ : **contexte local lu** (voisinage requis par l’applicabilité, le rayon $R_r$ et/ou le calcul local du coût).

On définit :

- **Lecture** (tout ce qui conditionne l’événement) :
$$\mathrm{Read}(e) \;=\; L_\mu \,\cup\, C_\mu.$$

- **Écriture** (tout ce qui est effectivement modifié dans la transition) :
$$\mathrm{Write}(e) \;=\; \mathrm{Del}(e)\,\cup\,\mathrm{Mod}(e)\,\cup\,\mathrm{New}(e),$$
où :
- $\mathrm{Del}(e)= L_\mu \setminus I_\mu$ (éléments supprimés),
- $\mathrm{Mod}(e)\subseteq I_\mu$ (éléments conservés mais dont attributs/relations/incidences changent),
- $\mathrm{New}(e)= R\setminus I$ (éléments créés, vus comme “nouveaux identifiants” dans $H'$).

> Remarque : si tes règles ne modifient jamais l’interface, alors $\mathrm{Mod}(e)=\emptyset$.

**Exemple (paire-création)** :

- $\mathrm{Read}(e)$ contient le motif consommé (et éventuellement son voisinage requis)
- $\mathrm{Write}(e)$ contient les éléments supprimés, plus tous les nouveaux éléments créés


### A2.2 — Ordre de précédence

Pour éviter d’imposer (à tort) la transitivité directement sur une dépendance locale, on distingue :

1) une **dépendance immédiate** entre événements ;  
2) l’**ordre causal** comme fermeture transitive.

---

#### (i) Dépendance immédiate

Soient $e_1$ et $e_2$ deux événements. On définit :
$$e_1 \to e_2 \quad \Longleftrightarrow \quad \mathrm{Write}(e_1)\cap \mathrm{Read}(e_2)\neq \emptyset.$$

**Interprétation** : $e_2$ dépend directement d’une information que $e_1$ a modifiée/créée/supprimée.

---

#### (ii) Précédence causale (ordre)

On définit la précédence causale comme la **clôture transitive** de $\to$ :
$$e_1 \prec e_2 \quad \Longleftrightarrow \quad \exists k\ge 1,\ \exists (f_0,\dots,f_k)\ :\ f_0=e_1,\ f_k=e_2,\ \forall i,\ f_i\to f_{i+1}.$$

**Propriétés** :

- $\prec$ est un **ordre partiel strict** (irréflexif et transitif).
- L’absence de cycles est garantie par A2.γ (non-circularité).

**Option** (souvent pratique) : fermeture réflexive
$$e_1 \preceq e_2 \;\Longleftrightarrow\; (e_1 \prec e_2)\ \text{ou}\ (e_1=e_2),$$
qui est alors un ordre partiel (réflexif, antisymétrique, transitif).

---

#### Graphe causal

Le **graphe causal** $G_c$ est le graphe orienté dont les sommets sont les événements et dont les arêtes sont les dépendances immédiates $\to$. La relation $\prec$ correspond alors aux chemins orientés de $G_c$.


### A2.3 — Conflits et indépendance

**Conflit** :

Deux événements $e_1, e_2$ sont **en conflit** (noté $e_1 \smile e_2$) si :
$$\mathrm{Write}(e_1)\cap \mathrm{Write}(e_2)\neq \emptyset.$$

**Interprétation** : ils tentent de modifier (ou créer/supprimer) des éléments qui se chevauchent.

---

**Indépendance causale (concurrence)** :

Deux événements $e_1, e_2$ sont **causalement indépendants** si :
$$\mathrm{Write}(e_1)\cap \mathrm{Read}(e_2)=\emptyset,\quad
\mathrm{Write}(e_2)\cap \mathrm{Read}(e_1)=\emptyset,\quad
\mathrm{Write}(e_1)\cap \mathrm{Write}(e_2)=\emptyset.$$

On note alors $e_1 \parallel e_2$.

**Conséquence (commutation)** :

Si $e_1 \parallel e_2$ et que les deux sont applicables sur la même configuration $H$, alors appliquer $e_1$ puis $e_2$ ou $e_2$ puis $e_1$ conduit à des configurations **isomorphes** (même classe $[H]$).


### A2.4 — Diagramme de Hasse

**Représentation** :

Soit $\omega = (e_1, e_2, \ldots, e_n, \ldots)$ une séquence d'événements. L'ordre $\prec_\omega$ induit sur ces événements peut être visualisé comme un **diagramme de Hasse** :
- Nœuds : événements $e_i$
- Arêtes : $e_i \to e_j$ si $e_i \prec e_j$ immédiatement

**Structure** :

Pour une histoire causalement cohérente, ce diagramme est un **DAG** (A2.γ).

**Couches causales** :

On peut définir des **niveaux causaux** :
- Niveau 0 : événements initiaux (pas de prédécesseur)
- Niveau $n+1$ : événements dont tous les prédécesseurs sont au niveau $\leq n$

Ces niveaux forment une **foliation causale** de l'histoire.

---

### A2.5 — Propagation de l'information

**Cône causal passé** :

Pour un événement $e$, le **passé causal** est :
$$\text{Past}(e) = \{e' : e' \prec e\}$$

Ce sont tous les événements qui peuvent avoir influencé $e$.

**Cône causal futur** :

Le **futur causal** est :
$$\text{Future}(e) = \{e' : e \prec e'\}$$

Ce sont tous les événements que $e$ peut influencer.

**Indépendance** :

Si $e' \notin \text{Past}(e) \cup \text{Future}(e)$, alors $e$ et $e'$ sont **causalement déconnectés**.

**Lien avec la relativité** :

Ces cônes sont l'analogue combinatoire des **cônes de lumière** en relativité. Dans la limite continue :
$$\text{Past}(e) \to \{x : x \in J^-(e)\} \quad \text{(cône passé)}$$

---

## Résumé A2

**Ce qui est accompli** :

Nous avons défini :
1. **L'ordre partiel** $\prec$ (précédence causale)
2. **Les conflits** $\smile$ (incompatibilité)
3. **Les cônes causaux** (propagation de l'information)

**Propriétés clés** :

- $\prec$ est un ordre partiel acyclique (DAG)
- Deux événements peuvent être causalement indépendants
- La causalité se propage localement (pas d'action à distance)

**Ce qui reste** :

Comment passer d'un ordre partiel $\prec$ à une **mesure sur les histoires** $\mu_\beta$ ? C'est l'objet de A3.

---

# A3 — Espace des histoires

**Le vide est l'ensemble de toutes les évolutions possibles**

---

## Partie I : Construction de Ω

### A3.α — Définition de l'espace des histoires

**Histoire** :

Une **histoire** (ou évolution) est une séquence (finie ou infinie) d'événements :
$$\omega = (e_1, e_2, e_3, \ldots)$$

satisfaisant les contraintes causales (A2).

**Espace $\Omega$** :

L'espace des histoires est :
$$\Omega = \Omega(H_0, \mathcal{R}) = \{\omega : \omega \text{ compatible avec } (H_0, \mathcal{R}, \prec)\}$$

où :
- $H_0$ : configuration initiale (peut être $\varnothing$)
- $\mathcal{R}$ : catalogue de règles
- $\prec$ : ordre de précédence (A2)

**Compatibilité** :

Une histoire $\omega$ est **compatible** si :
1. Chaque événement $e_i$ applique une règle $r \in \mathcal{R}$
2. L'ordre des événements respecte $\prec$ (pas de violation de causalité)
3. Pas de conflits non résolus (si $e_i \smile e_j$, au plus un se produit)

**Réalisation de A0.δ** :

Ce principe réalise formellement l'idée que "le vide est Ω, pas ∅" :
$$\text{Vide pré-géométrique} = \Omega$$

Le vide n'est pas une configuration particulière, mais **toutes les histoires possibles**.

---

### A3.β — Ordre partiel sur Ω

**Ordre de continuation** :

Sur $\Omega$, on définit un ordre partiel $\omega \sqsubseteq \omega'$ si :
$$\omega \text{ est un préfixe de } \omega'$$

C'est-à-dire : $\omega'$ est une **continuation** de $\omega$.

**Interprétation** :

$\omega \sqsubseteq \omega'$ signifie que $\omega'$ "contient plus d'événements" que $\omega$. C'est une évolution plus longue.

**Structure** :

$(\Omega, \sqsubseteq)$ forme un **ensemble partiellement ordonné** (poset).

**Branches** :

Les **histoires maximales** (non prolongeables) forment les "branches" de l'arbre des possibilités.

**Exemples de branches** :

1. **Histoire infinie** : $\omega = (e_1, e_2, e_3, \ldots)$ prolongeable indéfiniment
2. **Histoire bloquée** : $\omega$ atteint une configuration $H$ sans successeur (état absorbant)

---

### A3.γ — Filtration et $\sigma$-algèbre

**Filtration** :

Pour chaque "temps" $n$, on définit :
$$\mathcal{F}_n = \sigma(\{e_1, e_2, \ldots, e_n\})$$

l'information disponible après $n$ événements.

**Propriété** :

$\mathcal{F}_1 \subseteq \mathcal{F}_2 \subseteq \cdots$ (croissance de l'information).

**$\sigma$-algèbre complète** :

$$\mathcal{F}_\infty = \sigma\left(\bigcup_{n=1}^\infty \mathcal{F}_n\right)$$

**Utilité** :

Cette structure permet de définir rigoureusement une **mesure de probabilité** sur $\Omega$ (Partie II).

---

### A3.δ — Configurations accessibles et graphe des états

**Graphe des configurations** :

Soit $\mathcal{G} = (C, E)$ où :
- $C = C(H_0, \mathcal{R})$ : configurations accessibles
- $E = \{(H, H') : \exists r \in \mathcal{R}, H \xrightarrow{r} H'\}$ : transitions

**Chemins** :

Une histoire $\omega \in \Omega$ correspond à un **chemin** dans $\mathcal{G}$.

**Propriétés** :

1. **Connexité** : Dépend de $\mathcal{R}$. Si $\mathcal{R}$ permet d'explorer toutes les configurations, $\mathcal{G}$ est fortement connexe.
2. **Diamètre** : Distance maximale entre deux configurations. Peut être infini.
3. **Cycles** : $\mathcal{G}$ peut contenir des cycles (retour à une configuration précédente).

**Exemple de cycle** :

Si $\mathcal{R}$ contient deux règles :
- $r_1 : H_1 \to H_2$
- $r_2 : H_2 \to H_1$

Alors $\mathcal{G}$ contient un cycle $H_1 \leftrightarrow H_2$.

---

## Partie II : Mesure statistique

### A3.1 — Mesure de Boltzmann (introduction du paramètre $\beta$)

**Principe de Boltzmann** :

Dans un système en équilibre thermodynamique, la probabilité d'un état d'énergie $E$ est :
$$p(E) \propto e^{-\beta E}$$
où $\beta = 1/(k_B T)$ est l'inverse de la température.

---

**Adaptation au cadre combinatoire** :

Ici, l'énergie est remplacée par le **coût** $K$ (A0.ε). Une mesure naturelle sur les configurations est :
$$\mu_\beta([H]) \propto e^{-\beta K(H)}.$$

---

#### Régularisation (cutoff de complexité)

Comme l’espace $\mathcal{C}$ peut être infini, on introduit un budget $\Lambda$ et :
$$\mathcal{C}_\Lambda=\{[H]\in\mathcal{C}\ :\ K(H)\le \Lambda\}.$$

On définit alors :
$$Z_{\beta,\Lambda}=\sum_{[H]\in\mathcal{C}_\Lambda} e^{-\beta K(H)},\qquad
\mu_{\beta,\Lambda}([H])=\frac{e^{-\beta K(H)}}{Z_{\beta,\Lambda}} \ \ \ ([H]\in\mathcal{C}_\Lambda).$$

La limite $\Lambda\to\infty$ (si elle existe, au sens de convergence faible sur cylindres) définit une mesure non régularisée ; sinon, la théorie se formule naturellement “à cutoff” ou via des spécifications locales (type Gibbs/DLR) au niveau II.

---

**Cas limites** :

1. **$\beta \to 0$** (température infinie) : tendance vers une mesure plus “entropique” sur $\mathcal{C}_\Lambda$.
2. **$\beta \to \infty$** (température nulle) : concentration sur les configurations de coût minimal (à cutoff fixé).
3. **$\beta = 1$** : choix possible d’échelle, mais non imposé à ce stade.


### A3.2 — Mesure sur les histoires

On construit une mesure sur l’espace des histoires $\Omega$ à partir d’un **noyau local de transition** (ce qui évite de confondre “pondération ontologique” et “processus parcouru”).

---

#### (i) Événements activables depuis une configuration

Soit $H$ une configuration. On note :
$$\mathbb{E}(H)=\{(r,\mu)\ :\ r\in\mathcal{R}\ \text{et}\ \mu\ \text{est un match valide de}\ r\ \text{dans}\ H\}.$$

Chaque $(r,\mu)\in\mathbb{E}(H)$ définit un événement $e=(H,r,\mu,H')$.

---

#### (ii) Poids et probabilité de transition (cas markovien)

On associe à chaque événement un poids local :
$$w_\beta(e\mid H)=\exp\!\big(-\beta\,\Delta K(e;H)\big),$$
où $\Delta K(e;H)=K(H')-K(H)$ (ou une approximation locale compatible avec A1.ε).

La probabilité de choisir $e$ depuis $H$ est :
$$P_\beta(e\mid H)=\frac{w_\beta(e\mid H)}{\sum\limits_{e'\in \mathbb{E}(H)} w_\beta(e'\mid H)}.$$

---

#### (iii) Mesure sur les cylindres (histoires finies)

Pour un préfixe $\omega_{1:n}=(e_1,\dots,e_n)$ induisant la chaîne :
$$H_0 \xrightarrow{e_1} H_1 \xrightarrow{e_2} \cdots \xrightarrow{e_n} H_n,$$
on définit :
$$\mu_{\beta,\Lambda}(\omega_{1:n})
=\mu_{\beta,\Lambda}([H_0])\cdot \prod_{i=1}^{n} P_\beta(e_i\mid H_{i-1}).$$

Les cylindres engendrent une filtration $(\mathcal{F}_n)_{n\ge 0}$.

Si les compatibilités de marges sont satisfaites, le théorème d’extension de Kolmogorov permet d’étendre $\mu_{\beta,\Lambda}$ à une mesure sur $(\Omega,\mathcal{F}_\infty)$.

---

#### (iv) Invariance par isomorphisme

Pour toute bijection d’isomorphisme $\varphi$ (relabeling) compatible avec la structure :
$$\mu_{\beta,\Lambda}(\omega)=\mu_{\beta,\Lambda}(\varphi(\omega)).$$

---

#### (v) Statut de l’ergodicité

L’ergodicité peut être posée comme **hypothèse** (ou conjecture) pour certains choix de $(\mathcal{R},K,\beta)$, afin de relier typicalité et moyennes “sur histoires” au niveau II.


### A3.3 — Propriétés de la mesure $\mu_\beta$

**Normalisation** :

Si $\Omega$ est dénombrable :
$$\sum_{\omega \in \Omega} \mu_\beta(\omega) = 1$$

Si $\Omega$ est non dénombrable (continuum d'histoires), $\mu_\beta$ est une mesure $\sigma$-additive sur $\mathcal{F}_\infty$.

**Invariance par permutation** :

$$\mu_\beta(\omega) = \mu_\beta(\pi(\omega))$$

si $\pi$ est une permutation respectant la structure (A0.β).

**Ergodicité (conjecture)** :

Pour certains choix de $\mathcal{R}$ et $\beta$, la mesure $\mu_\beta$ pourrait être **ergodique** : presque toute histoire visite toute région de $\mathcal{C}$ avec une fréquence proportionnelle à $\mu_\beta$.

Cette propriété sera cruciale pour définir des **moyennes temporelles** (Niveau I.B).

---

### A3.4 — Lien avec la thermodynamique statistique

**Énergie libre** :

On définit l'**énergie libre** de Helmholtz :
$$F_\beta = -\beta^{-1} \ln Z_\beta$$

**Entropie** :

L'**entropie de Shannon** est :
$$S = -\sum_{[H]} \mu_\beta([H]) \ln \mu_\beta([H])$$

**Relation thermodynamique** :

$$F_\beta = \langle K \rangle_\beta - \beta^{-1} S$$

où $\langle K \rangle_\beta = \sum_{[H]} \mu_\beta([H]) K(H)$ est le coût moyen.

**Interprétation** :

La mesure $\mu_\beta$ réalise un **compromis** entre :
1. **Minimiser le coût** $K$ (ordre)
2. **Maximiser l'entropie** $S$ (désordre)

Le paramètre $\beta$ contrôle ce compromis.

---

### A3.5 — Statut du paramètre $\beta$

**Nature de $\beta$** :

Le paramètre $\beta$ est un **hyperparamètre** du modèle. Il n'est **pas** dérivé des axiomes A0-A2.

**Questions ouvertes** :

1. **Universalité** : Existe-t-il une valeur "naturelle" $\beta^* = 1$ (température de Planck combinatoire) ?
2. **Sélection** : Le principe S (Niveau II) pourrait-il sélectionner $\beta$ ?
3. **Évolution** : $\beta$ pourrait-il varier avec le temps émergent (refroidissement cosmologique) ?

**Lien avec la température physique** :

Dans la limite continue, $\beta$ sera relié à la température physique via :
$$\beta = \frac{1}{k_B T}$$

où $k_B$ est la constante de Boltzmann (à définir dans le cadre émergent).

---

### A3.6 — Mesure uniforme (cas $\beta = 0$)

**Définition** :

Pour $\beta = 0$, la mesure devient **uniforme** sur $\mathcal{C}$ :
$$\mu_0([H]) = \frac{1}{|C(H_0, \mathcal{R})|}$$

si $C$ est fini, ou :
$$\mu_0 = \text{mesure de comptage}$$

si $C$ est dénombrable.

**Interprétation** :

Toutes les configurations sont équiprobables. C'est le cas de **maximale ignorance** (principe d'indifférence de Laplace).

**Avantage** : Simplicité conceptuelle.

**Inconvénient** : Ne favorise aucune structure. Peu probable de produire des univers organisés.

---

### A3.7 — Exploration exhaustive

**Principe d'exploration** :

Le vide "explore" toutes les histoires compatibles. Formellement :
$$\Omega = \{\omega : \omega \text{ compatible}\}$$

Aucune histoire compatible n'est **exclue a priori**.

**Conséquence** :

Si $\mu_\beta(\omega) > 0$ pour toute histoire compatible $\omega$, alors le système "visite" effectivement tout $\Omega$.

**Lien avec le multivers** :

Cette interprétation suggère une forme de **multivers** : toutes les histoires possibles "existent" avec des poids $\mu_\beta$.

**Sélection observationnelle** :

Au Niveau II, le principe S sélectionnera un sous-ensemble de $\Omega$ correspondant aux univers **stables** et **observables**.

---

## Résumé A3

**Ce qui est accompli** :

Nous avons construit :
1. **L'espace $\Omega$** de toutes les histoires possibles
2. **L'ordre partiel** $\sqsubseteq$ (continuation)
3. **La mesure $\mu_\beta$** (statistique de Boltzmann)

**Paramètres du modèle** :

- $H_0$ : configuration initiale (souvent $\varnothing$)
- $\mathcal{R}$ : catalogue de règles (choix physique)
- $K$ : fonction de coût (choix A0.4)
- $\beta$ : température inverse (hyperparamètre)

**Transition vers Niveau I.B** :

La mesure $\mu_\beta$ permettra de définir :
- **Fréquences temporelles** (moyenne sur histoires)
- **Observables macroscopiques** (moyennes statistiques)
- **Émergence** (propriétés asymptotiques)

Ces concepts seront développés au Niveau I.B.

---

# Récapitulatif et notations

## Architecture des axiomes

```
NIVEAU I.A — AXIOMES FONDAMENTAUX
│
├── A0 — SUBSTRAT COMBINATOIRE
│   ├── Partie I : Noyau ontologique (α-ε)
│   └── Partie II : Représentation (1-4)
│
├── A1 — RÈGLES LOCALES
│   ├── Partie I : Principes (α-ε)
│   └── Partie II : Formalisation (1-4)
│
├── A2 — STRUCTURE CAUSALE
│   ├── Partie I : Principes (α-δ)
│   └── Partie II : Propriétés (1-5)
│
└── A3 — ESPACE DES HISTOIRES
    ├── Partie I : Construction de Ω (α-δ)
    └── Partie II : Mesure μ_β (1-7)
```

## Notations principales

| Notation | Signification |
|----------|---------------|
| $H = (V, E, S, \tau, \sigma)$ | Configuration (hypergraphe étiqueté) |
| $[H]$ | Classe d'isomorphisme de $H$ |
| $\mathcal{C}$ | Espace des classes d'isomorphisme |
| $K(H)$ | Coût combinatoire de $H$ |
| $\varnothing$ | Configuration vide |
| $\mathcal{R} = \{r_1, \ldots, r_n\}$ | Catalogue de règles |
| $r = (L, R, \iota_{\text{int}}, c)$ | Règle de réécriture |
| $H \xrightarrow{r, \mu} H'$ | Application de règle |
| $C(H_0, \mathcal{R})$ | Configurations accessibles |
| $e = (H, r, \mu, H')$ | Événement élémentaire |
| $\text{Read}(e), \text{Write}(e)$ | Lecture/écriture |
| $e_1 \prec e_2$ | Précédence causale |
| $e_1 \smile e_2$ | Conflit |
| $\omega = (e_1, e_2, \ldots)$ | Histoire |
| $\Omega = \Omega(H_0, \mathcal{R})$ | Espace des histoires |
| $\mu_\beta$ | Mesure de Boltzmann |
| $Z_\beta$ | Fonction de partition |
| $\beta$ | Température inverse |

## Concepts clés

**Minimalisme ontologique** :
- Seule la structure relationnelle existe (A0.α-β)
- Les entités n'ont pas d'identité intrinsèque
- Le vide est potentialité, pas néant (A0.δ)

**Localité** :
- Transformations locales uniquement (A1.α, A1.δ)
- Causalité locale (A2.δ)
- Pas d'action instantanée à distance

**Exploration exhaustive** :
- Toutes les histoires compatibles existent dans $\Omega$ (A3.α)
- Mesure $\mu_\beta$ donne des poids statistiques (A3.2)

**Émergence** (à développer en I.B-C) :
- Types émergents depuis fréquences
- Observables macroscopiques depuis moyennes
- Structure géométrique depuis connectivité

## Propriétés attendues (conjectures)

1. **Réversibilité** : Pour certains $\mathcal{R}$, $K$ est conservé (univers réversibles)
2. **Ergodicité** : Pour certains $\beta$, $\mu_\beta$ est ergodique
3. **Phases** : Il existe des régimes distincts (géométrique, informationnel, etc.)
4. **Dimension** : La dimension spectrale émerge comme propriété statistique

Ces conjectures seront explorées aux Niveaux I.B-D et II.

---

## Vers le Niveau I.B

**Ce qui est accompli** :

Nous disposons d'un **cadre axiomatique complet** pour définir :
- Les configurations et leurs transformations
- L'ordre causal
- L'espace des histoires
- Une mesure statistique

**Ce qui reste** (Niveau I.B) :

1. **Fréquences temporelles** : Comment mesurer l'activité d'une hyperarête/règle le long d'une histoire ?
2. **Classes fréquentielles** : Comment classifier les entités selon leur comportement dynamique ?
3. **Mesure stationnaire** : Lien rigoureux entre $\mu_\beta$ et les moyennes temporelles

Ces concepts nécessitent les **compteurs Read/Write** et une théorie des **fréquences** que nous développerons en I.B.

---

## Statut épistémologique

**Ce document constitue** :
- Un **cadre théorique** complet et cohérent
- Un ensemble d'**axiomes minimaux** (A0-A3)
- Une **stratégie de représentation** (hypergraphes)

**Ce document ne constitue pas** :
- Un modèle physique calibré (pas de $\mathcal{R}$ spécifique)
- Une théorie finale (développements en I.B-D, II-III nécessaires)
- Une dérivation ab initio de la physique connue (sélection par principe S au niveau II)

**Analogie** :

Ce niveau est à la physique complète ce que la géométrie différentielle est à la relativité générale : un **langage mathématique** dans lequel la théorie physique peut être formulée, mais pas encore la théorie elle-même.

---

**Document préparé le 21 décembre 2024**

**Prochaine étape** : Niveau I.B — Dynamique et fréquences (compteurs Read/Write, fréquences temporelles, mesure stationnaire)
