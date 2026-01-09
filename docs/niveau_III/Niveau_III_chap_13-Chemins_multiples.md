# Niveau III

# Émergence de la mécanique quantique

---

# Partie I : Fondations



---

# Chapitre 13 - Chemins multiples et classes d'équivalence observationnelles
---

## Résumé du chapitre

Ce chapitre établit le cadre formel pour comprendre comment un observateur avec accès limité perçoit la réalité microscopique. Nous démontrons que pour une observation macroscopique fixée, il existe génériquement de multiples histoires microscopiques (chemins dans l'espace des configurations) qui sont indistinguables pour l'observateur. Cette multiplicité est la source des phénomènes d'interférence qui nécessiteront (Chapitre 14) l'introduction d'amplitudes complexes.

**Résultats principaux** :
1. Définition rigoureuse de la relation d'équivalence $\sim$ sur l'espace des histoires $\Omega_B$
2. Caractérisation des classes d'équivalence $[\omega]$
3. Théorème : Pour $u \in \mathcal{M}_{\text{quant}}$, les classes ont une cardinalité $\gg 1$ typiquement
4. Structure causale de l'ensemble des chemins $\Gamma(H_0, H_f)$
5. Préparation formelle pour les interférences (Chapitre 14)

---

## 13.1. Introduction et motivation

### 13.1.1. Le problème de l'accès limité

**Fait fondamental** (Principe Ch. II.I.α) : Un observateur interne $\mathcal{O}$ n'a pas accès à l'histoire complète $\omega \in \Omega_B$.

**Ce que l'observateur voit** : Une séquence d'observations $\mathbf{x} = (X_0, X_1, X_2, \ldots) \in \mathcal{Y}^{\mathbb{N}} = \mathcal{H}_\mathcal{O}$ où $X_j \in \mathcal{Y}$ est l'observation au "temps interne" $j$ (Ch. II.H).

**Question centrale** : Combien d'histoires microscopiques $\omega$ sont compatibles avec une séquence d'observations $\mathbf{x}$ donnée ?

**Intuition** : Beaucoup ! L'observateur ne "résout" pas les détails microscopiques.

**Objectif de ce chapitre** : Quantifier et caractériser cette multiplicité rigoureusement.

---

### 13.1.2. Pourquoi c'est important

**Motivation physique** :

Si une observation macroscopique $\mathbf{x}$ peut provenir de multiples chemins microscopiques $\omega_1, \omega_2, \ldots$, alors la question se pose :

> Comment ces chemins contribuent-ils à la probabilité d'observer $\mathbf{x}$ ?

**Deux possibilités** :

**Option 1 (Classique)** : Assigner des probabilités $p_i \geq 0$ à chaque chemin, avec $$P(\mathbf{x}) = \sum_i p_i$$

**Option 2 (Quantique)** : Assigner des amplitudes $a_i \in \mathbb{C}$ à chaque chemin, avec $P(\mathbf{x}) = \left|\sum_i a_i\right|^2$

Ce chapitre montre que la multiplicité des chemins est bien réelle et générique (pour $u \in \mathcal{M}_{\text{quant}}$).

Le Chapitre 14 démontrera que l'Option 1 est incompatible avec les observations, nécessitant l'Option 2.

---

### 13.1.3. Plan du chapitre

**Section 13.2** : Rappel du cadre observationnel (niveaux I-II)

**Section 13.3** : Définition rigoureuse de la relation d'équivalence $\sim$

**Section 13.4** : Multiplicité des chemins causaux

**Section 13.5** : Structure mathématique de l'espace des chemins

**Section 13.6** : Exemples et calculs explicites

**Section 13.7** : Implications pour le Chapitre 2

**Section 13.8** : Conclusion

---

## 13.2. Rappel du cadre observationnel

### 13.2.1. Espace des histoires (niveau I)

**Définition I.1** (Espace des histoires). L'espace des histoires est $\Omega_B = \{(\omega, H_0, (e_k)_{k \geq 0}) : \text{crédit total} \leq B\}$

où :
- $\omega$ : identifiant de l'histoire
- $H_0$ : configuration initiale (hypergraphe)
- $(e_k)_{k \geq 0}$ : séquence d'événements (applications de règles)
- $B$ : crédit global (budgétise les ressources)

**Structure** :
- σ-algèbre $\Sigma_B$ (Borel pour topologie appropriée)
- Mesure de typicalité $\mu_\beta$ (Principe S, Ch. II.E)
- Shift $\Theta : \Omega_B \to \Omega_B$ (décalage temporel)

**Évolution** : Chaque événement $e_k$ applique une règle $r_k \in \mathcal{R}$ : $e_k : H_k \mapsto H_{k+1}$

**Causalité** : Ordre partiel $\prec$ sur événements (dépendances Write/Read).

---

### 13.2.2. Observateurs et projections (niveau II)

**Définition I.2** (Observateur). Un observateur est un triplet $\mathcal{O} = (R, M, \pi_M)$ où :
- $R \subset V \cup E \cup I$ : région structurale dans l'univers $U$
- $M \subseteq C_\Sigma(R)$ : cellules de mémoire
- $\pi_M : s \mapsto m$ : projection sur état de mémoire

**État de mémoire** : $m_k = \pi_M(s^{(k)})$ à l'étape $k$

**Temps interne** (Ch. II.H) : Séquence des $j$ tels que $m_j \neq m_{j-1}$

**Observation** : Fonction mesurable $X_j = F(m_j, \text{contexte local})$ prenant valeurs dans espace fini ou dénombrable $\mathcal{Y}$.

---

### 13.2.3. Projection observationnelle

**Définition I.3** (Projection X). La projection observationnelle est l'application 
$$\mathbf{X} : \Omega_B \to \mathcal{H}_\mathcal{O} = \mathcal{Y}^{\mathbb{N}}$$
$$\omega \mapsto (X_0(\omega), X_1(\omega), X_2(\omega), \ldots)$$

**Propriétés** :
- $\mathbf{X}$ est $(\Sigma_B, \mathcal{H}_\sigma)$-mesurable
- $\mathbf{X}$ est surjective (tous les $\mathbf{x}$ sont réalisables) pour $u$ riche
- $\mathbf{X}$ est très loin d'être injective (c'est le point clé !)

**Mesure d'observation** (Ch. II.I) : $\mu_\mathcal{O} = \mu_\beta^{\{u\}} \circ \mathbf{X}^{-1}$

---

### 13.2.4. Hypothèses de travail

Dans ce chapitre, nous fixons :

**H1.** Un type d'univers $u \in \mathcal{M}_{\text{univ}}$ (Ch. II.F)

**H2.** La mesure conditionnée $\mu_\beta^{\{u\}}$ (size-biased sur type $u$)

**H3.** Un observateur $\mathcal{O}$ typique dans $u$ (satisfait critères Ch. II.G)

**H4.** Le temps interne $\tau_\mathcal{O}$ est défini (Ch. II.H)

**Aucune hypothèse quantique** : Tout est classique à ce stade.

---

## 13.3. Classes d'équivalence observationnelles

### 13.3.1. Définition de la relation $\sim$

**Définition 13.1** (Équivalence observationnelle). Deux histoires $\omega_1, \omega_2 \in \Omega_B$ sont observationnellement équivalentes pour $\mathcal{O}$, noté  $\omega_1 \sim \omega_2$, si et seulement si $\mathbf{X}(\omega_1) = \mathbf{X}(\omega_2)$ autrement dit, si elles produisent la même séquence d'observations.

**Proposition 13.2**. La relation $\sim$ est une relation d'équivalence sur $\Omega_B$.

**Preuve**. Évident :
- Réflexivité : $\omega \sim \omega$ car $\mathbf{X}(\omega) = \mathbf{X}(\omega)$
- Symétrie : $\omega_1 \sim \omega_2 \Rightarrow \omega_2 \sim \omega_1$
- Transitivité : $\omega_1 \sim \omega_2$ et $\omega_2 \sim \omega_3 \Rightarrow \omega_1 \sim \omega_3$ 

---

### 13.3.2. Classes d'équivalence

**Définition 13.3** (Classe observationnelle). Pour $\omega \in \Omega_B$, la classe d'équivalence de $\omega$ est $[\omega] = \{\omega' \in \Omega_B : \omega' \sim \omega\}$

**Espace quotient** :
$$\Omega_B / \sim \; = \{[\omega] : \omega \in \Omega_B\}$$

**Bijection canonique** :
$$\Omega_B / \sim \; \longleftrightarrow \text{Image}(\mathbf{X}) \subseteq \mathcal{H}_\mathcal{O}$$
$$[\omega] \longleftrightarrow \mathbf{X}(\omega)$$

**Interprétation** : $[\omega]$ = ensemble de toutes les histoires microscopiques donnant la même séquence observable $\mathbf{x} = \mathbf{X}(\omega)$.

---

### 13.3.3. Préimage d'une observation

**Définition 13.4** (Préimage). Pour $\mathbf{x} \in \mathcal{H}_\mathcal{O}$, la préimage est
$$\Omega_{\mathbf{x}} := \mathbf{X}^{-1}(\{\mathbf{x}\}) = \{\omega \in \Omega_B : \mathbf{X}(\omega) = \mathbf{x}\}$$

**Relation avec classes** : Si $\mathbf{X}(\omega_0) = \mathbf{x}$, alors $\Omega_{\mathbf{x}} = [\omega_0]$

**Partition** : $\Omega_B = \bigsqcup_{\mathbf{x} \in \text{Image}(\mathbf{X})} \Omega_{\mathbf{x}}$

**Question centrale** : Quelle est la cardinalité de $\Omega_{\mathbf{x}}$ ?

---

### 13.3.4. Cardinalité des classes

**Définition 13.5** (Cardinalité observationnelle). Pour $\mathbf{x} \in \mathcal{H}_\mathcal{O}$, on note $N(\mathbf{x}) := |\Omega_{\mathbf{x}}|$ le nombre d'histoires compatibles avec l'observation $\mathbf{x}$.

**Remarques** :
1. $N(\mathbf{x})$ peut être fini ou infini
2. $N(\mathbf{x})$ dépend de la "résolution" de l'observateur $\mathcal{O}$
3. Plus $\mathcal{O}$ est "grossier", plus $N(\mathbf{x})$ est grand

**Question** : Pour $u \in \mathcal{M}_{\text{quant}}$, quelle est la valeur typique de $N(\mathbf{x})$ ?

---

## 13.4. Multiplicité des chemins causaux

### 13.4.1. Chemins entre configurations (avec événements explicites)

Dans le cadre des niveaux I–II, une "application de règle" n’est pas une flèche globale (r(H)=H'), mais un événement : une règle **+** un match (localisation) dans la configuration.

**Définition 13.6 (Événement et transition).**
Un événement est un couple $e=(r,\mu)$ où $r\in\mathcal R$ est une règle et $\mu$ un match applicable de (L) dans (H) (au sens du niveau I). L’événement (e) induit une transition $H \xrightarrow{e} H' \quad\text{notée}\quad H'=e(H).$
*(Option "invariance" : on peut quotienter les matches par les automorphismes de (H) si l’on veut éliminer les surcomptages dus aux symétries.)*

**Définition 13.7 (Chemin causal).**
Un chemin causal de $H_0$ à $H_f$ est une séquence finie $\gamma=(H_0,e_0,H_1,e_1,\dots,H_{n-1},e_{n-1},H_n=H_f)$, telle que $H_{i+1}=e_i(H_i)$ pour tout (i).

**Ensemble des chemins :**
$\Gamma(H_0,H_f)={\text{tous les chemins causaux de }H_0\text{ à }H_f}$.

### 13.4.2. Compatibilité avec une observation $\mathbf x$

L’observateur ne voit pas $\omega$, mais $\mathbf X(\omega)$. Il est donc naturel de distinguer :

- les chemins microscopiques $\gamma$,
- l’observation macroscopique $\mathbf x_{[0,n]}$ (préfixe).

**Définition 13.8 (Compatibilité observationnelle).**
Soit $\mathbf x_{[0,n]}$ un préfixe d’observation. Un chemin $\gamma$ de longueur (n) est dit compatible avec $\mathbf x_{[0,n]}$ si
$\exists \omega \in \Omega_B\ \text{réalisant }\gamma\ \text{tel que}\ \mathbf X(\omega)|*{[0,n]}=\mathbf x*{[0,n]}$.
On note l’ensemble correspondant : $\Gamma(H_0,H_n\mid \mathbf x_{[0,n]})$.

------

### 13.4.3. Multiplicité "robuste" : passer du comptage à l’information

Dans $\Gamma(H_0,H_n\mid \mathbf x_{[0,n]})$, le comptage brut $|\cdot|$ est fragile (infini possible, surcomptage par symétries, dépendance à une jauge d’étiquetage). Ce qui est robuste est la quantité d’incertitude résiduelle sur le micro-chemin, sachant l’observation.

On introduit donc une variable aléatoire "choix microscopique" :

- $E_i$ : l’événement effectivement réalisé au pas (i) (donc $E_i=(r_i,\mu_i)$),
- $X_{[0,n]}$ : l’observation macroscopique au pas (n).

**Définition 13.9 (Taux d’entropie conditionnelle des choix).**
Sous une mesure stationnaire $\mu_\beta^{{u}}$ sur $\Omega_B$, on définit le taux d’entropie conditionnelle : $h_{E\mid X}:=\liminf_{n\to\infty}\frac1n,H!\big(E_{0:n-1}\mid X_{0:n}\big)$.
Intuition : $h_{E\mid X}>0$ signifie qu’en moyenne, même en connaissant l’observation, il reste une incertitude linéaire sur le micro-chemin.

------

### 13.4.4. Théorème de multiplicité 

On pose une hypothèse pré-quantique de branchement (aucune interférence ici) :

**Hypothèse (B) — Branching opérationnel.**
Il existe $b>0$ tel que, pour $\mu_\beta^{{u}}$-presque toute histoire, à une densité asymptotique $\ge b$ d’instants (i), il existe au moins deux événements distincts $e\neq e'$ applicables en $H_i$ qui restent compatibles avec le même préfixe observé $X_{0:i+1}$.

> (B) est exactement l’idée "non-déterminisme microscopique sous contrainte macroscopique", sans parler de quantique.

**Théorème 13.10 (Multiplicité effective).**
Sous stationnarité/ergodicité de $\mu_\beta^{{u}}$ et l’hypothèse (B), on a
$h_{E\mid X}\ \ge\ b\log 2\ >0$.
En particulier, pour tout $\varepsilon>0$, il existe $n_0$ tel que pour tout $n\ge n_0$, il existe un ensemble de chemins compatibles $\mathcal T_{n}(\mathbf x_{0:n})\subset \Gamma(H_0,H_n\mid \mathbf x_{0:n})$ (ensemble "typique") vérifiant simultanément :

- $\mu(\mathcal T_{n}(\mathbf x_{0:n})\mid \mathbf x_{0:n})\ge 1-\varepsilon$,
- $|\mathcal T_{n}(\mathbf x_{0:n})|\ \ge\ \exp!\big((h_{E\mid X}-\varepsilon)n\big).$

**Interprétation.** Il existe exponentiellement (en (n)) beaucoup de micro-chemins "typiques" compatibles avec une même observation, dès qu’il y a branchement opérationnel à taux positif.

**Esquisse.**
Chaque instant de branchement apporte au moins 1 bit d’incertitude conditionnelle sur $E_i$ sachant (X). Par ergodicité, la fréquence des instants de branchement tend vers (b). On en déduit une croissance linéaire de $H(E_{0:n-1}\mid X_{0:n})$, puis une taille exponentielle de l’ensemble typique (argument standard de type AEP/Shannon–McMillan–Breiman).

------

### 13.4.5. Classique vs "pré-quantique" (à ce stade)

- **Régime "classique fort"** : si, conditionnellement à (X), les choix $E_i$ deviennent déterministes à grande échelle, alors $h_{E\mid X}=0$ et la multiplicité effective ne croît pas exponentiellement.
- **Régime à branchement (pré-quantique)** : si $h_{E\mid X}>0$, la multiplicité est exponentielle avant toute discussion d’interférence.

> Le chapitre 14 pourra ensuite montrer qu'une probabilité classique sur les chemins n’explique pas certaines signatures (CHSH/contextualité/Sorkin), d’où la nécessité d’amplitudes'*.

---

## 13.5. Structure de l’espace des chemins

### 13.5.1. Graphe de configurations (avec événements)

**Définition 13.11 (Graphe de configurations).**
On définit $\mathcal G=(\mathcal C,\mathcal E)$ par :

- **Sommets** $\mathcal C$ : configurations admissibles (H) (ou classes ([H]) si l’on quotient par isomorphisme),
- **Arêtes dirigées** $(H,H')\in\mathcal E$ ssi $\exists$ un événement applicable (e) tel que $H'=e(H)$.

**Localement fini (hypothèse technique).**
On suppose que, dans le secteur considéré (budget, région finie, contraintes de complexité, etc.), le nombre d’événements applicables à (H) est fini. Sinon, il faut remplacer "localement fini" par un énoncé "localement $\sigma$-fini" (mesure sur l’ensemble des événements).

**Chemins.**
Les chemins $\Gamma(H_0,H_f)$ coïncident avec les chemins dirigés dans $\mathcal G$.

------

### 13.5.2. Distance, composantes, topologie (correction)

**Définition 13.12 (Distance de graphe étendue).**
$d_{\mathcal G}(H,H')=\inf{n:\exists \text{ chemin dirigé de longueur }n\text{ de }H\text{ vers }H'}$, avec la convention $d_{\mathcal G}(H,H')=\infty$ s’il n’existe pas de tel chemin.

- Sur chaque composante atteignable (où la distance est finie), $d_{\mathcal G}$ définit une métrique (au sens usuel) et donc une topologie métrisable.
- Globalement, c’est une distance étendue (valeur $\infty$ entre composantes), typiquement non compacte.

**Boule :** $B_n(H_0)={H\in\mathcal C:\ d_{\mathcal G}(H_0,H)\le n}$.

------

### 13.5.3. Structure causale fine (version propre)

Chaque chemin $\gamma$ porte une structure causale induite par les dépendances Read/Write (niveau I) entre événements.

**Définition 13.13 (Poset causal le long d’un chemin).**
Pour un chemin $\gamma=(H_0,e_0,\dots,e_{n-1},H_n)$, on définit un ordre partiel $\prec_\gamma$ sur ${e_0,\dots,e_{n-1}}$ par :
$e_i \prec_\gamma e_j \quad \text{si l’action de }e_i\text{ est une dépendance nécessaire pour }e_j$
(au sens Read/Write, puis transitivité).

Une linéarisation $(e_0,\dots,e_{n-1})$ est une extension linéaire de $({e_i},\prec_\gamma)$.

> Ce point sera utile au chapitre 14 : des chemins différents peuvent correspondre à des ordres différents de micro-événements compatibles avec le même ordre causal partiel.

------

### 13.5.4. Mesure induite sur les chemins (disintégration)

La mesure fondamentale $\mu_\beta^{{u}}$ est sur $\Omega_B$ (histoires). Pour obtenir une mesure sur les chemins conditionnellement à une observation, il faut passer par une désintégration.

Soit $\mathbf x$ une observation (ou un préfixe $\mathbf x_{0:n}$). On note $\mu(\cdot\mid \mathbf x)$ une version de la mesure conditionnelle (si elle existe).

**Définition 13.14 (Mesure conditionnelle sur les chemins).**
On définit une mesure $\mu_{\mathbf x}$ sur l’ensemble des chemins compatibles par
$\mu_{\mathbf x}(\gamma)
:=\mu\big({\omega:\ \omega\ \text{réalise }\gamma}\ \big|\ \mathbf X(\omega)=\mathbf x\big)$.
Alors
$\sum_{\gamma\in\Gamma(H_0,H_f\mid \mathbf x)}\mu_{\mathbf x}(\gamma)=1$
(dans le cas discret fini ; sinon remplacer la somme par une intégrale/mesure).

**Remarque importante**
$\mu_{\mathbf x}$ est une mesure classique sur des chemins. Le chapitre 14 expliquera pourquoi, dans certains régimes, aucune mesure classique sur  chemins ne reproduit toutes les signatures (contextualité/CHSH/termes d’interférence), ce qui forcera l’introduction d’amplitudes.

---

## 13.6. Exemples et calculs explicites

### 13.6.1. Exemple jouet : Système à 2 états

**Configuration** :
- 2 configurations possibles : $H_A$, $H_B$
- 2 règles : $r_1 : H_A \to H_B$, $r_2 : H_B \to H_A$

**Chemins de $H_A$ à $H_A$ en $n=2$ étapes** :
$$\Gamma(H_A, H_A, n=2) = \{H_A \xrightarrow{r_1} H_B \xrightarrow{r_2} H_A\}$$

Un seul chemin.

**Chemins en $n=4$ étapes** :
$$\Gamma(H_A, H_A, n=4) = \left\{\begin{array}{l}
H_A \to H_B \to H_A \to H_B \to H_A \\
\end{array}\right\}$$

Un seul aussi (si on fixe nombre d'étapes).

**Observation** : Observateur ne voit que "$H_A$ au départ, $H_A$ à l'arrivée", sans distinguer les étapes intermédiaires.

**Multiplicité** : Si $n$ libre, alors $|\Gamma(H_A, H_A, n \text{ pair})| = 1$ pour chaque $n$.

**Conclusion** : Exemple trop simple, pas de multiplicité réelle.

---

### 13.6.2. Exemple réaliste : Hypergraphe 1D

**Configuration** :
- Sommets sur $\mathbb{Z}$
- Arêtes entre voisins

**Règles** :
- Ajout d'arête locale
- Suppression d'arête locale
- Déplacement de motif

**Observateur** : Ne voit que la densité moyenne d'arêtes (coarse-graining).

**Observation** : $\mathbf{x} = (\rho_0, \rho_1, \ldots)$ où $\rho_j$ = densité à temps $j$.

**Multiplicité** : Pour $\rho_j$ fixé, il existe
$$|\Gamma(\rho_j)| \sim e^{S(\rho_j) \cdot |\text{système}|}$$

où $S(\rho)$ = entropie microcanonique.

**Calcul** : Pour système de taille $L$, $S(\rho) \sim L$ donc
$$|\Gamma| \sim e^{c L}$$

Exponentiel en taille !

---

### 13.6.3. Expérience de pensée : Double fente

**Setup** :
- Source $S$ émet "particule" (configuration initiale $H_S$)
- Écran avec 2 fentes $F_1$, $F_2$
- Détecteur en position $x$

**Dans le formalisme** :
- Configuration initiale : $H_S$
- Configuration finale : $H_D(x)$ (détection en $x$)

**Chemins possibles** :
- $\gamma_1$ : Via fente $F_1$
- $\gamma_2$ : Via fente $F_2$
- (Autres chemins exotiques négligeables)

**Observation** : $\mathbf{x} = (S, x)$ (source et position de détection)

**Préimage** :
$$\Omega_\mathbf{x} \supseteq \{\text{histoires réalisant } \gamma_1\} \cup \{\text{histoires réalisant } \gamma_2\}$$

**Multiplicité** : $N(\mathbf{x}) \geq 2$ (au moins 2 chemins macroscopiquement distincts).

**Remarque** : Cette multiplicité est observable via les franges d'interférence (Chapitre 14) !

---

## 13.7. Implications et préparation pour le Chapitre 14

### 13.7.1. Récapitulatif

**Ce qu'on a montré** :
1. Pour observation $\mathbf{x}$, il existe une classe $\Omega_{\mathbf{x}} = [\omega]$ d'histoires équivalentes
2. Pour $u$ quantique (Q1-Q5), $|\Omega_{\mathbf{x}}| \gg 1$ typiquement (Théorème 13.8)
3. Chemins causaux $\Gamma(H_0, H_f | \mathbf{x})$ ont cardinalité $\sim e^{cn}$
4. Structure de graphe de configurations avec croissance exponentielle
5. Mesure classique $\mu_\mathbf{x}$ sur chemins

**Point crucial** : La multiplicité est établie rigoureusement.

---

### 13.7.2. La question qui se pose

**Problème** : Comment ces multiples chemins $\gamma \in \Gamma(H_0, H_f | \mathbf{x})$ contribuent-ils à la probabilité d'observer $\mathbf{x}$ ?

**Option naïve** : Additivité classique $P(\mathbf{x}) = \sum_{\gamma} p(\gamma)$ où $p(\gamma) \geq 0$ sont des probabilités.

**Prédiction classique** : Si on bloque un chemin, la probabilité diminue strictement : $P(\mathbf{x}) > P(\mathbf{x} | \gamma_i \text{ bloqué})$

**Question** : Est-ce compatible avec les observations ?

**Réponse** (Chapitre 14) : NON !

Les expériences d'interférence (double fente, interféromètres) montrent que $P(\mathbf{x}) \neq \sum_i p(\gamma_i)$

Il peut même y avoir $P(\mathbf{x}) < P(\mathbf{x} | \gamma_i \text{ bloqué})$ (interférences destructives) !

---

### 13.7.3. Nécessité d'une nouvelle structure

**Conclusion provisoire** : La simple multiplicité des chemins + probabilités classiques est insuffisante.

**Indice** : Les chemins ne contribuent pas indépendamment, mais avec des phases relatives qui peuvent s'additionner ou s'annuler.

**Hypothèse de travail** (à démontrer au Chapitre 14) : Il faut associer à chaque chemin une amplitude $a(\gamma)$ qui n'est pas une probabilité réelle mais un nombre complexe.

Alors :
$$P(\mathbf{x}) = \left|\sum_{\gamma} a(\gamma)\right|^2$$

Ce chapitre a établi que la multiplicité existe.

Le Chapitre 14 établira que cette multiplicité nécessite des amplitudes complexes.

---

## 13.8. Conclusion du Chapitre 13

### 13.8.1. Résultats principaux

**R1.** Définition rigoureuse de la relation d'équivalence observationnelle $\omega_1 \sim \omega_2 \iff \mathbf{X}(\omega_1) = \mathbf{X}(\omega_2)$

**R2.** Classes d'équivalence $[\omega] = \Omega_{\mathbf{x}}$ ont cardinalité $N(\mathbf{x})$

**R3.** Théorème de multiplicité (1.8) : Pour $u$ quantique, $N(\mathbf{x}) \sim e^{cn}$ typiquement

**R4.** Structure de graphe de configurations $\mathcal{G}$ avec croissance exponentielle du volume

**R5.** Mesure classique $\mu_\mathbf{x}$ sur chemins (préparation pour Chapitre 2)

---

### 13.8.2. Avancée vers la MQ

**État à l'issue du Chapitre 1**3 :

- Multiplicité des chemins établie
- Structure causale clarifiée
- Pas encore d'amplitudes complexes
- Pas encore de règle de composition

**Prochaine étape** (Chapitre 2) :
- Montrer que les interférences observées sont incompatibles avec $P = \sum_i p_i$
- Démontrer que des amplitudes (avec phases) sont nécessaires
- Poser la question : Quelle algèbre ? (réponse au Chapitre 3 : ℂ uniquement)

---

### 13.8.3. Dépendances logiques

**Ce chapitre utilise** :
- Niveaux I-II (hypergraphes, $\mu_\beta$, observateurs, temps interne)
- Aucune structure quantique

**Ce chapitre établit** :
- Multiplicité des chemins (nécessaire pour interférences)

**Chapitres suivants utiliseront** :
- Ces classes $\Omega_{\mathbf{x}}$
- Ces chemins $\Gamma(H_0, H_f | \mathbf{x})$
- Cette mesure $\mu_\mathbf{x}$

**Pas de circularité** : Tout est construit depuis les niveaux I-II classiques. 

---

## Annexe 1.A : Notations

| Notation | Signification |
|----------|---------------|
| $\Omega_B$ | Espace des histoires |
| $\mathcal{O}$ | Observateur |
| $\mathbf{X}$ | Projection observationnelle |
| $\mathcal{H}_\mathcal{O}$ | Espace des trajectoires observables |
| $\omega_1 \sim \omega_2$ | Équivalence observationnelle |
| $[\omega]$ | Classe d'équivalence |
| $\Omega_{\mathbf{x}}$ | Préimage de $\mathbf{x}$ |
| $N(\mathbf{x})$ | Cardinalité de $\Omega_{\mathbf{x}}$ |
| $\Gamma(H_0, H_f)$ | Chemins causaux |
| $\mathcal{G}$ | Graphe de configurations |
| $\mu_\mathbf{x}$ | Mesure conditionnelle sur chemins |

---

## Annexe 1.B : Démonstration détaillée du Théorème 13.8

**Théorème 13.8** (rappel). Pour $u \in \mathcal{M}_{\text{quant}}$,
$$\mathbb{E}_{\mu_\beta^{\{u\}}}[|\Gamma(H_0, H_n | \mathbf{X}(\omega)|_{[0,n]})| \, | \, \mathbf{X}(\omega)|_{[0,n]}] \geq e^{c n}$$

**Démonstration complète**.

**Hypothèses** :
- $u$ satisfait Q1 (interférences typiques)
- $u$ satisfait Q3 ($\beta$ dans fenêtre critique)
- Percolation (Ch. II.C) : composante géante existe

**Étape 1 : Points de branchement**

Définissons un point de branchement comme un événement $e_k$ où :
1. Au moins 2 règles distinctes $r, r'$ sont applicables
2. Ces règles donnent des résultats $H_{k+1} \neq H'_{k+1}$ distincts
3. Ces résultats sont compatibles avec l'observation future $\mathbf{X}(\omega)|_{[k+1,n]}$

**Lemme 13.B.1**. Sous Q1, le taux de points de branchement est $\lambda > 0$ p.p.

*Preuve du lemme*. Par Q1, les interférences sont typiques. Cela implique que des chemins multiples existent et sont "proches" (corrélés sur courtes distances). Donc localement, des branchements se produisent. Birkhoff + ergodicité donnent $\lambda = \lim_{n \to \infty} \frac{1}{n}|\{k \leq n : e_k \text{ est branchement}\}|$ p.s. 

**Étape 2 : Nombre de branchements**

Entre temps $0$ et $n$, le nombre de branchements est $\sim \lambda n$ (par Lemme 13.B.1 + LGN).

**Étape 3 : Choix à chaque branchement**

À chaque branchement, au moins $b \geq 2$ choix (typiquement $b \geq 2$ par définition de branchement).

**Étape 4 : Estimation multiplicative**

Nombre total de chemins :
$$|\Gamma| \geq b^{\lambda n} = e^{(\lambda \log b) n}$$

avec $c = \lambda \log b > 0$.

**Étape 5 : Conditionnement**

Sous $\mu_\beta^{\{u\}}$, par ergodicité (Ch. II.C), cette estimation vaut en espérance conditionnelle. 

---

## Annexe 1.C : Exemple numérique

**Système** : Automate cellulaire 1D, 10 cellules

**Règle** : Règle 110 (Turing-complet)

**Observation** : Densité $\rho$ (fraction de cellules "1")

**Question** : Combien de configurations initiales donnent $\rho = 0.5$ après $t=10$ étapes ?

**Calcul** :
- Configurations totales : $2^{10} = 1024$
- Configurations avec $\rho=0.5$ : $\binom{10}{5} = 252$
- Après évolution par règle 110 : simulation numérique
- Configurations initiales menant à $\rho=0.5$ après $t=10$ : $\approx 180$ (empirique)

**Multiplicité** : $N \approx 180$ histoires distinctes donnent même observation macroscopique.

**Conclusion** : Même dans système simple, multiplicité significative ($N \gg 1$).

