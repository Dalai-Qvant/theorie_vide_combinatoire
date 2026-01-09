### 1. Résumé

Nous proposons un cadre combinatoire pour la physique fondamentale fondé sur un substrat discret, relationnel, décrit par des hypergraphes dynamiques et des règles locales de réécriture. À ce niveau le plus profond (niveau I), il n’existe ni temps ni espace de fond : seules comptent la structure relationnelle, l’ordre causal émergent et un budget de complexité qui contraint les histoires possibles d’évolution. Un principe de complétude combinatoire impose que tout ce qui n’est pas interdit par les règles se réalise dans au moins une histoire.

Sur cet espace d’histoires, nous introduisons un principe de sélection informationnelle (principe S) qui, au niveau II, définit des mesures privilégiées minimisant un compromis entre complexité et entropie. Les histoires typiques pour ces mesures se regroupent en phases, dans lesquelles émergent des univers macroscopiquement bien définis, dotés d’observateurs internes et d’un temps propre construit à partir de la structure causale.

Au niveau III, nous montrons que la description opérationnelle optimale qu’un observateur interne peut donner de ses expériences, sous des contraintes d’invariance et de cohérence informationnelle, possède la structure d’une théorie quantique finie-dimensionnelle. Les axiomes d’optimalité conduisent à un espace d’états convexe, à une composition de systèmes, à l’apparition d’une structure hilbertienne et à la règle de Born, interprétée comme solution optimale d’un problème de prédiction et de compression de l’information.

Enfin, au niveau IV, nous considérons des phases "quasi-lisses" du graphe causal, qui peuvent être approchées par un espace-temps continu muni d’une métrique lorentzienne. Nous argumentons que l’application du même principe de sélection à la géométrie effective conduit à des équations de type Einstein avec constantes effectives $(G_{\mathrm{eff}}, \Lambda_{\mathrm{eff}})$, interprétées comme invariants de phase du substrat combinatoire. Ce texte ne présente pas encore un modèle unique ni des prédictions numériques, mais propose une architecture conceptuelle cohérente et une feuille de route précise pour une théorie unifiée émergente de la mécanique quantique et de la relativité générale.

------

## 2. Introduction générale

### 2.1. Contexte et motivations

Un siècle après leur naissance, la mécanique quantique et la relativité générale décrivent remarquablement bien des domaines très différents de notre expérience : l’une régit les phénomènes microscopiques et les processus d’information, l’autre la dynamique de l’espace-temps et de la gravitation à grande échelle. Pourtant, ces deux théories fondamentales s’appuient sur des structures conceptuelles difficilement compatibles : espace-temps lisse et dynamique d’un côté, espace-temps fixe et structures d’état abstraites dans un espace de Hilbert de l’autre ; covariance générale versus description par un temps externe global ; champ métrique continu versus opérateurs agissant sur des vecteurs d’état.

De nombreuses approches cherchent à combiner ou dépasser ces cadres : théorie des cordes, gravitation quantique à boucles, programmes de type "causal sets", réseaux de spin, approches informationnelles et opérationnelles de la mécanique quantique, etc. Chacune apporte des idées fortes (discrétisation de l’espace-temps, holographie, rôle de l’information, structures algébriques sous-jacentes), mais aucune ne fournit encore un scénario largement accepté où :

1. la mécanique quantique et la relativité générale apparaissent toutes deux comme des théories effectives émergentes ;
2. à partir d’un substrat plus simple, doté d’une dynamique bien définie et d’une interprétation claire.

Le point de départ de ce travail est le suivant : et si, au lieu de chercher à "quantifier" directement la gravitation ou à "géométriser" la mécanique quantique, on repartait d’un niveau plus profond, où ni l’espace ni le temps, ni même les objets classiques ou quantiques, ne sont encore présents ? Un niveau purement combinatoire et relationnel, où l’on ne parle que de configurations discrètes, de règles locales, de relations causales et de complexité.

Dans un tel cadre, deux idées deviennent centrales :

- l’espace-temps et sa géométrie pourraient émerger comme une description macroscopique d’une phase particulière de ce substrat ;
- la mécanique quantique pourrait émerger non comme une loi fondamentale, mais comme la théorie optimale adoptée par des observateurs internes pour décrire et prédire ce qui leur arrive dans ces univers émergents.

L’objectif de ce livre blanc est de présenter une architecture conceptuelle où ces deux idées sont mises en œuvre de manière cohérente, autour d’un principe de sélection informationnelle commun.

------

### 2.2. Idée directrice : principe S et niveaux d’émergence

La proposition centrale peut se résumer ainsi :

1. Il existe un substrat discret et relationnel décrit par des hypergraphes dynamiques et des règles locales de réécriture. Ce substrat génère un ensemble immense d’"histoires" possibles d’évolution. À ce niveau, il n’y a ni espace-temps continu, ni champs, ni états quantiques : seulement des configurations, des transitions et des dépendances causales.

2. Sur cet espace d’histoires, on introduit un principe de sélection informationnelle, le principe S. Il associe à chaque mesure de probabilité sur les histoires une fonctionnelle de coût combinant :

   - une notion de complexité ou d’"action combinatoire", qui pénalise les univers trop compliqués ou trop irréguliers,
   - une notion d’entropie ou de diversité, qui favorise les ensembles d’histoires riches en possibilités.

   Les mesures qui minimisent ce coût définissent des univers typiques : ce sont eux qui sont "privilégiés" par le principe S.

3. Dans ces univers typiques, il peut exister des observateurs internes : des sous-structures stables, capables d’enregistrer des corrélations, de faire des expériences, de construire des modèles. Ces observateurs ne voient pas le substrat combinatoire brut : ils disposent seulement d’un flux d’événements localement ordonné dans leur propre temps.

4. On peut alors poser une question supplémentaire : quelle est la meilleure théorie qu’un tel observateur peut adopter pour décrire et prédire ses expériences, compte tenu de ses limitations informationnelles et des régularités statistiques imposées par le principe S ? La réponse proposée est : une théorie de type mécanique quantique.

5. Enfin, certaines phases du substrat peuvent présenter, à grande échelle, une structure quasi-lisse qui se laisse approximer par une variété lorentzienne munie d’une métrique. Là encore, le principe S joue le rôle d’un critère d’optimalité : parmi toutes les géométries compatibles avec les données combinatoires, il sélectionne une dynamique effective qui, dans une limite continue, prend la forme d’une équation de type Einstein.

Pour articuler ces idées, nous distinguons quatre niveaux d’émergence :

- Niveau I : substrat combinatoire
  Hypergraphes dynamiques, règles locales, histoires, structure causale, budget de complexité. C’est le niveau ontologique minimal.
- Niveau II : sélection statistique et univers typiques
  Introduction d’une mesure sur les histoires via le principe S ; apparition de phases, d’univers typiques, d’observateurs internes et d’un temps propre.
- Niveau III : mécanique quantique comme théorie optimale
  Reconstructions opérationnelles : à partir des contraintes imposées par le substrat et par l’optimalité informationnelle, les observateurs internes aboutissent à une description de type quantique (espace d’états convexe, structure hilbertienne, règle de Born).
- Niveau IV : espace-temps ébmergent et relativité générale effective
  Dans certaines phases quasi-lisses, la géométrie effective satisfait une équation de type Einstein, avec des constantes physiques interprétées comme des invariants de phase du substrat.

Un schéma conceptuel simple consiste à imaginer :

- une flèche principale
  $\text{substrat (I)} \longrightarrow \text{univers typiques (II)}$
- se dédoublant ensuite en deux branches complémentaires :
  - vers la description interne par les observateurs → niveau III,
  - vers la description géométrique macroscopique → niveau IV.

Les niveaux III et IV ne sont pas indépendants : la structure causale et les corrélations qui sous-tendent la mécanique quantique des observateurs sont elles-mêmes encodées dans la phase géométrique émergente. Le rôle du principe S est de fournir un fil conducteur unique à travers ces différents étages.