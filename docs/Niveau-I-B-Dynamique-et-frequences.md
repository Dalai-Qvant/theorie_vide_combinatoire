# Niveau I.B — Dynamique et fréquences

### **Du vide statique au vide dynamique : mesurer l’activité sans temps externe**

---

## Table des matières

- [Introduction](#introduction)
- [B0 — Rappels et fondements](#b0--rappels-et-fondements)
- [B1 — Compteurs locaux (Read/Write)](#b1--compteurs-locaux-readwrite)
- [B2 — Fréquences temporelles](#b2--fréquences-temporelles)
- [B3 — Classes fréquentielles (types émergents)](#b3--classes-fréquentielles-types-émergents)
- [B4 — Moyenne temporelle et vide statistique](#b4--moyenne-temporelle-et-vide-statistique)
- [B5 — Mesure stationnaire, ergodicité et pratique (cutoff)](#b5--mesure-stationnaire-ergodicité-et-pratique-cutoff)
- [Récapitulatif](#récapitulatif)

---

## Notations principales (ajouts de I.B)

| Notation | Signification |
|----------|---------------|
| $n^{\mathrm{read}}_x(\omega,k)$ | Compteur de lecture de $x$ après $k$ événements |
| $n^{\mathrm{write}}_x(\omega,k)$ | Compteur d'écriture de $x$ après $k$ événements |
| $\tau_x(\omega,k)$ | Temps local (interactions) de $x$ |
| $f_x^{\mathrm{read}}(\omega)$ | Fréquence globale de lecture (si elle existe) |
| $f_x^{\mathrm{write}}(\omega)$ | Fréquence globale d'écriture (si elle existe) |
| $\tilde f_x^{\mathrm{read}}(\omega)$ | Fréquence conditionnelle (sur la vie) de lecture |
| $\tilde f_x^{\mathrm{write}}(\omega)$ | Fréquence conditionnelle (sur la vie) d'écriture |
| $f_r(\omega)$ | Fréquence d'activation de la règle $r$ |
| $F_x(\omega)$ | Vecteur fréquentiel (profil dynamique) de $x$ |
| $T_{\mathrm{emerg}}^{(\varepsilon)}(\omega)$ | Types émergents à résolution $\varepsilon$ |
| $\langle O\rangle_\omega$ | Moyenne temporelle de l'observable $O$ |
| $\pi_\Lambda$ | Mesure stationnaire sur $\mathcal{C}_\Lambda$ (cutoff $\Lambda$) |

---

## Introduction

### Motivation

Au niveau I.A, nous avons défini :

- Un espace de configurations (classes d’isomorphisme) $\mathcal{C}$ et un coût combinatoire $K$.
- Un catalogue fini de règles locales $\mathcal{R}$ et des événements élémentaires $e$.
- Une causalité locale via dépendance immédiate ($\to$) et clôture transitive ($\prec$).
- Un espace d’histoires $\Omega$ et (au moins) une famille de mesures régularisées à cutoff $\mu_{\beta,\Lambda}$.

**Question centrale** : comment passer des événements microscopiques à des quantités macroscopiques (fréquences, moyennes, "types" dynamiques) sans postuler de temps externe ?

### Idée directrice

Le "temps" Au niveau I est un artefact interne : on ne dispose que de l’énumération des événements, de la structure causale et de compteurs qui mesurent *combien* et *comment* chaque élément est impliqué dans l’évolution.

Ce document introduit :
- des compteurs Read/Write,
- des fréquences (globales et conditionnelles à la durée de vie),
- des types émergents (classes de comportement),
- des moyennes temporelles (vide statistique),
- et des conditions (souvent à cutoff) garantissant l’existence de limites et d’une mesure stationnaire.

---

# B0 — Rappels et fondements

## B0.1 — Concepts de I.A nécessaires (version cohérente)

### Configurations et événements

Une configuration est un hypergraphe étiqueté fini (cf. I.A) :
$$H = (V, E, S, \tau, \sigma).$$

Un événement élémentaire est un quadruplet :
$$e=(H,r,\mu,H')$$
où $r\in\mathcal{R}$, $\mu$ est un match valide de $r$ dans $H$, et $H'$ est la configuration obtenue après application.

### Read/Write (avec contexte + création/suppression)

Soit $r:L\Rightarrow R$ avec interface (partie conservée) $I=L\cap R$ et match $\mu$ dans $H$.
On note :
- $L_\mu$ l’occurrence de $L$ dans $H$,
- $I_\mu$ l’image de $I$ dans $H$,
- $C_\mu$ un contexte local lu (voisinage requis par l’applicabilité, le rayon $R_r$ et/ou le calcul local de $\Delta K$).

On définit alors :

- **Lecture** :
$$\mathrm{Read}(e)=L_\mu\cup C_\mu.$$

- **Écriture** :
$$\mathrm{Write}(e)=\mathrm{Del}(e)\cup \mathrm{Mod}(e)\cup \mathrm{New}(e),$$
avec
$$\mathrm{Del}(e)=L_\mu\setminus I_\mu,\qquad
\mathrm{Mod}(e)\subseteq I_\mu,\qquad
\mathrm{New}(e)=R\setminus I.$$

> Remarque : 
>
> - "création pure" $\Rightarrow \mathrm{Read}(e)$ peut être vide sur le nouvel élément ; 
> - "destruction" $\Rightarrow \mathrm{Write}(e)$ contient des éléments qui cessent d’exister après l’événement.

### Causalité : dépendance immédiate puis ordre strict

On introduit d’abord la dépendance immédiate :
$$e_1\to e_2 \quad\Longleftrightarrow\quad \mathrm{Write}(e_1)\cap \mathrm{Read}(e_2)\neq\emptyset.$$

Puis la précédence causale est la clôture transitive de $\to$ :
$$e_1\prec e_2 \quad\Longleftrightarrow\quad \exists (f_0,\dots,f_k): f_0=e_1,\ f_k=e_2,\ \forall i,\ f_i\to f_{i+1}.$$

Ainsi $\prec$ est un ordre strict (transitif et irréflexif) sur les événements d’une histoire.  
On peut définir la fermeture réflexive $\preceq$ si besoin : $e_1\preceq e_2 \iff (e_1\prec e_2)\ \text{ou}\ (e_1=e_2)$.

---

## B0.2 — Le problème du temps

### Absence de temps absolu

Au niveau I, il n’existe ni métrique, ni horloge externe, ni paramètre $t$ donné a priori.  
Toute notion de "durée" doit être construite à partir de :

- la structure causale des événements,
- la progression de la réécriture,
- et des compteurs intrinsèques.

### Temps causal vs temps métrique

- Le temps causal est un ordre (partiel) sur des événements : il dit "quoi peut influencer quoi".
- Un temps métrique (avec unités) n’existe pas encore ; il apparaîtra seulement au niveau IV dans les phases quasi-lisses.

---

## B0.3 — Stratégie : compteurs locaux

### Idée directrice

Chaque élément $x\in V\sqcup E$ subit :
- des lectures (il est consulté pour décider ou appliquer un événement),
- des écritures (il est créé, modifié ou supprimé).

En comptant ces interactions le long d’une histoire, on définit :
- un temps local pour chaque élément,
- et des fréquences qui caractérisent l’activité et les rôles dynamiques.

---

# B1 — Compteurs locaux (Read/Write)

## B1.1 — Définitions formelles

Soit $\omega=(e_1,e_2,\dots)$ une histoire (séquence d’événements) et $x\in V\sqcup E$.

### Compteur de lecture

$$n_x^{\mathrm{read}}(\omega,k)=\sum_{i=1}^k \mathbf{1}_{x\in \mathrm{Read}(e_i)}.$$

### Compteur d’écriture

$$n_x^{\mathrm{write}}(\omega,k)=\sum_{i=1}^k \mathbf{1}_{x\in \mathrm{Write}(e_i)}.$$

### Temps local

On définit le temps local (ou "âge interactionnel") :
$$\tau_x(\omega,k)=n_x^{\mathrm{read}}(\omega,k)+n_x^{\mathrm{write}}(\omega,k).$$

> Convention : si $x$ n’existe pas avant son événement de création $e_j$, alors ses compteurs valent $0$ pour $k<j$ (les "nouvelles instances" sont distinctes).

---

## B1.2 — Temps global : jauge, séquentialisation et causalité

### Pourquoi un temps global ?

Pour comparer deux éléments distincts, on utilise souvent un paramètre global (par exemple "après $k$ événements").  
Mais la causalité $\prec$ est un ordre partiel : des événements peuvent être concurrents.

### Deux paramétrisations utiles

**(A) Temps séquentiel (processus de réécriture)**  
Dans une réalisation dynamique (simulation, chaîne de Markov), on applique un événement à la fois.  
Le temps global est alors simplement l’indice $k$ dans la séquence $\omega$.

**(B) Temps causal (profondeur dans le DAG d’événements)**  
On peut définir la *hauteur causale* d’un événement $e$ :
$$h(e)=1+\max\{h(e'):\ e'\prec e\},\quad h(e)=1\ \text{si $e$ n’a pas de prédécesseur}.$$
Puis considérer les "coupes" causales $\mathcal{E}_{\le n}=\{e:\ h(e)\le n\}$.

> - (A) est le plus simple et correspond à la dynamique effective ; 
> - (B) est invariant par linéarisation mais plus exigeant.

Dans ce document, nous adoptons (A) par défaut (cohérent avec la construction markovienne de I.A), tout en rappelant que (B) existe et fournit des observables causalement invariantes.

### Activité parallèle (commutation)

Deux événements $e_i,e_j$ sont concurrents s’ils sont causalement indépendants (cf. I.A) ; on note $e_i\parallel e_j$.  
Lorsque $e_i\parallel e_j$ et que les zones Read/Write sont disjointes, l’ordre relatif de ces deux événements n’affecte pas les résultats *globaux* (par exemple des sommes sur un ensemble fixé d’événements), mais peut affecter des quantités "préfixes".

Pour cette raison, les observables asymptotiques (fréquences, moyennes) seront formulées de manière à être robustes :
- soit sous hypothèse d’ergodicité/stationnarité,
- soit via des moyennes de Cesàro,
- soit via des constructions causalement invariantes (option B).

---

## B1.3 — Propriétés de base des compteurs

### Additivité

Pour une concaténation $\omega=\omega_1\cdot \omega_2$ et $k=k_1+k_2$ :
$$n_x^{\mathrm{read}}(\omega,k)=n_x^{\mathrm{read}}(\omega_1,k_1)+n_x^{\mathrm{read}}(\omega_2,k_2),$$
et de même pour $n_x^{\mathrm{write}}$.

### Invariance par isomorphisme

Si $\varphi$ est un isomorphisme (relabeling) et $\omega'=\varphi(\omega)$, alors :
$$n_{\varphi(x)}^{\mathrm{read}}(\omega',k)=n_x^{\mathrm{read}}(\omega,k),\qquad
n_{\varphi(x)}^{\mathrm{write}}(\omega',k)=n_x^{\mathrm{write}}(\omega,k).$$

### Bornes

Toujours :
$$0\le n_x^{\mathrm{read}}(\omega,k)\le k,\qquad 0\le n_x^{\mathrm{write}}(\omega,k)\le k.$$

---

## B1.4 — Espérance des compteurs (si $\omega$ est aléatoire)

Si $\omega$ est tirée selon une mesure sur histoires $\mu$, alors :
$$\mathbb{E}_\mu[n_x^{\mathrm{read}}(\omega,k)]
=\sum_{i=1}^k \mathbb{P}_\mu\big(x\in \mathrm{Read}(e_i)\big),$$
et analogiquement pour $n_x^{\mathrm{write}}$.

L’existence de limites pour $k\to\infty$ dépendra de la stationnarité/ergodicité (B5).

---

## B1.5 — Exemple court (création et suppression)

Même si deux instances successives d’un "même" motif sont isomorphes, elles sont des éléments distincts (nouveaux identifiants) : leurs compteurs ne se transmettent pas.  
Cette distinction est importante pour définir les fréquences conditionnelles à la durée de vie (B2.1).

---

# B2 — Fréquences temporelles

## B2.1 — Fréquences de lecture/écriture d’un élément

### (i) Fréquences globales (sur l’histoire entière)

On définit, si la limite existe :
$$f_x^{\mathrm{read}}(\omega)=\lim_{k\to\infty}\frac{n_x^{\mathrm{read}}(\omega,k)}{k},\qquad
f_x^{\mathrm{write}}(\omega)=\lim_{k\to\infty}\frac{n_x^{\mathrm{write}}(\omega,k)}{k}.$$

**Interprétation** : fraction des événements (au sens séquentiel) qui lisent/écrivent $x$.

> Pour un élément éphémère créé tard ou détruit tôt, ces fréquences peuvent valoir $0$ même si l’élément est "très actif" durant sa courte vie.

### (ii) Fréquences conditionnelles "sur la durée de vie"

On définit une fenêtre de vie (au sens séquentiel) :
- $k_{\mathrm{cr}}(x)$ : premier indice où $x$ apparaît (création),
- $k_{\mathrm{del}}(x)$ : premier indice où $x$ est supprimé (ou $+\infty$ s’il persiste).

La durée de vie (en pas séquentiels) est :
$$\ell_x(\omega)=\max\{0,\,k_{\mathrm{del}}(x)-k_{\mathrm{cr}}(x)\} \in \mathbb{N}\cup\{+\infty\}.$$

On définit alors les fréquences "intrinsèques" (si $\ell_x=+\infty$ et limites existantes) :
$$\tilde f_x^{\mathrm{read}}(\omega)=\lim_{k\to\infty}\frac{n_x^{\mathrm{read}}(\omega,k)-n_x^{\mathrm{read}}(\omega,k_{\mathrm{cr}}(x)-1)}{k-k_{\mathrm{cr}}(x)+1},$$
et de même pour $\tilde f_x^{\mathrm{write}}$.

**Interprétation** : la fréquence d’interaction est *conditionnée au fait que l’élément existe*.

> Cette distinction (globale vs conditionnelle) est cruciale pour des systèmes où l’activité est portée par des structures éphémères.

---

## B2.2 — Fréquence d’activation d’une règle

Soit $r\in\mathcal{R}$. On définit :
$$n_r(\omega,k)=\sum_{i=1}^k \mathbf{1}_{e_i\ \text{utilise la règle}\ r}.$$

La fréquence d’activation est, si elle existe :
$$f_r(\omega)=\lim_{k\to\infty}\frac{n_r(\omega,k)}{k}.$$

---

## B2.3 — Vecteur fréquentiel (profil dynamique)

On regroupe les fréquences d’un élément $x$ dans un vecteur (dimension finie) :
$$F_x(\omega)=\big(f^{\mathrm{read}}_{x,r_1},\dots,f^{\mathrm{read}}_{x,r_m};\ f^{\mathrm{write}}_{x,r_1},\dots,f^{\mathrm{write}}_{x,r_m}\big)\in [0,1]^{2m}$$
où $m=|\mathcal{R}|$ et
$$f^{\mathrm{read}}_{x,r}(\omega)=\lim_{k\to\infty}\frac{1}{k}\sum_{i=1}^k \mathbf{1}_{x\in \mathrm{Read}(e_i)}\mathbf{1}_{e_i\ \text{utilise}\ r},$$
et analogiquement pour $f^{\mathrm{write}}_{x,r}$.

> Variante (recommandée) : définir aussi un vecteur conditionnel $\tilde F_x$ basé sur $\tilde f$ lorsque $\ell_x=+\infty$.

---

## B2.4 — Fréquence de visite d’une configuration (ou macro-configuration)

Comme les configurations sont des classes $[H]\in\mathcal{C}$, on peut définir un processus d’états $([H_k])_{k\ge 0}$ le long d’une histoire.

Pour $A\subseteq\mathcal{C}$ (un ensemble de configurations ou un macro-état), définir :
$$n_A(\omega,k)=\sum_{i=0}^{k-1}\mathbf{1}_{[H_i]\in A}.$$

La fréquence de visite est :
$$f_A(\omega)=\lim_{k\to\infty}\frac{n_A(\omega,k)}{k}$$
si la limite existe.

---

## B2.5 — Existence des fréquences : statut correct

Il y a trois niveaux d’existence :

### (i) Sans hypothèses : les limites peuvent ne pas exister

Des histoires périodiques ou quasi-périodiques peuvent produire des oscillations.  
Dans ce cas, on peut utiliser les moyennes de Cesàro :
$$f^{\mathrm{Ces}}(\omega)=\lim_{N\to\infty}\frac1N\sum_{k=1}^N \frac{n(\omega,k)}{k},$$
lorsqu’elles existent (elles existent plus souvent que les limites simples).

### (ii) Sous stationnarité + ergodicité (théorème ergodique)

Soit $\mu$ une mesure sur $\Omega$ invariante par décalage (shift) et ergodique.  
Pour toute observable intégrable $g(\omega)$ dépendant localement de l’événement $e_1$ (par exemple $g(\omega)=\mathbf{1}_{x\in \mathrm{Read}(e_1)}$), le théorème ergodique de Birkhoff donne :
$$\lim_{k\to\infty}\frac1k\sum_{i=0}^{k-1} g(\mathrm{shift}^i(\omega)) = \mathbb{E}_\mu[g],\quad \mu\text{-p.s.}$$

En particulier, les fréquences $f_x^{\mathrm{read}}, f_x^{\mathrm{write}}, f_r$ existent $\mu$-presque sûrement.

### (iii) Sous dynamique markovienne à cutoff (chaîne positive récurrente)

Si l’on travaille à cutoff $\Lambda$ (espace $\mathcal{C}_\Lambda$ fini ou dénombrable bien contrôlé) et si le processus induit sur $\mathcal{C}_\Lambda$ est une chaîne de Markov positive récurrente (en particulier : finie irréductible apériodique), alors :
- il existe une mesure stationnaire $\mu_*$,
- les fréquences temporelles existent $\mu_*$-p.s.,
- et coïncident avec les espérances sous $\mu_*$ (B5).

---

# B3 — Classes fréquentielles (types émergents)

## B3.1 — Équivalence fréquentielle : version exacte et version robuste

### Version exacte

On peut définir :
$$x\sim_{\mathrm{freq}} y \quad\Longleftrightarrow\quad F_x(\omega)=F_y(\omega).$$

C’est une relation d’équivalence.

**Attention** : l’ensemble des vecteurs possibles $F_x(\omega)$ peut être infini (les composantes sont réelles).  
Donc $|T_{\mathrm{emerg}}|$ n’est pas a priori borné par une constante ne dépendant que de $\mathcal{R}$.

### Version robuste : $\varepsilon$-types

Fixons une résolution $\varepsilon>0$ et une norme $\|\cdot\|$ sur $\mathbb{R}^{2m}$.  
On définit :
$$x\sim_{\varepsilon} y \quad\Longleftrightarrow\quad \|F_x(\omega)-F_y(\omega)\|\le \varepsilon.$$

Les $\varepsilon$-classes sont les *types émergents à résolution $\varepsilon$* :
$$T_{\mathrm{emerg}}^{(\varepsilon)}(\omega)=(V\sqcup E)/\sim_{\varepsilon}.$$

C’est cette notion qui est stable numériquement, physiquement (coarse-graining) et conceptuellement.

---

## B3.2 — Types émergents vs types primitifs

Les types primitifs $T_V,T_E$ sont des étiquettes de représentation (A0).  
Les types émergents sont des classes définies par l’activité et le rôle dynamique.

- Raffinement : un seul type primitif peut se subdiviser en plusieurs types émergents.
- Coalescence : des types primitifs distincts peuvent avoir un même type émergent.

---

## B3.3 — Étiquetage émergent

On définit l’application de type émergent (exact ou à $\varepsilon$) :
$$\tau_{\mathrm{emerg}}^{(\varepsilon)}: V\sqcup E \to T_{\mathrm{emerg}}^{(\varepsilon)}(\omega),\qquad
\tau_{\mathrm{emerg}}^{(\varepsilon)}(x)=[x]_{\varepsilon}.$$

Une configuration vue à travers la dynamique peut être décrite par un ensemble de types émergents et leurs fréquences/positions, plutôt que par les étiquettes primitives.

---

## B3.4 — Stabilité des classes

### Invariance par changement d’un préfixe fini

Si deux histoires $\omega,\omega'$ diffèrent seulement par un préfixe fini (ou un nombre fini d’événements), alors toutes les fréquences asymptotiques (et donc les classes exactes ou $\varepsilon$) coïncident :
$$T_{\mathrm{emerg}}^{(\varepsilon)}(\omega)=T_{\mathrm{emerg}}^{(\varepsilon)}(\omega').$$

### Stabilité probabiliste sous ergodicité

Sous stationnarité + ergodicité, les types émergents à résolution $\varepsilon$ sont bien définis $\mu$-presque sûrement et ne dépendent pas d’un choix "typique" de trajectoire.

---

## B3.5 — Nombre de types émergents : bornes correctes

### Borne inférieure (conjecture "univers riche")

Pour des histoires persistantes et non triviales, on peut conjecturer :
$$|T_{\mathrm{emerg}}^{(\varepsilon)}(\omega)|\ge 3,$$
par exemple : structure géométrique / degrés de liberté / couplages.

### Borne supérieure à résolution finie

Pour tout $\varepsilon>0$ et $m=|\mathcal{R}|$ :
$$F_x(\omega)\in[0,1]^{2m}.$$
Le cube $[0,1]^{2m}$ peut être recouvert par un nombre fini de boules de rayon $\varepsilon$, d’où une borne du type :
$$|T_{\mathrm{emerg}}^{(\varepsilon)}(\omega)| \le N(2m,\varepsilon) \ \lesssim\ \left(\frac{C}{\varepsilon}\right)^{2m},$$
où $C$ dépend seulement de la norme choisie.

> Cette borne reflète exactement ce qu’on veut : *à résolution finie*, il n’y a qu’un nombre fini de types dynamiques discernables.

---

# B4 — Moyenne temporelle et vide statistique

## B4.1 — Moyenne temporelle d’une observable

Une observable est une fonction $O:\mathcal{C}\to\mathbb{R}$ (ou sur un espace de macro-états).

La moyenne temporelle le long d’une histoire $\omega$ est :
$$\langle O\rangle_\omega=\lim_{k\to\infty}\frac1k\sum_{i=0}^{k-1} O([H_i]),$$
si la limite existe (ou en moyenne de Cesàro sinon).

---

## B4.2 — Vide statistique

Le "vide ontologique" (niveau I.A) est la potentialité $\Omega$.  
Le "vide statistique" (ici) correspond à un régime stationnaire : les observables ont des moyennes stables et des fluctuations caractéristiques.

On peut définir un profil statistique d’une histoire par un ensemble de moyennes :
$$\mathcal{P}(\omega)=\big(\langle O_1\rangle_\omega,\dots,\langle O_p\rangle_\omega\big).$$

Ce profil remplace l’idée (généralement ill-posed) d’une "configuration moyenne" unique.

---

## B4.3 — Lien avec les moyennes d’ensemble

Si $\mu$ est stationnaire et ergodique, alors pour toute observable intégrable :
$$\langle O\rangle_\omega = \mathbb{E}_\mu[O],\qquad \mu\text{-p.s.}$$

Cela justifie l’usage des simulations temporelles (Monte Carlo) pour estimer les grandeurs macroscopiques.

---

# B5 — Mesure stationnaire, ergodicité et pratique (cutoff)

Cette section explicite ce qui est vrai de manière standard :
- dans un modèle à cutoff (espace fini) ;
- et ce qui devient délicat en limite infinie.

---

## B5.1 — Dynamique markovienne induite (à cutoff)

Fixons un cutoff $\Lambda$ et considérons $\mathcal{C}_\Lambda=\{[H]:K(H)\le \Lambda\}$.

On suppose une dynamique séquentielle : depuis une configuration $H$, on choisit un événement activable $e$ avec probabilité $P(e\mid H)$, puis on applique $e$.

Cela induit une chaîne de Markov sur $\mathcal{C}_\Lambda$ avec matrice de transition :
$$P_\Lambda([H]\to [H'])=\sum_{e:\ H\xrightarrow{e}H'} P(e\mid H).$$

---

## B5.2 — Existence et unicité de la mesure stationnaire (cas fini)

**Théorème (standard, cas fini)**  
Si $\mathcal{C}_\Lambda$ est finie et si la chaîne est :
- irréductible (tous les états communiquent),
- apériodique,

alors :
- il existe une unique distribution stationnaire $\pi_\Lambda$,
- et pour toute observable $O$ :
$$\lim_{k\to\infty}\frac1k\sum_{i=0}^{k-1} O([H_i])=\sum_{[H]\in\mathcal{C}_\Lambda} O([H])\,\pi_\Lambda([H])\quad \text{p.s.}$$

---

## B5.3 — Quand la stationnaire est-elle la Boltzmann $\propto e^{-\beta K}$ ?

Il existe deux approches :

### (A) Mesure "canonique" posée sur configurations

On pose directement (cf. I.A) :
$$\mu_{\beta,\Lambda}([H])=\frac{e^{-\beta K(H)}}{Z_{\beta,\Lambda}}.$$

C’est une mesure d’ensemble. Elle ne dépend pas d’une dynamique particulière.

### (B) Dynamique dont la stationnaire est $\mu_{\beta,\Lambda}$ (detailed balance)

On choisit $P(e\mid H)$ de sorte que la chaîne sur $\mathcal{C}_\Lambda$ vérifie la balance détaillée :
$$\mu_{\beta,\Lambda}([H])\,P_\Lambda([H]\to[H'])=\mu_{\beta,\Lambda}([H'])\,P_\Lambda([H']\to[H]).$$

Une construction pratique est le schéma Metropolis–Hastings :

1. Proposer un événement $e$ parmi les événements activables selon une loi $q(e\mid H)$.
2. Accepter avec probabilité :
$$a=\min\{1,\exp(-\beta\Delta K)\},\qquad \Delta K=K(H')-K(H).$$
3. Sinon, rester en $H$.

Alors $\mu_{\beta,\Lambda}$ est stationnaire (et souvent unique sous irréductibilité/apériodicité).

---

## B5.4 — Calcul pratique (simulation)

### Estimer des fréquences et moyennes

- Simuler longtemps la chaîne (après un temps de burn-in).
- Estimer :
  - $f_r$ par comptage des règles,
  - $f_x^{\mathrm{read}}, f_x^{\mathrm{write}}$ par comptage Read/Write,
  - $\langle O\rangle$ par moyenne temporelle.

### Diagnostic de non-ergodicité

- dépendance forte aux conditions initiales,
- histogrammes bimodaux persistants (métastabilité),
- transitions rares (barrières de coût).

---

## B5.5 — Limite $\Lambda\to\infty$ : ce qu’on peut dire

Lorsque $\Lambda\to\infty$, il peut apparaître :
- absence de normalisation (divergence),
- fuite vers l’infini (non-récurrence),
- non-unicité des mesures stationnaires (phases multiples).

À ce stade (niveau I), on garde ces questions comme statut :
- soit on travaille à cutoff (physiquement : "budget de complexité"),
- soit on impose des conditions de stabilité (drift/récurrence),
- soit on reporte la sélection à un principe de niveau II (principe S) qui choisira des phases.

---

# Récapitulatif

1. Les compteurs Read/Write définissent un temps local $\tau_x$ et une activité mesurable sans horloge externe.
2. Les fréquences se définissent globalement (sur tout $k$) et conditionnellement (sur la durée de vie).
3. Les types émergents sont des classes de comportement ; leur version utile est à résolution $\varepsilon$.
4. Les limites et théorèmes d’existence nécessitent des hypothèses : stationnarité/ergodicité ou modèle à cutoff.
5. Le lien entre "Boltzmann" et "dynamique" se fait proprement en choisissant une dynamique qui satisfait la balance détaillée.

---

## Conjectures et questions ouvertes

**Conjecture 1 (Ergodicité générique à cutoff)**  
Pour "la plupart" des systèmes $(H_0,\mathcal{R},K,\beta)$ et pour un cutoff $\Lambda$ suffisamment grand, la chaîne markovienne induite sur $\mathcal{C}_\Lambda$ est irréductible et apériodique (donc ergodique).

**Conjecture 2 (Nombre minimal de types émergents)**  
Dans des phases persistantes "riches", on s’attend à au moins trois familles de rôles dynamiques (structure / information / couplage), c.-à-d. $|T_{\mathrm{emerg}}^{(\varepsilon)}|\ge 3$ pour une large gamme de $\varepsilon$.

**Conjecture 3 (Stabilisation des types)**  
Les $\varepsilon$-classes fréquentielles se stabilisent après un temps de mélange polynomial en la taille effective (à cutoff).

**Question ouverte 1 (limite $\Lambda\to\infty$)**  
Sous quelles conditions (drift, renormalisation, principe S) la limite sans cutoff admet-elle des mesures stationnaires non triviales ?

**Question ouverte 2 (temps causal vs temps séquentiel)**  
Peut-on définir des fréquences entièrement invariantes par linéarisation (via coupes causales) et montrer leur équivalence, en phase, aux fréquences séquentielles ?

---
