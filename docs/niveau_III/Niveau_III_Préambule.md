# Niveau III
# Émergence de la mécanique quantique

---

# Préambule et introduction générale

## Résumé

Cette théorie établit une dérivation de la mécanique quantique comme loi effective émergente au-dessus d’un substrat combinatoire (hypergraphe + dynamiques locales) défini aux niveaux I–II.

L’approche n’assume ni espace-temps, ni Hilbert, ni nombres complexes, ni règle de Born, ni Hamiltonien.  

On part uniquement :

- d’un espace d’histoires \((\Omega_B,\Sigma_B)\) et d’une mesure sélectionnée \(\mu_\beta^{\{u\}}\) (Niveau II),
- d’observateurs \(\mathcal O\) définissant une projection observationnelle \(\mathbf X:\Omega_B\to\mathcal H_{\mathcal O}\) (Niveau II),
- de la localité et de l’invariance causale des réécritures (Niveau I),
- et d’hypothèses opérationnelles minimales (mélange, contrôle continu, composition, cohérence des coarse-grainings).

**Résultat directeur (forme du programme)** : pour une classe d’univers \(u\) satisfaisant des conditions explicites (Q0–Q5), la théorie observationnelle induite devient nécessairement :

- **Hilbertienne** (reconstruction par treillis orthomodulaire + théorèmes de représentation),
- **complexe** (sélection du corps par composition/tomographie locale + minimalité),
- **unitaire** sous contrôles réversibles continus,
- et probabiliste via **Born** (unicité Gleason/Busch sous cohérence).

**Point conceptuel clé** : *tous les univers ne sont pas quantiques*. La MQ émerge comme un régime de phase contingent, caractérisable.

---

## Table des matières du préambule

**0.1** Contexte et motivation  
**0.2** État de l’art et problématique  
**0.3** Cadre théorique : rappel des Niveaux I et II  
**0.4** Objectifs de la thèse (OS1–OS10)  
**0.5** Ce qui doit être démontré : axiomes A1–A9 de la MQ  
**0.6** Stratégie de dérivation et architecture du Niveau III  
**0.7** Pièges de circularité (et comment les éviter)  
**0.8** Tous les univers ne sont pas quantiques : conditions Q0–Q5  
**0.9** Contributions originales  
**0.10** Plan de la thèse  
**0.11** Note méthodologique sur la rigueur

---

## 0.1. Contexte et motivation

### 0.1.1. Le mystère de la mécanique quantique

La MQ décrit la matière et la lumière avec une efficacité remarquable, mais laisse ouvertes plusieurs questions structurantes :

1. **Pourquoi ces axiomes ?** Pourquoi des états en espace de Hilbert, des mesures projectives/POVM, une dynamique unitaire ?  
2. **Pourquoi les nombres complexes ?** Pourquoi \(\mathbb C\), plutôt que \(\mathbb R\), \(\mathbb H\) (quaternions), ou une structure plus riche ?  
3. **D’où vient le "\(i\)" ?** L’unité imaginaire dans Schrödinger semble "posée". Quelle est son origine physique/opérationnelle ?  
4. **Pourquoi \( |\psi|^2 \) ?** Pourquoi la règle de Born et pas une autre lecture probabiliste ?  
5. **Mesure et "collapse"** : comment relier l’acquisition d’information (observateur) à la mise à jour d’état ?  
6. **Universalité ou contingence ?** La MQ est-elle une structure nécessaire de toute réalité possible, ou un régime de phase ?

La théorie adopte une position tranchée : la MQ n’est pas postulée, et son émergence n’est pas universelle.

### 0.1.2. Approches existantes (repères)

On peut regrouper les programmes existants en :
- reconstructions axiomatiques (principes opérationnels),
- interprétations (QBism, Everett, Bohm, etc.),
- formalismes de somme sur histoires et décohérence,
- approches de gravité quantique (ensembles causaux, réseaux de spins, etc.),
- programmes computationnels et multiway (simulations de réécritures).

Notre approche se distingue par deux engagements :
1) substrat combinatoire minimal (hypergraphe + réécritures locales) ;  
2) méthode par filtres (phases, sélection, observateurs), où la MQ apparaît comme un régime parmi d’autres.

### 0.1.3. Notre approche : émergence depuis un substrat combinatoire

Le niveau I introduit le substrat : hypergraphe, règles locales, causalité, invariances.  
Le niveau II introduit la sélection et l’observation : mesure \(\mu_\beta^{\{u\}}\), observateurs \(\mathcal O\), lois effectives via coarse-grainings.

Le niveau III répond à la question :
> *Quelles structures mathématiques minimales doivent émerger au niveau observationnel lorsqu’il existe multiplicité d’histoires, recombinaison, contrôles continus, et composition cohérente ?*

---

## 0.2. État de l’art et problématique

### 0.2.1. Contexte scientifique

Deux difficultés majeures apparaissent dans la plupart des dérivations de la MQ :
- **circularité** : on introduit implicitement \(\mathbb C\), Born, Hilbert, ou une notion équivalente (amplitudes complexes, phases) avant de "les dériver" ;
- **non-robustesse** : la dérivation dépend fortement d’axiomes à saveur déjà quantique.

### 0.2.2. Problématique spécifique

Dans notre cadre, la question devient :
> *Quelles contraintes strictement observationnelles et combinatoires forcent, et uniquement dans certains régimes, l’apparition d’une structure hilbertienne complexe, d’une dynamique unitaire continue, et de Born ?*

### 0.2.3. Verrous scientifiques

- Formaliser une notion de "non-classicalité" compatible avec notre cadre (éviter une "densité sur \(\Omega_B\)" qui serait trop restrictive).  
- Construire une reconstruction de type Hilbert sans introduire \(L^2\) "par choix naturel".  
- Sélectionner \(\mathbb C\) sans l’insérer dans le vocabulaire trop tôt (et sans confondre "secteur complexe" et "complexes postulés").  
- Relier les générateurs continus (Hamiltonien) à des données de sélection \(\beta\) et à l’action locale du niveau I, sans identifier \(\hbar\) par décret.

---

## 0.3. Cadre théorique : rappel des niveaux I et II

### 0.3.1. Niveau I (substrat)
- Hypergraphe \(H\), règles locales de réécriture, événements causaux.
- Invariance causale : commutation d’événements concurrents sans effet sur les prédictions macroscopiques.

### 0.3.2. Niveau II (sélection et observation)
- Espace d’histoires \((\Omega_B,\Sigma_B)\), univers de type \(u\).
- Mesure sélectionnée \(\mu_\beta^{\{u\}}\) (principe de sélection au paramètre \(\beta\)).
- Observateur \(\mathcal O\), projection \(\mathbf X:\Omega_B\to\mathcal H_{\mathcal O}\), mesure observée \(\mu_{\mathcal O}=\mu_\beta^{\{u\}}\circ \mathbf X^{-1}\).
- Coarse-grainings et lois effectives (niveau II.I).
- Structures informationnelles et témoins (niveau II.G), temps interne (niveau II.H).

---

## 0.4. Objectifs

### 0.4.1. Objectif général

Démontrer que la MQ (axiomes A1–A9) émerge rigoureusement comme théorie effective observationnelle dans un régime de phase caractérisable, sans circularité.

### 0.4.2. Objectifs spécifiques (OS1–OS10)

**OS1. Nécessité d’une structure d’amplitudes (vs probabilités classiques)**  

Montrer que certaines statistiques observationnelles ne peuvent pas être reproduites par un modèle classique au sens adéquat (variables cachées + fonctions de réponse). En déduire qu’un calcul "additif de probabilités" est insuffisant et qu’une structure de poids recombinables est nécessaire.

**OS2. Sélection du secteur complexe et unicité de \(\mathbb C\) (sans l’assumer)**  

(i) Prouver l’émergence d’un secteur de phase continu (existence d’un endomorphisme \(J\) tel que \(J^2=-I\)) à partir de contrôles réversibles continus.  

(ii) Exclure \(\mathbb R\) et \(\mathbb H\) comme corps de description opérationnelle canonique via composition/tomographie locale + minimalité, et conclure \(\mathbb C\).  

**Remarque** : une réalisation "octonionique" peut fournir un mécanisme UV, mais \(\mathbb C\) doit être sélectionné au niveau IR observationnel.

**OS3. Reconstruction hilbertienne (événements → espace d’états)**  

Construire la structure logique des événements observables (treillis orthomodulaire) et appliquer des théorèmes de représentation (type Piron/Solèr) pour obtenir un Hilbert sur \(\mathbb F\in\{\mathbb R,\mathbb C,\mathbb H\}\), puis utiliser OS2(ii) pour sélectionner \(\mathbb C\).  

**Important** : ne pas identifier automatiquement \(\mathcal H\) à un \(L^2(\mathcal C,\mu_\beta)\) sans hypothèses additionnelles ; donner seulement les conditions suffisantes pour une représentation \(L^2\) (ou GNS).

**OS4. Hamiltonien effectif depuis la dynamique hypergraphique et la sélection**  
Relier le noyau de propagation (multiway) à une dynamique unitaire IR ; définir le générateur \(H\) comme limite effective (Stone), et expliquer comment l’échelle \(\hbar\) apparaît comme conversion entre temps interne, phase, et normalisations de la dynamique.

**OS5. Dérivation de Schrödinger (avec le "\(i\)")**  
Une fois \(J\) établi (OS2(i)) et l’unitarité obtenue, déduire l’équation de Schrödinger par Stone, en expliquant l’origine du "\(i\)" comme structure de phase, non comme postulat.

**OS6. Dérivation de Born (unicité)**  
Montrer que la cohérence des coarse-grainings et la non-contextualité (au sens requis) imposent l’unicité de la règle probabiliste (Gleason/Busch), puis relier cette unicité à la typicalité sous \(\mu_\beta^{\{u\}}\).

**OS7. Structures canoniques (commutateurs, générateurs)**  
Définir position/impulsion comme observables/générateurs émergents issus de symétries effectives et montrer l’apparition des commutateurs \([\hat x,\hat p]=i\hbar\) dans la limite géométrique adéquate.

**OS8. Mesure et mise à jour d’état (sans "collapse" fondamental)**  
Expliquer la mesure via témoins, redondance, et décohérence émergente : la mise à jour d’état est une mise à jour informationnelle effective.

**OS9. Intrication et non-séparabilité**  
Montrer que la non-factorisabilité des états est naturelle dans un multiway avec recombinaison et composition ; relier cela à la possibilité de violations de type Bell dans les régimes Q.

**OS10. Caractérisation des univers quantiques**  
Formuler des conditions nécessaires/suffisantes (Q0–Q5) et discuter leur rôle (notamment \(\beta\), criticité, capacité mémoire, stabilité des secteurs internes).

---

## 0.5. Ce qui doit être démontré : axiomes A1–A9 de la MQ

### 0.5.1. Axiomes standards (référence)

| Axiome | Énoncé (forme standard)                | Ce qu’il faut démontrer ici                                  |
| ------ | -------------------------------------- | ------------------------------------------------------------ |
| **A1** | États = rayons d’un Hilbert            | Reconstruction \(\mathcal H\) via événements + représentation |
| **A2** | Superposition (linéarité)              | Linéarité issue de la cohérence multiway / recombinaison     |
| **A3** | Observables = opérateurs auto-adjoints | Apparition d’une algèbre d’effets/observables et représentation |
| **A4** | Mesures = projecteurs / POVM           | Définition opérationnelle et compatibilité coarse-graining   |
| **A5** | Born                                   | Probabilité = $P(\lambda) = \|\langle\lambda\|\psi\rangle\|^2$ |
| **A6** | Dynamique réversible = unitaire        | Wigner + continuité (Stone)                                  |
| **A7** | Composition = produit tensoriel        | Compatibilité avec tomographie locale / composition effective |
| **A8** | Incertitudes / commutateurs            | Générateurs et structures IR                                 |
| **A9** | Symétries (unitaires/anti-unitaires)   | Wigner au niveau projectif                                   |

---

## 0.6. Stratégie de dérivation et architecture (niveau III)

Le niveau III suit une chaîne de résultats locaux, chaque étape ajoutant un filtre.

**Architecture (idée)** :
1) poser la multiplicité observationnelle et l’impossibilité d’un calcul purement additif classique (OS1) ;  
2) établir la nécessité d’un secteur de phase continu \(J^2=-I\) (OS2(i)) ;  
3) reconstruire l’espace d’états (Hilbertisation) à partir des événements (OS3) ;  
4) sélectionner \(\mathbb C\) par composition/tomographie locale + minimalité (OS2(ii)) ;  
5) obtenir unitarité, Schrödinger, Born, puis structures canoniques (OS4–OS7) ;  
6) articuler mesure, intrication, et typologie des univers (OS8–OS10).

---

## 0.7. Pièges de circularité à éviter

Les points suivants ne doivent pas être postulés dans le niveau III :

1) \(\mathbb C\) comme "scalaires des amplitudes" ;  
2) Born (\(|\psi|^2\)) ;  
3) Hilbert \(\mathcal H\) ou \(L^2\) "naturel" ;  
4) Hamiltonien/Schrödinger sous forme déjà quantique ;  
5) intrication/tensorisation comme axiome ;  
6) commutateurs et \(\hbar\) comme données.

**Règle méthodologique** : chaque objet "quantique" doit être introduit soit comme
- conséquence d’un résultat de représentation (avec hypothèses explicites), soit
- conséquence d’un filtre opérationnel testable (continuité, composition, cohérence).

---

## 0.8. Tous les univers ne sont pas quantiques : conditions Q0–Q5

### 0.8.1. Révélation fondamentale

Dans notre cadre, la MQ n’est pas universelle : elle émerge seulement pour certaines phases et certains observateurs.

### 0.8.2. Conditions quantiques (Q0–Q5)

#### **Q0. Multiplicité observationnelle (branching sous \(\mathbf X\))**
Pour un préfixe observable \(\mathbf x_{[0,n]}\in\mathcal H_{\mathcal O}\), notons
\[
N_n(\mathbf x_{[0,n]}) := \left|\{\omega\in\Omega_B : \mathbf X(\omega)_{[0,n]}=\mathbf x_{[0,n]}\}\right|.
\]
Q0 exige qu’il existe une densité non nulle de temps où plusieurs prolongements microscopiques restent indiscernables observationnellement, de sorte que typiquement \(N_n\) croît au moins exponentiellement en \(n\).  
**Intuition** : "beaucoup d’histoires" sous une même trace observable.

#### **Q1. Non-classicalité opérationnelle (pas de modèle classique adéquat)**

**(a) Définition correcte de "classique" (variables cachées)**  
On appelle modèle classique (pour une famille finie de procédures de mesure \(\mathsf M\) et d’issues \(y\)) l’existence :

- d’un espace mesurable \((\Lambda,\Sigma)\) de variables cachées,
- d’une mesure de probabilité \(\nu\) sur \(\Lambda\),
- de fonctions de réponse \(P(y|\mathsf M,\lambda)\), telles que pour toute procédure \(\mathsf M\),
\[
P_{\mathrm{obs}}(y|\mathsf M) = \int_\Lambda P(y|\mathsf M,\lambda)\,d\nu(\lambda),
\]
avec les contraintes de cohérence imposées (non-contextualité sur les identifications d’événements, et/ou localité sur les dispositifs bipartites quand pertinent).

**Condition Q1** : il existe une famille finie de tests \(\{\mathsf M_k\}\) telle qu’aucun modèle de ce type ne reproduit simultanément toutes les statistiques observées (dans une fenêtre IR).

**(b) Critères suffisants**

- **Proxy Bell/CHSH (biparti)** : existence d’un test donnant \(S_{\mathrm{CHSH}}>2\) (et \(\le 2\sqrt2\) dans le régime quantique standard).  
- **Proxy contextualité (type Kochen–Specker)** : impossibilité d’une assignation globale cohérente de valeurs aux observables partagées par des contextes.  
- **Proxy Sorkin (interférences d’ordre 2, mais pas 3)** : il existe une situation à trois alternatives où
  \[
  I_2 \neq 0 \quad\text{(interférence à deux alternatives)},
  \qquad
  I_3 = 0 \quad\text{(pas d’interférence d’ordre 3)},
  \]
  avec
  \[
  I_2(a,b)=P_{ab}-P_a-P_b,
  \quad
  I_3(a,b,c)=P_{abc}-P_{ab}-P_{ac}-P_{bc}+P_a+P_b+P_c.
  \]
  Dans la MQ standard : \(I_2\) peut être non nul tandis que \(I_3\) est nul (à précision expérimentale).

**Remarque** : la version "\(I_3>\varepsilon\)" caractérise plutôt une physique *au-delà* de la MQ ; elle n’est pas la condition d’émergence de la MQ standard mais pourra être traitée par la suite.

#### **Q2. Stabilisation d’un secteur interne (mécanisme octonionique optionnel mais utile)**

On considère des variables informationnelles internes \(\xi_c\) (niveau II.G) pouvant prendre des valeurs dans \(\mathbb O\) (octonions) au niveau UV.

Q2 demande qu’il existe une direction interne stabilisée \(\mathbf n \in S^7\subset\mathbb O\) (unitaire, imaginaire) telle que la redondance des témoins la rende objectivée :
\[
\mu_\beta^{\{u\}}(R_{\mathbf n}\ge R_0)\approx 1,
\]
où \(R_{\mathbf n}\) est un degré de redondance (niveau II.G).

**Conséquence** : l’algèbre effective engendrée par \(\{1,\mathbf n\}\),
\[
\mathcal A_{\mathbf n}=\mathrm{span}_{\mathbb R}\{1,\mathbf n\},
\]
est associative et isomorphe à \(\mathbb C\) *une fois* que \(\mathbf n^2=-1\) est assuré (ce qui vaut pour une unité imaginaire normalisée).

**Rôle** : Q2 n’est pas indispensable à la sélection IR de \(\mathbb C\) (qui peut venir de OS2(i)+(ii)), mais fournit un mécanisme UV compatible avec les développements ultérieurs (symétries/jauge au niveau IV).

#### **Q3. Fenêtre critique en \(\beta\) (sélection et cohérence)**
Le paramètre \(\beta\) (Principe S) doit être dans une fenêtre où :
- la phase n’est ni chaotique (\(\beta\to 0\)),
- ni figée (\(\beta\to\infty\)),
- mais suffisamment structurée pour supporter cohérence et contrôles continus.

Conjecture de travail : la MQ émerge près d’un régime critique \(\beta\approx \beta_c\).

#### **Q4. Condition phénoménologique (notre univers 3+1)**
Pour retrouver la MQ *telle que nous l’observons* (couplée à une géométrie effective standard), il faut que la géométrie émergente IR (niveau II.I / niveau IV) soit compatible avec \(3+1\).  

**Important** : Q4 n’est pas nécessaire à la structure quantique en tant que telle.

#### **Q5. Observateurs capables de maintenir des cohérences**
Il doit exister des observateurs \(\mathcal O\) dont la capacité mémoire/structure de témoin permet l’accès à des corrélations fines (sinon, la décohérence effective rend Q1 indétectable).

### 0.8.3. Typologie (schéma)

| Type d’univers                      |   Q0 |   Q1 |            Q2 |   Q3 |   Q5 | MQ observationnelle ? |
| ----------------------------------- | ---: | ---: | ------------: | ---: | ---: | --------------------: |
| Stérile                             |      |      |               |      |      |                       |
| Classique fort                      |    x |      | (peu importe) |    !️ |    x |                       |
| "Au-delà MQ" (Sorkin \(I_3\neq 0\)) |    x |    x |             ! |    x |    x |         ≠ MQ standard |
| Quantique (standard)                |    x |    x |   (optionnel) |    x |    x |                     x |

---

## 0.9. Contributions originales

1) Dérivation observationnelle de la MQ sans supposer \(\mathbb C\), Born ou Hilbert.  
2) Sélection de \(\mathbb C\) comme corps opérationnel canonique via composition/tomographie locale + minimalité, et non par simple choix.  
3) Mise en évidence du rôle de \(\beta\) (régimes de phase) et de la capacité des observateurs (Q5).  
4) Articulation possible avec un mécanisme UV interne (octonions) sans confondre UV riche et IR minimal.  
5) Cadre permettant d’adosser les preuves à des proxies simulables (multiway/atlas).

---

## 0.10. Plan de la théorie (vue d’ensemble)

- **Niveaux I–II** : substrat combinatoire, sélection \(\mu_\beta\), observateurs, lois effectives.  
- **Niveau III** (ce volume) : voir ci-dessous
- **Niveau IV** (à venir) : géométrie émergente, jauge, SM-like, GR-like, etc.
- **Niveau V** (à venir) : gravité quantique, trous noirs, matière noire, énergie noire, etc.

## Plan du niveau III (12 chapitres en 5 parties)

**PARTIE I : FONDATIONS**

- Chapitre 13 : Chemins multiples et classes d'équivalence 
- Chapitre 14 : Non-classicalité opérationnelle et nécessité d'un calcul de poids recombinables

**PARTIE II : STRUCTURE ALGÉBRIQUE**

- Chapitre 15 : Du degré interne octonionique au secteur complexe effectif
- Chapitre 4 : Espace de Hilbert 

**PARTIE III : DYNAMIQUE**

- Chapitre 5 : Hamiltonien depuis principe S 
- Chapitre 6 : Équation de Schrödinger 

**PARTIE IV : MESURE ET OBSERVATION**

- Chapitre 7 : Règle de Born 
- Chapitre 8 : Commutateurs 
- Chapitre 9 : Mesure et effondrement 
- Chapitre 10 : Intrication 

**PARTIE V : CONDITIONS ET EXTENSIONS**

- Chapitre 11 : Conditions sur univers (Q1-Q5)  (typologie)
- Chapitre 12 : Connexions profondes 

---

## 0.11. Note méthodologique sur la rigueur

### 0.11.1. Résultats locaux structurants
Chaque étape clef sera formulée en propositions/lemmes/théorèmes à hypothèses explicites, afin de rendre claire la chaîne de dépendances .

### 0.11.2. Distinction UV / IR
Une structure UV riche (ex. octonionique) n’implique pas une description IR riche : la sélection IR suit OS2(ii) (tomographie + minimalité). Ceci évite une "sur-théorie" qui ne serait pas observable.

### 0.11.3. Conditions vérifiables
Les hypothèses (Q0–Q5, H-sat, tomographie, cohérence) seront associées à des proxies calculables/simulables (densité de branching, tests CHSH/contextualité, stabilité de secteurs, etc.).
