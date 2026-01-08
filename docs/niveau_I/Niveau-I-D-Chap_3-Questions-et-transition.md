# Niveau I - Chapitre 3

# I.D Questions ouvertes et transition

### **Clôture du niveau I : classifier les histoires, formuler les conjectures testables, et préciser ce que le cadre ne peut pas décider sans un principe de sélection.**

---

## Table des matières

- [Introduction](#introduction)
- [D0 — État des lieux](#d0--état-des-lieux)
- [D1 — Taxonomie de Ω](#d1--taxonomie-de-ω)
- [D2 — Conjectures sur les univers viables](#d2--conjectures-sur-les-univers-viables)
- [D3 — Programme de recherche](#d3--programme-de-recherche)
- [D4 — Transition vers le Niveau II](#d4--transition-vers-le-niveau-ii)
- [Récapitulatif du Niveau I](#récapitulatif-du-niveau-i)
- [Notations (rappel)](#notations-rappel)

---

## Introduction

### Contexte

Aux niveaux I.A–I.C, nous avons :

- défini un substrat combinatoire (hypergraphes étiquetés, isomorphismes, coût combinatoire) ;
- défini des règles locales de réécriture et une notion d’événement ;
- construit un ordre causal local (via Read/Write) ;
- défini un espace d’histoires Ω et une pondération statistique (mesure sur les cylindres, éventuellement tronquée par un cutoff Λ) ;
- introduit des observables émergentes et des opérateurs de coarse-graining intrinsèques.

Le niveau I reste volontairement pré-sélection : il expose un *langage* et des *outils*, pas encore une théorie physique calibrée.

### Objectif de I.D

1. Donner une taxonomie utile des histoires ω ∈ Ω.
2. Formuler des conjectures à statut clair : conjecture / hypothèse / preview.
3. Proposer un programme de tests (principalement numériques) cohérent avec le niveau I.
4. Justifier l’introduction d’un principe de sélection (Principe S) au niveau II.

---

# D0 — État des lieux

## D0.1 — Ce qui est construit

On dispose, au sens strict, de définitions et constructions :

1. **Espace des configurations** : classes d’isomorphisme [H] et coût K(H).
2. **Catalogue de règles** 𝓡 et application locale (match, événement e = (H,r,μ,H’)).
3. **Causalité** : Read(e), Write(e), conflits, ordre partiel ≺ et cônes causaux.
4. **Espace d’histoires** Ω(H₀,𝓡) et cylindres ω₁:ₙ.
5. **Pondération** : poids locaux wβ(e|H) et probabilité locale Pβ(e|H).
6. **Observables** : fonctions locales o(H) et agrégations le long d’une histoire (moyennes, corrélations), sous réserve d’existence des limites.

> **Point important** : à ce stade, on a un *cadre* ; certaines propriétés (ergodicité, existence des limites, convergence quasi-lisse) demandent des hypothèses et/ou un cutoff Λ.

## D0.2 — Ce qui est établi sous hypothèses (statut : "si … alors …")

Les énoncés suivants sont vrais sous des conditions explicites (typiquement : troncature Λ, chaîne de Markov finie, irréductibilité, apériodicité, ou hypothèses de stationnarité/ergodicité) :

- **Stationnarité/équilibre** : existence d’une mesure stationnaire pour la dynamique tronquée ; unicité si irréductible+apériodique.
- **Moyennes temporelles** : égalité "moyenne temporelle = moyenne d’ensemble" si ergodicité (ou théorème ergodique approprié).
- **Robustesse des propriétés de queue** : stabilité des propriétés asymptotiques sous modification d’un préfixe fini.
- **Coarse-graining** : stabilité de certains observables sous changement de résolution, si l’état est dans une phase "bien mélangée".

## D0.3 — Questions ouvertes majeures (niveau I)

1. Quelles classes d’universalité existent pour des familles de règles 𝓡 ?
2. Quels critères minimaux garantissent persistance + structure (non-trivialité) ?
3. Comment relier les objets "microscopiques" (règles, motifs) à des observables macroscopiques robustes ?
4. Quelles quantités (dimension effective, courbure discrète, entropies, flux) sont les plus discriminantes numériquement ?
5. Où introduire le principe de sélection (niveau II) sans circularité ?

---

# D1 — Taxonomie de Ω

## D1.1 — Axes de classification

On classifie une histoire ω selon plusieurs axes indépendants (ce sont des "coordonnées" dans l’espace Ω) :

1. **Finitude**  
   - *finie* : ω = (e₁,…,eₙ), n < ∞  
   - *infinie* : ω = (e₁,e₂,…)  

2. **Blocage (absorption)**  
   Notons Succ(H) l’ensemble des événements activables depuis H (défini par 𝓡 et les matches).  
   - *bloquante* : ∃n tel que Succ(Hₙ)=∅  
   - *non-bloquante* : ∀n, Succ(Hₙ)≠∅

3. **Réversibilité (au sens dynamique)**  
   Deux notions à distinguer :
   - **Micro-réversibilité** : chaque événement e admet (dans le catalogue) un événement inverse e⁻¹ applicable dans le bon contexte.
   - **Réversibilité asymptotique** : la fraction d’événements "réversibles" tend vers 1 le long de ω.

4. **Persistance structurelle**  
   Informel : l’histoire ne "tourne pas à vide" (ni gel complet, ni fuite vers un attracteur trivial), et conserve une richesse de motifs/observables.

Ces axes peuvent être mesurés via des observables (temps de blocage, taux de création/destruction, diversité de motifs, stabilité des classes fréquentielles, etc.).

## D1.2 — Univers bloquants

### Définition

Une histoire ω est bloquante si :
\[
\exists n : \mathrm{Succ}(H_n)=\varnothing.
\]

### Types typiques

- **B1 — Annihilation totale** : Hₙ = ∅.
- **B2 — Gel** : Hₙ ≠ ∅ mais aucune règle n’est applicable (état "verrouillé").
- **B3 — Attracteur absorbant non trivial** : Hₙ appartient à un petit ensemble absorbant.

### Temps de blocage

\[
\tau_{\mathrm{block}}(\omega)=\min\{n : \mathrm{Succ}(H_n)=\varnothing\}.
\]

On peut ensuite définir (pour une mesure donnée sur Ω, typiquement tronquée) une moyenne ⟨τ_block⟩ et une probabilité de blocage P_block(β,Λ).

> **Remarque** : "β grand ⇒ gel" est plausible si le coût K favorise des minima absorbants, mais dépend fortement de (𝓡,K). À traiter comme *hypothèse testable*, pas comme loi générale.

## D1.3 — Univers réversibles

### Définition (version opérationnelle)

On introduit un indicateur local rev(e) ∈ {0,1} (e est "réversible" s’il existe un inverse autorisé dans le catalogue et compatible causalement).  
La réversibilité asymptotique est :

\[
\rho_{\mathrm{rev}}(\omega)=\lim_{n\to\infty}\frac{1}{n}\sum_{i=1}^n \mathrm{rev}(e_i),
\qquad \text{et "presque réversible" si }\rho_{\mathrm{rev}}(\omega)=1.
\]

### Attention conceptuelle

- La réversibilité du coût (ΔK(e) = −ΔK(e⁻¹)) n’implique pas automatiquement la réversibilité de la dynamique (conflits, accessibilité, contraintes de match).
- Inverse "formel" ≠ inverse "effectivement accessible".

## D1.4 — Univers persistants

### Définition (minimaliste, Niveau I)

Une histoire ω est dite persistante si :

1. elle est non-bloquante ;
2. certaines familles d’observables macroscopiques restent non dégénérées (variance non nulle) après un transitoire ;
3. la diversité structurale (motifs, types émergents à une résolution ε) reste bornée inférieurement.

## D1.5 — Diagramme de classification

On peut représenter Ω par un diagramme à 3 axes (blocage / réversibilité / persistance), et étudier :

- les régions "triviales" (bloquantes),
- les régions "thermiques chaotiques" (non bloquantes, peu réversibles),
- les régions "structurées" (persistantes, stabilité d’observables, éventuellement quasi-réversibles).

---

# D2 — Conjectures sur les univers viables

## D2.1 — Définition d’univers viable (hiérarchie)

Pour éviter les mélanges de niveaux, on définit une hiérarchie :

- **Viable-I (niveau I)** : persistant + non trivial (diversité minimale à résolution ε) + existence d’observables stables.
- **Viable-III (niveau III, preview)** : existence d’observateurs internes (sous-systèmes informationnels) et description opérationnelle quantique.
- **Viable-IV (Niveau IV, preview)** : phase quasi-lisse donnant une limite (M,g) avec dynamique effective compatible GR.

Ainsi, I.D ne demande pas "observateurs" comme critère *de base* : c’est une cible ultérieure.

## D2.2 — Conjecture de complexité minimale

**Énoncé** : dans un univers viable-I, il existe au moins quelques "familles" de comportements dynamiques distincts (types émergents à résolution ε), de sorte que le système ne se réduit pas à un seul régime.

## D2.3 — Conjectures géométriques

- **Dimension effective** : existence d’une dimension spectrale/locale stable, éventuellement proche de 4 dans une phase quasi-lisse.
- **Signature** : compatibilité de la structure causale avec une direction temporelle privilégiée (au sens causal), et isotropies transverses.

> À ce stade : ce sont des objectifs de simulation (D3), pas des résultats.

## D2.4 — Conjecture de "phase structurée"

Il existe des régions du paramètre (𝓡,K,β,Λ) où :

- les observables de structure (dimension effective, courbure discrète, distributions locales) se stabilisent ;
- les corrélations présentent une longueur caractéristique non triviale ;
- la dynamique n’est ni absorbée (blocage) ni totalement "mélangée" (désordre sans structure).

---

# D3 — Programme de recherche

## D3.1 — Objectifs

1. **Cartographier** l’espace (𝓡,K,β,Λ) : quelles phases, quelles transitions ?
2. **Tester** les conjectures du Niveau I (persistance, stabilité d’observables, existence de phases structurées).
3. **Produire** des "benchmarks" reproductibles : mêmes règles, mêmes métriques, mêmes scripts.

## D3.2 — Simulations numériques (Niveau I)

### Pipeline minimal

1. Choisir un petit catalogue 𝓡 (2–10 règles) + un coût K local.
2. Fixer un cutoff Λ (taille max, énergie max, profondeur max, etc.).
3. Générer des histoires longues (ou un ensemble d’histoires) via la dynamique pondérée.
4. Mesurer :
   - P_block, ⟨τ_block⟩,
   - diversité de motifs/types émergents à résolution ε,
   - observables de structure (dimension effective, courbure discrète, distributions locales),
   - indicateurs de mélange (temps de relaxation, autocorrélations).

### Tests "critiques" (au bon niveau)

- **Test A — Existence de phases** : observe-t-on des régimes stables séparés par des transitions ?
- **Test B — Robustesse** : les observables de phase changent-elles sous perturbations finies de l’histoire ?
- **Test C — Universalité** : différentes règles donnent-elles les *mêmes* exposants/lois à grande échelle ?

## D3.3 — Sélection de règles (interface avec niveau II)

Le Niveau I ne sélectionne pas 𝓡 ; mais il peut :
- définir des critères (localité, réversibilité partielle, richesse de motifs, absence d’absorbants dominants),
- et produire une banque de règles candidates.

## D3.4 — Preview (niveau IV) : signatures observationnelles

Cette partie est volontairement hors niveau I ; elle sert de feuille de route.

Exemples de cibles possibles (à reformuler proprement une fois un modèle effectif obtenu) :
- constante cosmologique effective,
- spectre de fluctuations primordiales,
- éventuelles violations de Lorentz / dispersion modifiée,
- signatures de granularité (bruit, corrélations).

> Tant qu’on n’a pas un passage contrôlé vers une théorie effective (niveau IV), ces items doivent rester au statut "preview".

---

# D4 — Transition vers le niveau II

## D4.1 — Limitations du Niveau I

Le niveau I ne peut pas, à lui seul :

1. sélectionner 𝓡 (et donc la "dynamique réelle") ;
2. fixer β (ou sa loi d’évolution) ;
3. expliquer pourquoi *certaines* histoires (ou phases) sont "typiques" du point de vue d’un observateur interne ;
4. dériver une théorie opérationnelle optimale (quantique) pour un observateur interne ;
5. dériver une dynamique géométrique effective (type Einstein) sans hypothèse supplémentaire.

## D4.2 — Introduction du Principe S (énoncé préliminaire)

Le Principe S est introduit comme un principe de sélection informationnelle sur l’espace des histoires :

- il privilégie des mesures sur Ω qui réalisent un compromis entre
  - complexité (coût de description / Kolmogorov / ressources),
  - et entropie (multiplicité des réalisations / robustesse statistique).

Le contenu exact (fonctionnelle, invariances, contraintes) appartient au niveau II.

## D4.3 — Attendus (préviews)

Ce que le Principe S *devrait* permettre, si cohérent :

- **Niveau II** : sélectionner des mesures privilégiées et des phases typiques ;
- **Niveau III** : reconstruire une description opérationnelle finie-dimensionnelle de type quantique (Hilbert/Born comme optimum informationnel) ;
- **Niveau IV** : dans une phase quasi-lisse, obtenir une dynamique effective de la géométrie (type Einstein) avec constantes comme invariants de phase.

---

# Récapitulatif du niveau I

## Architecture complète

- **I.A** : axiomes (substrat, règles, causalité, Ω + mesure)
- **I.B** : dynamique interne (Read/Write, fréquences, stationnarité sous hypothèses)
- **I.C** : émergence (observables, coarse-graining intrinsèque, phases ; previews vers III–IV)
- **I.D** : taxonomie + conjectures + programme + transition vers S

## Message final du niveau I

Le Niveau I produit une architecture mathématique cohérente pour parler d’un "vide pré-géométrique" comme espace d’histoires combinatoires.  
Ce qui manque n’est pas un "détail technique" mais un principe de sélection : sans lui, on a un multi-ensemble d’univers possibles ; avec lui, on espère obtenir des univers *typiques* et des lois effectives.

---

## Notations (rappel)

- H : configuration (hypergraphe étiqueté)
- 𝓡 : catalogue de règles
- e : événement élémentaire
- Read/Write : dépendances causales
- ≺ : précédence causale
- Ω : espace des histoires
- μ_{β,Λ} : mesure/pondération (souvent définie sur cylindres, avec cutoff Λ)
- K : coût combinatoire
- β : paramètre de compromis coût/entropie (hyperparamètre avant sélection)

