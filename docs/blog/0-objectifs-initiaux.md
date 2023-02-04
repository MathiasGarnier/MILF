# 0 - Objectifs initiaux

Il est relativement compliqué d'avoir une idée (rien qu'un peu) précise de ce que je souhaite faire. Découvrant à peine ce nouveau monde (design de compilateurs, formalisation, programmation (très) bas niveau...), il est difficile de savoir exactement par où commencer et surtout où aller !

Pour donner une idée, voici une liste (à la volée) de termes que je vois passer mais dont je n'ai aucune idée du sens qu'ils possèdent / de leur fonctionnement / définition / utilisation précise : Turing-complet, machine de Turing, logique du premier ordre (etc), théorie des types, CPU, RAM, (accélération) GPU, lambda calculus, complexité, preuve, registre, circuit imprimé, sémantique, grammaire...

Même si le vocabulaire manque, essayons tout de même de décrire ce que je souhaite faire (au moins sommairement dans un premier temps).

## Une première idée

Prenons l'exemple de [Lean](https://leanprover.github.io/). C'est un assistant de preuve. Concrètement, il prend en entrée un jeu de données (chaîne de caractère ayant un sens dans un langage précis) qu'il va être capable "d'évaluer" puis de "traiter". Une fois fait, son utilité réside notamment dans le fait de "certifier" de la justesse de la preuve ! (Lean est même incroyablement plus fort que cela en permettant diverses automatisations...)

Essentiellement, Lean est un langage écrit en C++ (cf. [github](https://github.com/leanprover-community/lean)). Comme exemple d'utilisation, un utilisateur programmerait en Lean sur VSCode sur Windows / Linux / McIntosh... Avant que le processeur soit sollicité beaucoup d'intermédiaires vont s'interposer (même si ce sera un temps relativement court). Assez bêtement, je me suis demandé s'il ne serait pas possible d'écrire un langage (au plus proche du processeur) opérant dans une logique similaire à celle de Lean. Néanmoins, ne pourrait-on pas aller plus loin ?

Dans quelle direction aller ? Pour tenter de m'expliquer un petit peu, je vais faire une _explication détournée_ : semblerait-il que tous les langages assembleurs possèdent une instruction ```add``` (et plus généralement celles de l'arithmétique (binaire ou pas) de base). Fondamentalement, si je ne suis pas trop dans l'erreur, dans un assistant de preuve, on ne va _jamais_ "prouver" que _"deux et deux font quatre"_. En revanche, on va prouver que la manière de faire l'addition implique qu'en raisonnant sur un certain alphabet / langage (définit arbitrairement; les nombres usuels par exemple) conduira à obtenir des équivalences / égalités purement numériques (2 + 2 = 4).
Mon idée serait de baser le langage non sur des instructions au processeurs usuelles mais de "détourner" le fonctionnement habituel d'un ordinateur pour "raisonner" sur des données "symboliques" et non sur des opérations arithmétiques brutes. (Comment définir alors un tel objet ? Est-ce seulement possible ? A-ce seulement un sens ?)

Dit autrement, l'idée est de calquer la vérification et la formalisation de preuve sur l'architecture même d'un processeur (tout en ayant un petit peu _bidouillé_ le "fonctionnement originel").

On m'a parlé de VHDL et Verilog (wow). À voir bien plus tard.

## Une idée du travail (quelques tâches à accomplir)

Je suis théoriquement parti pour... longtemps. Dans l'optique d'un déroulement pas trop chaotique du projet, je suis censé réaliser bon nombres de prototypes (qui, dans leur ordre de réalisation, ne correspondent aucunement à une quelconque priorisation des objectifs).

Pour l'instant (et depuis ma prime adolescence), je me passionne pour le design de compilateur. Il ne m'aura fallu que cinq / six années pour me lancer... [Ben](https://github.com/lngns/) m'a fait découvrir beaucoup de choses et continue à m'en faire découvrir beaucoup. Aujourd'hui, et c'est l'occasion d'un des prochains billets, j'ai mon petit compilateur _source-to-source_ et c'est un heureux début... 

### Le temps des compilateurs

Honnêtement, c'est la jungle. Ça part dans tous les sens, faire un truc propre est loin d'être trivial.

### Le temps du fonctionnement système


### Le temps des performances et cette idée qui m'échappe : l'optimisation


### Un niveau en dessous

Au fond, le C est très haut niveau ().

### Le temps des cathédrales

==> l'architecture / électrocinétique et cie


### Mastering Lean


### Le formalean-inator !

Il va bien falloir que j'apprenne à manier un assistant de preuve un jour ou l'autre ! Ce serait bien de le faire avec un bon petit projet en tête (par exemple celui du second semestre : formaliser "entièrement" la preuve du résultat que l'on devra montrer; n'ayant pas encore le sujet, je ne sais pas vraiment ce qu'il en retourne).

Le choix de Lean est purement subjectif mais divers points renforcent cette décision : une communauté débordante et active (par exemple [sur leur forum](https://leanprover.zulipchat.com/)), une sacrée documentation (sur leurs sites : [microsoft](https://leanprover.github.io/) ou [communautaire](https://leanprover-community.github.io/); ou directement sur [github](https://github.com/leanprover-community)).

Dans un second temps, écrire un micro-lean (un premier assistant de preuve) serait simplement merveilleux.


### Beaucoup de mathématiques et d'informatique théorique

En parallèle de chacune de ces étapes, il va falloir se documenter sur les bases mathématiques / informatiques de chacun des objets.


## Ne pas abandonner

Il faut tenir bon et ne pas baisser les bras. Adoptons la [philosophie Vulkan](https://vulkan-tutorial.com/Introduction) :
> It's also important to keep in mind that once you have that boring looking triangle, drawing fully textured 3D models does not take that much extra work, and each step beyond that point is much more rewarding.

Au travail, il ne faut pas se décourager (surtout pas au début) !
