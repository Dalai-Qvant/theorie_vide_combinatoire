# Niveau II - Chapitre 6

# C. Macrostates structuraux et phases stables du vide

---

## Introduction

Les chapitres précédents ont établi :
- Une structure mesurable sur l'espace des histoires $(\Omega_B, \Sigma_B)$
- Des mesures de typicalité $\mu$
- Des observables et des mécanismes de coarse-graining $\Gamma : \Omega_B \to \mathcal{M}$

Ce chapitre introduit la notion centrale de phase : un régime statistiquement homogène où les propriétés macroscopiques sont bien définies et stables.

> **Point clé :** Une phase n'est pas un "état" qui évolue dans le temps. C'est une classe de mesures sur l'espace des histoires, caractérisée par des propriétés macroscopiques typiques.

L'outil mathématique fondamental est la théorie ergodique : l'étude des mesures invariantes sous une transformation (ici, la translation $\Theta$).

---

## Partie I : Noyau ontologique

### 6.I.α — Principe de structure globale (interaction/couplage)

> **Chaque histoire possède une structure globale analysable en composantes.**

Une histoire $\omega$ n'est pas seulement une suite d'événements ; elle induit un réseau d'interactions entre événements (via recouvrement de supports Read/Write). Ce réseau se décompose en composantes d'interaction : des sous-ensembles maximaux d'événements qui interagissent entre eux mais pas avec le reste.

Cette décomposition est intrinsèque à l'histoire (définie à partir de $G_{\mathrm{int}}(\omega)$) et indépendante de toute mesure ou convention.

---

### 6.I.β — Principe de dichotomie fini/infini

> **Les composantes d'interaction se divisent en deux catégories fondamentales : finies et infinies.**

Une composante d'interaction est soit :
- **Finie** : nombre borné d'événements (fluctuation locale, "bulle" éphémère)
- **Infinie** : nombre illimité d'événements (structure persistante à grande échelle)

Cette dichotomie est absolue et ne dépend d'aucun seuil arbitraire.

---

### 6.I.γ — Principe d'homogénéité statistique (stationnarité)

> **Le vide fondamental n'a pas de position causale privilégiée.**

Une mesure représentant le "vide" doit être invariante par translation le long de la structure causale. La statistique des événements est la même quelle que soit la "position" dans l'histoire.

Ce principe est la réalisation statistique de l'absence de temps absolu.

---

### 6.I.δ — Principe d'indécomposabilité (ergodicité)

> **Une phase pure ne peut pas être décomposée en sous-phases.**

Une mesure ergodique est "indivisible" : tout ensemble invariant a mesure 0 ou 1. Il n'existe pas de sous-ensemble non trivial d'histoires qui serait statistiquement isolé du reste.

L'ergodicité caractérise les phases élémentaires — les briques fondamentales à partir desquelles toute mesure stationnaire se construit.

---

### 6.I.ε — Principe de décomposition en phases

> **Toute mesure stationnaire est un mélange de phases élémentaires.**

Si une mesure $\mu$ n'est pas ergodique, elle peut être décomposée de manière unique en une "intégrale" de mesures ergodiques. Chaque composante ergodique représente une phase pure.

Ce principe garantit que la notion de "phase" est bien définie et exhaustive.

---

### 6.I.ζ — Principe de stabilité macroscopique

> **Dans une phase stable, les propriétés macroscopiques sont asymptotiquement constantes.**

Pour une histoire typique dans une phase ergodique, les fréquences empiriques des macrostates convergent vers des valeurs déterministes. Un observateur parcourant la causalité verrait les mêmes statistiques macroscopiques "partout".

C'est l'analogue de l'équilibre thermodynamique, sans référence au temps.

---

## Partie II : Choix de représentation

### 6.1 — Cadre : système dynamique mesuré (jauge de linéarisation)

On fixe :
- Un système de niveau I $(H_0, \mathcal{R}, K, B)$
- L'espace $(\Omega_B, \Sigma_B)$ des histoires admissibles (au sens *partiel*, i.e. poset d'événements muni de $\prec$)
- Une convention de codage linéarisé d'une histoire (choix d'une extension linéaire d'un ordre partiel)
- Une mesure de probabilité $\mu$ sur $(\Omega_B, \Sigma_B)$

Dans ce chapitre, on travaille avec un codage en suite $(e_0,e_1,\dots)$ (une linéarisation). On introduit alors l'opérateur de décalage :

$$\Theta : \Omega_B \to \Omega_B, \qquad (\Theta\omega)_n := \omega_{n+1}.$$

> **Important (jauge).** Deux linéarisations d'une même histoire ne diffèrent que par permutations d'événements concurrents (commutations). Les énoncés "physiques" doivent donc être formulés pour des observables intrinsèques, invariantes sous ces permutations (ou bien moyennées sur elles).

**Hypothèse de stationnarité (sur la jauge choisie).** On suppose $\mu$ invariante par $\Theta$ :

$$\forall A \in \Sigma_B, \quad \mu(\Theta^{-1}A) = \mu(A).$$

Le quadruplet $(\Omega_B, \Sigma_B, \mu, \Theta)$ est alors un système dynamique mesuré.

**Lecture correcte :** $\Theta$ n'est pas une "évolution temporelle" physique ; c'est un reparamétrage interne du codage linéarisé. La stationnarité exprime l'absence d'instant privilégié *du point de vue des observables intrinsèques*.

---

### 6.2 — Graphe des événements : causalité et interaction

#### 6.2.1 — Graphe causal orienté (dépendances immédiates)

Pour une histoire $\omega \in \Omega_B$, on note $E(\omega)$ l'ensemble des événements.

On construit le graphe causal orienté des événements $G_{\to}(\omega)$ :

- **Sommets :** les événements $e \in E(\omega)$
- **Arêtes orientées :** une arête $e \to f$ existe ssi $f$ dépend immédiatement de $e$ :

$$\mathrm{Write}(e) \cap \mathrm{Read}(f) \neq \varnothing.$$

La relation de précédence stricte $\prec$ est la clôture transitive de $\to$ (cf. niveau I.A).

#### 6.2.2 — Graphe d'interaction (support partagé)

Pour raisonner sur des propriétés structurales globales (percolation, fragmentation, isolement), il est utile d'oublier l'orientation et de connecter aussi les événements qui se recouvrent sur leurs supports, même sans dépendance orientée immédiate.

On définit le support d'un événement :
$$\mathrm{Supp}(e):=\mathrm{Read}(e)\cup\mathrm{Write}(e).$$

On construit alors le graphe d'interaction des événements $G_{\mathrm{int}}(\omega)$ :

- **Sommets :** les événements $e \in E(\omega)$
- **Arêtes (non orientées) :** une arête relie $e$ et $f$ ssi

$$\mathrm{Supp}(e) \cap \mathrm{Supp}(f) \neq \varnothing.$$

**Interprétation :** Deux événements sont connectés s'ils "interagissent" au sens où ils impliquent des objets communs (sommets ou hyperarêtes), qu'il s'agisse d'une dépendance causale orientée ou d'un recouvrement structurel.

> **Remarque (à ne pas confondre).**
> - $G_{\to}(\omega)$ encode la causalité orientée (dépendances).
> - $G_{\mathrm{int}}(\omega)$ encode le couplage structurel (support partagé).
> Les composantes connexes de $G_{\mathrm{int}}(\omega)$ sont donc des composantes d'interaction, pas des "composantes causales" au sens strict.

#### 6.2.3 — Composantes connexes d'interaction

On note $\mathcal{C}(G_{\mathrm{int}}(\omega))$ l'ensemble des composantes connexes de $G_{\mathrm{int}}(\omega)$.

Pour chaque composante $C \in \mathcal{C}(G_{\mathrm{int}}(\omega))$ :
- **Cardinalité** : $|C| \in \mathbb{N}\cup\{\infty\}$
- **Type (optionnel)** : on peut associer à $C$ un type $\tau(C)$ (par exemple via un invariant de graphe, une distribution locale de degrés, etc.).

---

### 6.3 — Macrostates structuraux

Les macrostates structuraux sont des coarse-grainings basés sur les propriétés globales des composantes d'interaction $\mathcal{C}(G_{\mathrm{int}}(\omega))$.

#### 6.3.1 — Observable "existence d'une composante infinie"

**Définition.** L'observable de percolation (interaction) est :

$$
O_{\mathrm{inf}}(\omega) := 
\begin{cases}
1 & \text{si } \exists\, C\in\mathcal{C}(G_{\mathrm{int}}(\omega))\ \text{tel que } |C|=\infty,\\
0 & \text{sinon.}
\end{cases}
$$

**Mesurabilité :** $O_{\mathrm{inf}}$ est mesurable (limite d'événements cylindriques du type "il existe une composante de taille $\ge n$").

**Coarse-graining associé :**

$$\Gamma_{\mathrm{inf}} : \Omega_B \to \{\text{PasInf},\ \text{Inf}\}$$

avec $\Gamma_{\mathrm{inf}}(\omega)=\text{Inf}$ ssi $O_{\mathrm{inf}}(\omega)=1$.

#### 6.3.2 — Distribution des types de composantes

Pour une classification plus riche, on introduit un ensemble (dénombrable) de types $\mathcal{T}$, et une application de typage $\tau : \mathcal{C}(G_{\mathrm{int}}(\omega)) \to \mathcal{T}$ (définie par des invariants combinatoires).

On définit alors :

$$N_\omega : \mathcal{T} \to \mathbb{N} \cup \{\infty\},$$

où $N_\omega(t)$ est le nombre de composantes de type $t$ dans l'histoire $\omega$.

**Coarse-graining :**

$$\Gamma_{\mathrm{comp}} : \Omega_B \to \mathcal{M}_{\mathrm{comp}},$$

où $\mathcal{M}_{\mathrm{comp}}$ est l'espace des distributions (ou densités) de types.

Sous des hypothèses raisonnables (typage borélien, localité), $\Gamma_{\mathrm{comp}}$ est mesurable.

**Exemples de macrostates :**
- "Toutes les composantes sont finies"
- "Exactement une composante infinie de type $t_0$"
- "Densité de composantes de type $t$ égale à $\rho$"

---

### 6.4 — Ergodicité et phases élémentaires (réalisation de 6.I.δ)

#### 6.4.1 — Ensembles invariants

**Définition.** Un ensemble $A \in \Sigma_B$ est $\Theta$-invariant si :

$$\Theta^{-1}(A) = A \quad \text{(mod } \mu\text{-négligeable)}$$

**Exemples d'ensembles invariants :**
- $\{\omega : O_{\mathrm{inf}}(\omega) = 1\}$ (si $\Theta$-invariant)
- $\{\omega : \text{densité asymptotique de motif } [\mathcal{P}] = d\}$

#### 6.4.2 — Définition de l'ergodicité

**Définition 6.1 (Ergodicité).** La mesure $\mu$ est ergodique pour $\Theta$ si :

$$\forall A \in \Sigma_B, \quad \Theta^{-1}(A) = A \implies \mu(A) \in \{0, 1\}$$

**Interprétation :** Il n'existe pas de décomposition non triviale de $\Omega_B$ en sous-ensembles invariants de mesure intermédiaire.

#### 6.4.3 — Phases élémentaires

**Définition 6.2 (Phase élémentaire).** Une phase élémentaire (ou phase pure) est un système :

$$(\Omega_B, \Sigma_B, \mu_\alpha, \Theta)$$

où $\mu_\alpha$ est une mesure $\Theta$-invariante ergodique.

**Propriété clé :** Dans une phase élémentaire, tout observable $\Theta$-invariant prend une valeur constante $\mu_\alpha$-presque sûrement.

---

### 6.5 — Décomposition ergodique (réalisation de 6.I.ε)

#### 6.5.1 — Théorème de décomposition

**Théorème 6.3 (Décomposition ergodique).** Toute mesure $\Theta$-invariante $\mu$ sur $(\Omega_B, \Sigma_B)$ se décompose de manière unique en une intégrale de mesures ergodiques :

$$\mu = \int_{\mathcal{E}} \mu_\alpha \, \nu(d\alpha)$$

où :
- $\mathcal{E}$ est l'espace des mesures ergodiques sur $(\Omega_B, \Sigma_B, \Theta)$
- $\nu$ est une mesure de probabilité sur $\mathcal{E}$
- Les $\mu_\alpha$ sont les composantes ergodiques de $\mu$

*Référence : Walters, "An Introduction to Ergodic Theory", chapitre sur la décomposition ergodique.*

#### 6.5.2 — Interprétation

- Une mesure stationnaire générale $\mu$ est un mélange de phases pures
- Le poids $\nu(\{\mu_\alpha\})$ (ou $\nu(d\alpha)$) mesure la "proportion" de la phase $\mu_\alpha$ dans le mélange
- Si $\mu$ est elle-même ergodique, alors $\nu = \delta_\mu$ (mesure de Dirac)

---

### 6.6 — Phases macroscopiques

#### 6.6.1 — Mesure induite et "valeurs typiques"

Soit $\Gamma : \Omega_B \to \mathcal{M}$ un coarse-graining et $\mu_\alpha$ une mesure $\Theta$-invariante.

La mesure macroscopique induite est :

$$\mu_\alpha^\Gamma := \mu_\alpha \circ \Gamma^{-1}.$$

Il y a deux cas conceptuellement distincts :

1. **Macro-observable $\Theta$-invariante.**  
   Si $\Gamma \circ \Theta = \Gamma$ (macro-état invariant par décalage), alors, sous l'hypothèse que $\mu_\alpha$ est ergodique, $\Gamma$ est constante $\mu_\alpha$-p.s. et $\mu_\alpha^\Gamma$ est une mesure de Dirac $\delta_{m^*_\alpha}$.

2. **Macro-observable non invariante (profil macroscopique).**  
   En général, $\Gamma$ varie le long du décalage. Le comportement "typique" est alors porté par les fréquences des macrostates le long d'une histoire. Une façon robuste de l'exprimer est via la mesure empirique :

   $$\widehat\mu^{\Gamma}_N(\omega) := \frac{1}{N}\sum_{n=0}^{N-1}\delta_{\Gamma(\Theta^n\omega)}.$$

   Sous stationnarité et ergodicité (cf. 6.8), $\widehat\mu^{\Gamma}_N(\omega)$ converge (au sens faible) vers $\mu_\alpha^\Gamma$ pour $\mu_\alpha$-presque toute histoire.

#### 6.6.2 — Définition des phases macroscopiques

**Définition 6.4 (Phase macroscopique).** Pour un coarse-graining $\Gamma$ fixé :

1. Une phase macroscopique élémentaire est le couple $(\mu_\alpha, \mu_\alpha^\Gamma)$ où $\mu_\alpha$ est $\Theta$-invariante et ergodique (phase pure).
2. L'espace des phases macroscopiques est l'ensemble $\{\mu_\alpha^\Gamma : \mu_\alpha \text{ ergodique}\}$.

Deux phases macroscopiques sont distinctes si leurs mesures $\mu_\alpha^\Gamma$ diffèrent (support différent, valeurs moyennes différentes, distributions différentes, etc.).

---

### 6.7 — Exemple : phases de percolation (interaction/couplage)

On considère le coarse-graining $\Gamma_{\mathrm{inf}}$ basé sur l'existence d'une composante d'interaction infinie dans $G_{\mathrm{int}}(\omega)$ :

$$\mathcal{M}_{\mathrm{inf}} = \{\text{PasInf},\ \text{Inf}\}.$$

#### 6.7.1 — Deux phases (au sens ergodique)

Soit $\mu_\alpha$ une mesure $\Theta$-invariante ergodique. L'événement "il existe une composante infinie" est $\Theta$-invariant (au sens des observables intrinsèques), donc :

$$\mu_\alpha^{\Gamma_{\mathrm{inf}}}(\{\text{Inf}\}) \in \{0,1\}.$$

Il y a donc deux régimes ergodiques :

| Phase | Condition | Interprétation |
|-------|-----------|----------------|
| **Non percolante** | $\mu_\alpha^{\Gamma_{\mathrm{inf}}}(\{\text{Inf}\}) = 0$ | Toutes les composantes d'interaction sont finies p.s. |
| **Percolante** | $\mu_\alpha^{\Gamma_{\mathrm{inf}}}(\{\text{Inf}\}) = 1$ | Au moins une composante d'interaction infinie p.s. |

**Remarque.** Un cas "mixte" $0<\mu(\{\text{Inf}\})<1$ correspond à une mesure non ergodique (mélange de phases), et non à une phase pure.

#### 6.7.2 — Régime critique (défini par les lois de tailles, pas par 0/1)

Le "critique" se lit typiquement dans la distribution des tailles des composantes finies et les longueurs de corrélation, pas dans la valeur intermédiaire de $\mu(\{\text{Inf}\})$.

Une définition pratique (au niveau macro) consiste à considérer, pour $s\in\mathbb N$, la densité empirique de composantes finies de taille $s$ (définition schématique) :

$$\rho_s(\omega;N) := \frac{\#\{C\in\mathcal C(G_{\mathrm{int}}(\omega)):\ |C|=s\ \text{et}\ C\cap\{0,\dots,N-1\}\neq\varnothing\}}{N},$$

et ses limites $\rho_s = \lim_{N\to\infty}\rho_s(\omega;N)$ lorsqu'elles existent $\mu_\alpha$-p.s. (ergodicité).

On peut alors distinguer (heuristique standard) :
- **Sous-critique** : $\mu(\{\text{Inf}\})=0$ et la queue de $(\rho_s)$ décroît rapidement (souvent de type exponentiel).
- **Critique** : $\mu(\{\text{Inf}\})=0$ mais $(\rho_s)$ présente une queue lourde (souvent proche d'une loi de puissance) et une longueur de corrélation effective diverge.
- **Sur-critique** : $\mu(\{\text{Inf}\})=1$ et une fraction non nulle d'événements appartient à la composante infinie.

#### 6.7.3 — Interprétation physique (au niveau I)

- **Non percolante** : le vide est "fragmenté" — les couplages restent confinés à des régions finies.
- **Percolante** : le vide contient une structure couplée à grande échelle (un "réseau" d'interaction).
- **Critique** : régime de transition où apparaissent des corrélations à toutes les échelles (préfigure des transitions de phase plus riches au Niveau II).

---

### 6.8 — Stabilité macroscopique (réalisation de 6.I.ζ)

#### 6.8.1 — Profil macro (le long du décalage)

Pour un coarse-graining $\Gamma$, on définit le profil le long de la translation :

$$\Gamma_n(\omega) := \Gamma(\Theta^n \omega).$$

Le profil macroscopique de $\omega$ est la suite $(\Gamma_n(\omega))_{n \geq 0}$.

**Interprétation :** c'est la séquence des macrostates "vus" en parcourant une jauge de linéarisation. Les énoncés de stabilité doivent concerner des quantités robustes aux permutations d'événements concurrents.

#### 6.8.2 — Moyennes empiriques

Pour une fonction test $f : \mathcal{M} \to \mathbb{R}$, on définit :

$$\bar{f}_N(\omega) := \frac{1}{N} \sum_{n=0}^{N-1} f(\Gamma_n(\omega)).$$

#### 6.8.3 — Théorème ergodique (statut exact)

**Théorème 6.5 (Birkhoff).** Si $\mu$ est $\Theta$-invariante et $g\in L^1(\Omega_B,\mu)$, alors :

$$\lim_{N\to\infty}\frac{1}{N}\sum_{n=0}^{N-1} g(\Theta^n\omega)=\mathbb{E}_\mu[g\mid\mathcal I](\omega)\quad \text{pour }\mu\text{-presque tout }\omega,$$

où $\mathcal I$ est la $\sigma$-algèbre des ensembles invariants. Si de plus $\mu$ est ergodique, alors $\mathbb{E}_\mu[g\mid\mathcal I]$ est constante et vaut $\int g\,d\mu$.

En appliquant ceci à $g(\omega)=f(\Gamma(\omega))$, on obtient :

$$\lim_{N\to\infty}\bar f_N(\omega)=\int_{\mathcal M} f(m)\,\mu^\Gamma(dm)\quad \text{pour }\mu\text{-presque tout }\omega,$$

dès que $f\circ\Gamma$ est intégrable, et la limite est constante si $\mu$ est ergodique.

#### 6.8.4 — Deux niveaux de stabilité : faible et forte

**Définition 6.6 (Stabilité ergodique — faible).** Le couple $(\mu,\Gamma)$ définit une phase macroscopiquement stable (faible) si :

1. $\mu$ est $\Theta$-invariante et ergodique (au sens des observables intrinsèques),
2. pour toute fonction test bornée $f$ sur $\mathcal{M}$, les moyennes empiriques $\bar f_N(\omega)$ convergent $\mu$-p.s. vers $\int f\,d\mu^\Gamma$.

Cette stabilité exprime un "équilibre statistique" minimal : les fréquences macroscopiques existent et sont typiques.

**Définition 6.7 (Stabilité forte — optionnelle).** On parle de stabilité forte si, en plus de la stabilité faible, la dynamique macroscopique $(\Gamma_n)$ possède une propriété de mélange / décroissance des corrélations (et idéalement une inégalité de grandes déviations), assurant que les fluctuations autour des valeurs typiques sont quantitativement contrôlées.

> La stabilité forte est le bon analogue de l'“équilibre thermodynamique” avec concentration, mais elle dépend de conditions supplémentaires (cutoff, récurrence, structure du noyau de transition).

---

## Résumé de la structure

```
CHAPITRE 6 — PHASES STABLES DU VIDE
│
├── Partie I : NOYAU ONTOLOGIQUE (6 principes)
│   ├── 6.I.α  Structure
│   ├── 6.I.β  Typicalité
│   ├── 6.I.γ  Localité
│   ├── 6.I.δ  Ergodicité (indécomposabilité)
│   ├── 6.I.ε  Décomposition ergodique (exhaustivité)
│   └── 6.I.ζ  Stabilité macroscopique
│
├── 6.1  Système dynamique mesuré (jauge de linéarisation)
├── 6.2  Graphe des événements : causalité et interaction
├── 6.3  Macrostates structuraux (percolation, types de composantes)
├── 6.4  Phases élémentaires (mesures ergodiques)
├── 6.5  Décomposition ergodique
├── 6.6  Phases macroscopiques (mesures induites, profils)
├── 6.7  Exemple : percolation (0/1 en ergodique, critique par tailles)
└── 6.8  Stabilité (faible vs forte)
```

