# Niveau III
# Émergence de la mécanique quantique

---

# Partie II : Structure algébrique

---

# Chapitre 15
# Du degré interne octonionique au secteur complexe effectif (sans postuler \(\mathbb C\))

---

## Résumé du chapitre

Le chapitre 14 a établi un verrou : dans certains univers \(u\) et pour certains observateurs \(\mathcal O\), les statistiques observationnelles ne peuvent pas être reproduites par un modèle classique local à variables cachées (proxy CHSH). Il devient alors nécessaire d’introduire un calcul de contributions recombinables \((K,\oplus,\odot,N)\), sans encore imposer le choix de \(K\).

Ce chapitre montre comment, dans un mécanisme UV compatible avec les octonions, un secteur complexe effectif émerge sans être postulé :

- on suppose que certains degrés internes (niveau II.G : structures informationnelles / témoins) sont décrits en UV par des
  variables \(\xi\in\mathbb O\) (octonions) ;
- on suppose qu’une direction imaginaire unitaire \(\mathbf n^*\in S^6\subset\mathrm{Im}\,\mathbb O\) est objectivée (stabilisée) par redondance de témoins : c’est l’hypothèse de phase Q2 ;
- on montre que la cohérence opérationnelle impose que l’observateur n’accède qu’à une sous‑structure associative ;
- or, dans une algèbre alternative (comme \(\mathbb O\)), la sous‑algèbre engendrée par deux éléments est associative (théorème d’Artin),
  et en particulier le sous‑espace \(\mathcal A_{\mathbf n^*}=\mathrm{span}_{\mathbb R}\{1,\mathbf n^*\}\) est une copie canonique de \(\mathbb C\).

**Résultats principaux**

**Lemme 15.3 (Stabilisation Q2)** : sous Q2, il existe une direction imaginaire unitaire stabilisée \(\mathbf n^*\in S^6\subset\mathrm{Im}\,\mathbb O\), essentiellement unique (à une symétrie près).

2. **Proposition 15.4 (Cohérence ⇒ associativité effective)** : l’accès observationnel doit se restreindre à un secteur où les compositions
   sont associatives (sinon, ambiguïté prédictive).
3. **Lemme 15.5 (Artin)** : dans une algèbre alternative, la sous‑algèbre engendrée par deux éléments est associative.
3. **Lemme 15.6 (Plan complexe octonionique)** : si \(\mathbf n\in S^6\subset\mathrm{Im}\,\mathbb O\), alors \(\mathcal A_{\mathbf n}=\mathrm{span}_{\mathbb R}\{1,\mathbf n\}\cong\mathbb C\) et \(\mathbf n^2=-1\).
5. **Théorème 15.8 (Secteur complexe effectif)** : sous Q2 + cohérence, les poids effectifs peuvent être pris dans une copie de \(\mathbb C\)
   (unique à automorphisme près), avec une involution naturelle (conjugaison) et une norme multiplicative.

**Important.**  
Ce chapitre ne démontre pas encore la règle de Born (qui sera verrouillée plus tard via Gleason/Busch dans la phase hilbertienne).
Il ne reconstruit pas non plus l’espace de Hilbert : cela relève du chapitre de représentation (niveau III, partie suivante).
Ici, on dérive seulement l’émergence d’un secteur scalaire complexe compatible avec la recombinaison.

---

## 15.1 — Où se place le chapitre dans la chaîne logique ?

### 15.1.1. Sorties du chapitre 15
Le chapitre 15 a établi qu’il existe (dans certains régimes) des statistiques incompatibles avec un modèle classique local, donc qu’un calcul purement additif de probabilités "au niveau micro" est insuffisant.

Cela justifie l’introduction d’un objet \(K\) de "poids" et d’opérations \(\oplus,\odot\), plus une lecture positive \(N\), sans encore choisir leur nature algébrique.

### 15.1.2. Question du Chapitre 3
La question devient :

> Quel est le plus petit (et le plus naturel) secteur scalaire permettant une phase continue, une involution, et une norme multiplicative,
> lorsque la micro‑structure interne peut être plus riche (octonionique) ?

Le chapitre propose un mécanisme UV : octonions \(\to\) stabilisation \(\to\) plan associatif \(\to\) complexes.

---

## 15.2 — Hypothèse interne octonionique (UV) et redondance de témoins

### 15.2.1. Variables internes
On considère des variables informationnelles locales \(\xi_c\) (attachées à des cellules/événements \(c\)) prenant valeurs dans \(\mathbb O\).
Ces variables ne sont pas des "amplitudes fondamentales" : elles représentent un degré interne potentiel de l’hypergraphe (au sens niveau II.G : structures informationnelles), susceptible d’être partiellement observable via des témoins.

### 15.2.2. Conjugaison et partie imaginaire
On note \(\overline{x}\) la conjugaison octonionique, et \(\mathrm{Im}\,\mathbb O\cong\mathbb R^7\) la partie imaginaire.
Un imaginaire unitaire est \(\mathbf n\in\mathrm{Im}\,\mathbb O\) tel que \(|\mathbf n|=1\).
L’ensemble de ces unités imaginaires est une sphère :
\[
S^6\;\subset\;\mathrm{Im}\,\mathbb O.
\]
Pour tout \(\mathbf n\in S^6\), on a :
\[
\mathbf n^2=-1.
\]
*(Justification en Annexe 15.A.)*

### 15.2.15. Redondance et objectivation (rappel niveau II.G)
On introduit un score de redondance \(R_{\mathbf n}\) (ou plus généralement \(R(\xi)\)) quantifiant la réplication d’un même "fait interne" dans des témoins indépendants (niveau II.G).

Intuition : lorsque \(R\) est grand, une direction interne devient objectivée (robuste et partagée), donc l’observateur peut l’utiliser comme référence stable.

---

## 15.3 — Q2 : stabilisation d’une unité imaginaire (et unicité typique)

### 15.3.1. Hypothèse Q2 (forme propre)
On adopte Q2 sous une forme non ambiguë :

> **Q2 (stabilisation d’un imaginaire unitaire).**  
> Il existe un imaginaire unitaire \(\mathbf n^*\in S^6\subset\mathrm{Im}\,\mathbb O\) tel que, sous \(\mu_\beta^{\{u\}}\), la redondance \(R_{\mathbf n^*}\) est typiquement grande et \(\mathbf n^*\) est stable sur une fenêtre IR.

Cette hypothèse exprime un filtre de phase : seuls certains univers \(u\), certains \(\beta\) et certains observateurs \(\mathcal O\) permettent cette objectivation.

### 15.3.2. Lemme de stabilisation
**Lemme 15.3 (Stabilisation par redondance, version corrigée).**  
Supposons Q2. Alors il existe \(\mathbf n^*\in S^6\subset\mathrm{Im}\,\mathbb O\) tel que :

1. (**Objectivation**) \(\mu_\beta^{\{u\}}(R_{\mathbf n^*}\ge R_0)\approx 1\) pour un \(R_0\gg 1\).
2. (**Unicité typique**) si \(\mathbf n\) et \(\mathbf n'\) sont deux directions avec redondance \(\ge R_0\), alors \(\|\mathbf n-\mathbf n'\|=\mathcal O(e^{-R_0})\) (à une symétrie interne près).
3. (**Stabilité**) \(\mathbf n^*\) reste stable pour des temps internes \(\tau\) bien au‑delà d’un temps de décohérence IR.

*Preuve (schéma).*  
(1) est la formulation directe de Q2 ; 

(2) est une conséquence standard de l’objectivation par redondance : deux valeurs différentes seraient distinguées et ne pourraient pas coexister comme "fait" stable sans briser la cohérence des témoins ;
(3) découle du caractère redondant et de la localité des perturbations (une variation locale ne peut renverser un fait fortement redondant).

**Remarque.**  
L’objet \(\mathbf n^*\) n’est pas "choisi" par nous : il est une variable émergente objectivée par \(\mu_\beta^{\{u\}}\).

---

## 15.4 — Cohérence opérationnelle : pourquoi l’accès effectif doit être associatif

### 15.4.1. Le problème de la non‑associativité
L’algèbre \(\mathbb O\) est non associative. Or, pour un observateur, une même procédure composée peut admettre plusieurs parenthésages :
\[
(a\odot b)\odot c \quad \text{vs}\quad a\odot (b\odot c).
\]
Si le résultat dépend du parenthésage, une description opérationnelle ne peut pas être cohérente : la "même transformation effective" serait ambiguë.

### 15.4.2. Proposition de cohérence
**Proposition 15.4 (Cohérence ⇒ associativité effective).**  
Supposons que l’observateur \(\mathcal O\) dispose de procédures composables et que les prédictions \(P(E|\mathsf M)\) soient bien définies (indépendantes de la description computationnelle/parenthésage).
Alors les poids effectifs accessibles à \(\mathcal O\) doivent se restreindre à un secteur où la composition \(\odot\) est associative.

*Preuve.*  
Si \((a\odot b)\odot c \ne a\odot(b\odot c)\) dans le secteur accessible, alors deux descriptions d’une même procédure composée conduiraient à deux prédictions distinctes pour certains événements, violant la cohérence des coarse‑grainings (niveau II) et l’objectivité (témoin). 

**Conclusion.**  
Même si l’UV interne est octonionique, l’IR opérationnel doit sélectionner une sous‑structure associative.

---

## 15.5 — Artin : une sous‑algèbre engendrée par deux éléments est associative

### 15.5.1. Théorème d’Artin (algèbres alternatives)
Les octonions forment une algèbre alternative : les associateurs \([x,x,y]\) et \([y,x,x]\) sont nuls.
Un résultat classique en découle :

**Lemme 15.5 (Artin, version utilisée).**  
Dans une algèbre alternative, la sous‑algèbre engendrée par deux éléments quelconques est associative.

*Conséquence immédiate.*  
La sous‑algèbre engendrée par \(1\) et \(\mathbf n^*\) est associative, même si \(\mathbb O\) ne l’est pas globalement.

*(Preuve succincte en Annexe 15.A.)*

---

## 15.6 — Le "plan complexe" \(\mathrm{span}\{1,\mathbf n\}\) et son isomorphisme à \(\mathbb C\)

### 15.6.1. Définition
Pour \(\mathbf n\in S^6\subset\mathrm{Im}\,\mathbb O\), on définit :
\[
\mathcal A_{\mathbf n}:=\mathrm{span}_{\mathbb R}\{1,\mathbf n\}\subset\mathbb O.
\]

### 15.6.2. Lemme fondamental
**Lemme 15.6 (Plan complexe octonionique).**  
Si \(\mathbf n\in S^6\subset\mathrm{Im}\,\mathbb O\), alors :

1. \(\mathbf n^2=-1\).
2. \(\mathcal A_{\mathbf n}\) est fermée pour le produit et associative.
3. L’application
   \[
   \varphi:\mathbb C\to \mathcal A_{\mathbf n},\qquad \varphi(a+ib)=a+b\mathbf n
   \]
   est un isomorphisme d’algèbres (où \(i\) correspond à \(\mathbf n\)).

*Preuve.*  
(1) vient du fait qu’un imaginaire unitaire \(\mathbf n\) vérifie \(\mathbf n\overline{\mathbf n}=|\mathbf n|^2=1\) et \(\overline{\mathbf n}=-\mathbf n\), donc \(\mathbf n^2=-1\).  
(2) et l’associativité résultent de l’alternativité + Artin (Lemme 15.5) ; la fermeture se vérifie explicitement :
\[
(a+b\mathbf n)(c+d\mathbf n)=(ac-bd)+(ad+bc)\mathbf n\in\mathcal A_{\mathbf n}.
\]
(3) suit directement du calcul précédent. 

---

## 15.7 — Unicité (à symétrie interne près) et rôle de \(G_2\)

### 15.7.1. Automorphismes des octonions
Le groupe \(G_2=\mathrm{Aut}(\mathbb O)\) préserve le produit octonionique et laisse invariant l’axe réel.
Il agit naturellement sur les imaginaires unitaires \(S^6\subset\mathrm{Im}\,\mathbb O\).

**Fait (géométrie classique).**  
L’action de \(G_2\) sur \(S^6\) est transitive ; le stabilisateur d’un \(\mathbf n\in S^6\) est isomorphe à \(SU(3)\).
*(Rappel en Annexe 15.B.)*

### 15.7.2. Conséquence : "choix de \(\mathbf n\)" = jauge interne
Deux directions stabilisées \(\mathbf n\) et \(\mathbf n'\) reliées par un automorphisme \(g\in G_2\) donnent des plans \(\mathcal A_{\mathbf n}\) et \(\mathcal A_{\mathbf n'}\) isomorphes.

Ainsi, l’émergence d’un secteur complexe est unique à isomorphisme près : la donnée "quelle unité imaginaire précise" n’est pas une structure physique additionnelle si l’observateur ne mesure que des invariants du plan \(\mathcal A_{\mathbf n^*}\).

---

## 15.8 — Théorème : émergence d’un secteur scalaire complexe effectif

### 15.8.1. Énoncé principal
**Théorème 15.8 (Secteur complexe effectif, version verrouillée).**  
Supposons :

- (i) Q2 : il existe une unité imaginaire stabilisée \(\mathbf n^*\in S^6\subset\mathrm{Im}\,\mathbb O\) (Lemme 15.3) ;
- (ii) cohérence opérationnelle : les compositions accessibles sont indépendantes du parenthésage (Proposition 15.4).

Alors :

1. l’IR opérationnel peut restreindre les poids accessibles à \(K:=\mathcal A_{\mathbf n^*}\subset\mathbb O\), qui est associative ;
2. \(K\cong\mathbb C\) (Lemme 15.6) ; en particulier, il existe un "générateur de phase" \(J\) agissant comme multiplication par \(\mathbf n^*\) sur \(K\), avec \(J^2=-I\) ;
3. l’involution \(x\mapsto x^*\) naturelle pour \(K\) est la conjugaison restreinte : \((a+b\mathbf n^*)^*=a-b\mathbf n^*\) ;
4. la norme \(\|x\|^2:=x^*x\in\mathbb R_{\ge 0}\) est multiplicative sur \(K\).

*Preuve.*  
(1) et (2) : Propositions 15.4 + Lemme 15.5 sélectionnent un sous‑secteur associatif ; Q2 fournit un générateur \(\mathbf n^*\),
et Lemme 15.6 conclut \(K\cong\mathbb C\).  
(3) et (4) : sur \(\mathcal A_{\mathbf n^*}\), la conjugaison octonionique se réduit à la conjugaison complexe et
\(x^*x\) est un réel \(\ge 0\), multiplicatif. 

### 15.8.2. Interprétation par rapport aux objectifs OS2
Ce chapitre fournit un mécanisme (UV → IR) qui fabrique une structure complexe :

- il n’affirme pas que l’UV "est" \(\mathbb C\), mais que l’IR observationnel stabilisé se comporte comme \(\mathbb C\) ;
- il justifie l’apparition du "\(i\)" comme unité imaginaire stabilisée \(\mathbf n^*\) (donnée émergente).

---

## 15.9 — Ce que ce chapitre n’achève pas (et ce qui vient ensuite)

1. **Born n’est pas encore dérivée.**  

   Le fait qu’une norme \(x^*x\) existe sur \(K\cong\mathbb C\) ne suffit pas à imposer \(P(E)=\|\Pi_E\psi\|^2\). La dérivation rigoureuse de Born nécessite une reconstruction de l’espace d’états et un théorème d’unicité (Gleason/Busch) sous non‑contextualité — ce sera traité plus tard.

2. **Exclusion de \(\mathbb H\) (quaternions).**  

   Un accès effectif à plusieurs unités imaginaires stabilisées pourrait conduire à une sous‑algèbre associative plus grande (jusqu’à \(\mathbb H\)).
   La sélection opérationnelle de \(\mathbb C\) comme description canonique (tomographie locale / composition + principe S) sera introduite au niveau où la composition d’états est définie (après Hilbertisation).

3. **Lien avec le calcul \((K,\oplus,\odot,N)\) du Chapitre 2.**  

   Ici, on identifie un candidat naturel pour le "secteur scalaire" \(K\) (complexe effectif).  

   Le Chapitre suivant précisera comment la linéarité (\(\oplus\)) et la réversibilité (\(\odot\)) se représentent, et sous quelles hypothèses \(N\) devient quadratique (Born).

---

# ANNEXES — CHAPITRE 3

## Annexe 15.A — Rappels sur les octonions (faits utilisés)

### 15.A.1 — Conjugaison et imaginaire unitaire
Pour \(x\in\mathbb O\), la conjugaison \(\overline{x}\) vérifie :
\[
x\overline{x}=\overline{x}x=|x|^2\in\mathbb R_{\ge 0}.
\]
Si \(\mathbf n\in\mathrm{Im}\,\mathbb O\), alors \(\overline{\mathbf n}=-\mathbf n\).  
Si de plus \(|\mathbf n|=1\), alors \(\mathbf n\overline{\mathbf n}=1\), donc \(-\mathbf n^2=1\) et
\[
\mathbf n^2=-1.
\]

### 15.A.2 — Alternativité et Artin
Les octonions sont alternatifs : \([x,x,y]=0\) et \([y,x,x]=0\), où \([a,b,c]=(ab)c-a(bc)\) est l’associateur.
Artin : dans toute algèbre alternative, la sous‑algèbre engendrée par deux éléments est associative. C’est exactement ce qui garantit l’associativité de \(\mathcal A_{\mathbf n}\).

---

## Annexe 15.B — Action de \(G_2\) sur \(S^6\) (rappel)

- \(G_2=\mathrm{Aut}(\mathbb O)\) préserve le produit et fixe \(1\).
- Il agit sur \(\mathrm{Im}\,\mathbb O\cong\mathbb R^7\) et préserve la norme.
- Son action sur la sphère des imaginaires unitaires \(S^6\) est transitive ; le stabilisateur d’une unité est \(SU(3)\).

Ce fait formalise que le choix de \(\mathbf n^*\) est "unique à symétrie près".

---

## Annexe 15.C — Sur la cohérence (parenthésage) et les secteurs effectifs

Si un protocole effectif implique des compositions séquentielles de transformations/poids, l’observateur doit pouvoir regrouper mentalement/computationnellement ces compositions sans changer la prédiction.
Toute dépendance au parenthésage rendrait la prédiction non bien définie. Cela justifie l’hypothèse minimale : secteur associatif effectif
