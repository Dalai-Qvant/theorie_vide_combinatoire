# Niveau III

# Émergence de la mécanique quantique

---

# Partie I : Fondations

---

# Chapitre 14 — Non-classicalité opérationnelle et nécessité d'un calcul de poids recombinables
---

## 14.0 — Rôle du chapitre

Le chapitre 13 a établi que, pour un observateur \(\mathcal O\) et une projection observationnelle
\[
\mathbf X:\Omega_B\to \mathcal H_{\mathcal O},
\]
une même trace observable \(\mathbf x\in\mathcal H_{\mathcal O}\) peut correspondre à une multitude d’histoires microscopiques \(\omega\in\Omega_B\) (préimage \(\Omega_{\mathbf x}\)), avec une croissance typiquement rapide du nombre de préimages lorsque la multiplicité observationnelle (Q0) est satisfaite.

Le présent chapitre établit le verrou suivant :

> **Verrou (Chapitre 14).** Dans certains régimes (univers \(u\), fenêtres IR, observateurs \(\mathcal O\)), les statistiques observées ne peuvent pas  être reproduites par un modèle classique adéquat (variables cachées + contraintes naturelles de cohérence), ce qui impose l’introduction d’une représentation plus riche qu’une simple mesure additive unique.  
> On en déduit la nécessité d’un calcul de poids recombinables \((K,\oplus,\odot,N)\), dont l’identification fine (et la sélection du secteur  complexe effectif) sera l’objet du Chapitre 15.

**Point méthodologique crucial.**  
Ce chapitre ne postule pas :

- un espace de Hilbert,
- des amplitudes complexes,
- la règle de Born \(P=|\psi|^2\),
- ni une dynamique unitaire.

Il établit seulement : 

* un no‑go classique (au sens correct), 

* la nécessité d’un calcul de contributions qui se recombine avant lecture probabiliste.

---

## 14.1 — Notations et données héritées (rappel minimal)

- \((\Omega_B,\Sigma_B)\) : espace mesurable des histoires (niveau II).
- \(\mu_\beta^{\{u\}}\) : mesure sélectionnée pour un univers de type \(u\) (niveau II).
- \(\mathcal O\) : observateur ; \(\mathbf X:\Omega_B\to\mathcal H_{\mathcal O}\) : projection observationnelle ;  
  \(\mu_{\mathcal O}=\mu_\beta^{\{u\}}\circ\mathbf X^{-1}\) : mesure observée.
- Une procédure de mesure est notée \(\mathsf M\) (ou "contexte" au sens opérationnel), avec des issues \(y\in\mathcal Y\).  
  Un événement observable \(E\) est un cylindre dans \(\mathcal H_{\mathcal O}\), et sa probabilité opérationnelle est \(P(E|\mathsf M)\) (définie via \(\mu_{\mathcal O}\), cf. Chapitre 13).

---

## 14.2 — Protocole : de l’interférence à un no‑go rigoureux

### 14.2.1 — Interférence à deux alternatives (motivation, pas preuve)
Des dispositifs de type "double alternative" (double fente, Mach–Zehnder, etc.) montrent expérimentalement des motifs qui sont intuitivement incompatibles avec un simple raisonnement "soit A soit B".
Cependant, en logique des fondements, l’interférence seule ne suffit pas à exclure un modèle classique général : un modèle à variables cachées *contextuel* peut toujours "mimer" une expérience isolée.

Dans cette thèse, l’interférence sert donc de motivation pour la recombinaison de contributions, mais le no‑go est formulé via des contraintes standard (localité et/ou non‑contextualité).

### 14.2.2 — Principe : un no‑go "propre" doit contraindre le classique
On choisit une famille de procédures \(\{\mathsf M_k\}\) telle que les statistiques observées imposent une contradiction avec toute représentation classique respectant une contrainte naturelle :

- **(LOC)** localité (scénario biparti), ou
- **(NC)** non‑contextualité (scénario à contextes).

Dans ce chapitre, on prend comme verrou principal le scénario biparti CHSH, car il fournit une preuve courte et robuste.

### 14.2.3 — Protocole biparti : témoin CHSH
Considérons deux régions d’observation disjointes \(A\) et \(B\) (au sens causal du niveau I, et au sens "séparées" pour \(\mathcal O\)).
Chaque côté admet deux choix de mesure :
\[
\mathsf M_A\in\{A_0,A_1\},\qquad \mathsf M_B\in\{B_0,B_1\},
\]
avec issues binaires \(a,b\in\{-1,+1\}\).

On définit les corrélations :
\[
E(A_i,B_j)=\sum_{a,b\in\{-1,+1\}} ab\,P(a,b|A_i,B_j),
\]
puis le paramètre CHSH :
\[
S = E(A_0,B_0)+E(A_0,B_1)+E(A_1,B_0)-E(A_1,B_1).
\]

**Fait (théorème standard).**  
Tout modèle classique local (LOC) satisfait :
\[
S\le 2.
\]
Le détail de la preuve est donné en annexe 14.B.

Dans la MQ standard, on peut atteindre \(S=2\sqrt 2\) (borne de Tsirelson), mais ce résultat ne sera pas utilisé ici comme postulat : nous n’utilisons que le no‑go classique \(S\le 2\).

---

## 14.3 — Définition correcte du "classique" (variables cachées)

### 14.3.1 — Modèle à variables cachées (définition)
Soit une famille finie de procédures \(\mathsf M\) (mesures) et d’issues \(y\).
Un modèle classique au sens de cette théorie est la donnée :

- d’un espace mesurable \((\Lambda,\Sigma)\) (variables cachées),
- d’une mesure de probabilité \(\nu\) sur \(\Lambda\),
- de fonctions de réponse \(P(y|\mathsf M,\lambda)\in[0,1]\),

telles que, pour toute procédure \(\mathsf M\),
\[
P_{\mathrm{obs}}(y|\mathsf M)=\int_\Lambda P(y|\mathsf M,\lambda)\,d\nu(\lambda).
\]

### 14.3.2 — Contraintes de cohérence : (LOC) et (NC)
Selon le type de test, on ajoute une contrainte naturelle :

- **(LOC) Localité (biparti).**  
  Pour \(\mathsf M=(\mathsf M_A,\mathsf M_B)\) et issues \((a,b)\),
  \[
  P(a,b|\mathsf M_A,\mathsf M_B,\lambda)=P(a|\mathsf M_A,\lambda)\,P(b|\mathsf M_B,\lambda).
  \]

- **(NC) Non‑contextualité (à contextes).**  
  Si deux procédures représentent le *même événement observable* (au sens des identifications de coarse‑graining du niveau II), alors elles doivent avoir la même fonction de réponse.

Dans ce chapitre, nous employons principalement (LOC) via CHSH.

---

## 14.4 — Condition Q1 (verrou) : impossibilité d’un modèle classique adéquat

### 14.4.1 — Q1 comme proxy CHSH (choix principal)
On dira que l’univers \(u\) (dans une fenêtre IR et pour certains observateurs \(\mathcal O\)) satisfait Q1‑CHSH s’il existe un protocole biparti \((A_0,A_1;B_0,B_1)\) tel que
\[
S_{\mathrm{obs}} > 2.
\]
Ceci est un énoncé purement observationnel : il concerne \(\mu_{\mathcal O}\) et les procédures admissibles.

### 14.4.2 — Remarque : Sorkin (trois alternatives) est un test de Born, pas un no‑go classique
On rappelle le paramètre d’interférence à trois alternatives (Annexe 2.A) :
\[
I_3 = P_{abc}-P_{ab}-P_{ac}-P_{bc}+P_a+P_b+P_c.
\]
En MQ standard (Born quadratique), \(I_3=0\) (à précision expérimentale), tandis que l’interférence d’ordre 2 peut être non nulle.

Ainsi, un test de type Sorkin sert ici de filtre/contrôle pour la future dérivation de Born (chapitre dédié), mais ne suffit pas à établir une impossibilité classique au sens variables cachées + cohérence.

---

## 14.5 — Théorème 2.1 : no‑go classique (CHSH)

### 2.5.1 — Énoncé
**Théorème 2.1 (No‑go local, CHSH).**  
Supposons qu’il existe un modèle classique local (LOC) au sens de 2.3.  
Alors le paramètre CHSH satisfait \(S\le 2\).  
En particulier, si \(S_{\mathrm{obs}}>2\) est observé (Q1‑CHSH), aucun modèle classique local ne peut reproduire simultanément toutes les statistiques de ce protocole.

### 2.5.2 — Preuve (standard, complète)
Sous (LOC), on a :
\[
P(a,b|A_i,B_j)=\int_\Lambda P(a|A_i,\lambda)\,P(b|B_j,\lambda)\,d\nu(\lambda).
\]
Définissons, pour chaque \(\lambda\),
\[
\alpha_i(\lambda):=\sum_{a\in\{-1,+1\}} a\,P(a|A_i,\lambda)\in[-1,1],\qquad
\beta_j(\lambda):=\sum_{b\in\{-1,+1\}} b\,P(b|B_j,\lambda)\in[-1,1].
\]
Alors
\[
E(A_i,B_j)=\int_\Lambda \alpha_i(\lambda)\beta_j(\lambda)\,d\nu(\lambda).
\]
Donc
\[
S=\int_\Lambda \left(\alpha_0\beta_0+\alpha_0\beta_1+\alpha_1\beta_0-\alpha_1\beta_1\right)d\nu(\lambda).
\]
Pour chaque \(\lambda\),
\[
\alpha_0\beta_0+\alpha_0\beta_1+\alpha_1\beta_0-\alpha_1\beta_1
=\alpha_0(\beta_0+\beta_1)+\alpha_1(\beta_0-\beta_1).
\]
Comme \(\alpha_0,\alpha_1\in[-1,1]\),
\[
\left|\alpha_0(\beta_0+\beta_1)+\alpha_1(\beta_0-\beta_1)\right|
\le |\beta_0+\beta_1|+|\beta_0-\beta_1|\le 2,
\]
car pour \(x,y\in[-1,1]\), \(|x+y|+|x-y|\le 2\).  
En intégrant, on obtient \(S\le 2\). 

---

## 14.6 — Conséquence : nécessité d’un calcul de poids recombinables

### 14.6.1 — Pourquoi un simple calcul additif de probabilités est insuffisant
Si une description de la théorie se réduisait à une mesure additive classique unique (sous (LOC)) pour toutes les procédures du  protocole, elle induirait un modèle à variables cachées local reproduisant toutes les corrélations. Or le Théorème 2.1 l’exclut dès que \(S_{\mathrm{obs}}>2\).

Donc, dans un régime satisfaisant Q1‑CHSH, la théorie observationnelle ne peut pas être codée uniquement par :
- une mesure additive unique sur un espace de variables cachées,
- et des réponses locales factorisées.

Il faut une représentation plus riche, permettant que l’agrégation d’alternatives indiscernables au niveau observationnel se fasse avant la "lecture" probabiliste.

### 14.6.2 — Structure minimale : \((K,\oplus,\odot,N)\)
On introduit une structure abstraite, encore indéterminée :

- \(K\) : espace des poids (ou "contributions") d’alternatives microscopiques,
- \(\oplus\) : opération d’agrégation de contributions indiscernables,
- \(\odot\) : composition séquentielle (concaténation causale),
- \(N:K\to\mathbb R_{\ge 0}\) : lecture positive donnant des probabilités observationnelles.

Pour une procédure \(\mathsf M\) et un événement observable \(E\), on écrit formellement :
\[
W(E|\mathsf M)=\bigoplus_{\omega\in\Omega_{E,\mathsf M}} w(\omega|\mathsf M),
\qquad
P(E|\mathsf M)=N\!\left(W(E|\mathsf M)\right),
\]
où \(\Omega_{E,\mathsf M}\subset\Omega_B\) est l’ensemble des histoires compatibles avec l’événement \(E\) dans le protocole \(\mathsf M\), et \(w(\omega|\mathsf M)\in K\) est le poids élémentaire d’une histoire \(\omega\).

**Remarque.**  
À ce stade, \(N\) n’est pas supposée quadratique (ce serait Born) ; elle est seulement une lecture positive cohérente.

### 14.6.3 — Lien avec le multiway : cohérence et recombinaison
Aux niveau I–II, les histoires \(\omega\) sont produites par des réécritures locales dans un multiway.
La condition Q0 (multiplicité observationnelle) garantit l’existence de nombreuses alternatives microscopiques sous une même trace  observable.
La condition Q1 (no‑go classique) indique que ces alternatives ne peuvent pas être réduites à une simple addition de probabilités locales.

Cela motive la contrainte supplémentaire (formalisée au chapitre 14) :

> Il existe des situations où deux familles distinctes d’histoires microscopiques deviennent indiscernables au niveau observationnel,
> et doivent être agrégées par \(\oplus\) avant application de \(N\).

---

## 14.7 — Sorties du chapitre (vers le chapitre 14)

1) **No‑go local rigoureux** : si un protocole CHSH observable donne \(S_{\mathrm{obs}}>2\), aucun modèle local à variables cachées ne convient.  
2) **Nécessité d’un calcul de contributions recombinables** \((K,\oplus,\odot,N)\) au-dessus des histoires microscopiques.  
3) **Position de Sorkin** : \(I_3=0\) est un filtre de cohérence Born, pas un critère "classique vs quantique".  
4) **Prochain verrou** : montrer que l’existence d’un contrôle réversible continu force un secteur de phase \(J^2=-I\), puis sélectionner \(\mathbb C\) comme description opérationnelle canonique (Chapitre 3).

---

# ANNEXES — CHAPITRE 14

## Annexe 14.A — Paramètres d’interférence (Sorkin)

### 14.A.1 — Interférence d’ordre 2
Pour deux alternatives \(a,b\), on définit
\[
I_2(a,b) := P_{ab}-P_a-P_b.
\]

### 14.A.2 — Interférence d’ordre 3
Pour trois alternatives \(a,b,c\),
\[
I_3(a,b,c):=P_{abc}-P_{ab}-P_{ac}-P_{bc}+P_a+P_b+P_c.
\]
Dans la MQ standard (Born quadratique), on attend \(I_3=0\) (à précision expérimentale).
Un \(I_3\neq 0\) signale typiquement une déviation de Born (ou des effets non idéaux nécessitant un modèle plus fin).

---

## Annexe 14.B — Inégalité CHSH (preuve courte)

Soient des variables aléatoires \(A_0,A_1,B_0,B_1\in[-1,1]\) sur un même espace probabilisé, et posons
\[
S := A_0B_0 + A_0B_1 + A_1B_0 - A_1B_1.
\]
Alors
\[
S = A_0(B_0+B_1) + A_1(B_0-B_1),
\]
et donc
\[
|S| \le |B_0+B_1| + |B_0-B_1| \le 2.
\]
En prenant l’espérance, on obtient \(\langle S\rangle \le 2\).

---

## Annexe 14.C — Note : protocole biparti dans un cadre hypergraphique
Dans une réalisation hypergraphique, un protocole biparti correspond à :
- deux sous‑régions causalement disjointes de la fenêtre \(\mathcal W\),
- des choix de procédures locales \(A_i\) et \(B_j\),
- et une lecture observationnelle \(\mathbf X\) produisant les issues \(a,b\).

Le point clé pour CHSH est l’existence de corrélations observables violant \(S\le 2\), ce qui est une condition sur \(\mu_{\mathcal O}\) et l’ensemble des procédures admissibles.
