<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/mathjax@2/MathJax.js">
</script>


# 0 - Objectifs initiaux

Il est relativement compliqué d'avoir une idée (rien qu'un peu) précise de ce que je souhaite faire. Découvrant à peine ce nouveau monde (design de compilateurs, formalisation, programmation (très) bas niveau...), il est difficile de savoir exactement par où commencer et surtout où aller !

Pour donner une idée, voici une liste (à la volée) de termes que je vois passer mais dont je n'ai aucune idée du sens qu'ils possèdent / de leur fonctionnement / définition / utilisation précise : Turing-complet, machine de Turing, logique du premier ordre (etc), théorie des types, CPU, RAM, (accélération) GPU, lambda calculus, complexité, preuve, registre, circuit imprimé, sémantique, grammaire...

Même si le vocabulaire manque, essayons tout de même de décrire ce que je souhaite faire (au moins sommairement dans un premier temps).

## Une première idée

Prenons l'exemple de [Lean](https://leanprover.github.io/). C'est un assistant de preuve. Concrètement, il prend en entrée un jeu de données (chaîne de caractère ayant un sens dans un langage précis) qu'il va être capable "d'évaluer" puis de "traiter". Une fois fait, son utilité réside notamment dans le fait de "certifier" de la justesse de la preuve ! (Lean est même incroyablement plus fort que cela en permettant diverses automatisations...)

Essentiellement, Lean est un langage écrit en C++ (cf. [github](https://github.com/leanprover-community/lean)). Comme exemple d'utilisation, un utilisateur programmerait en Lean sur VSCode sur Windows / Linux / McIntosh... Avant que le processeur soit sollicité beaucoup d'intermédiaires vont s'interposer (même si ce sera un temps relativement court). Assez bêtement, je me suis demandé s'il ne serait pas possible d'écrire un langage (au plus proche du processeur) opérant dans une logique similaire à celle de Lean. Néanmoins, ne pourrait-on pas aller plus loin ?

Dans quelle direction aller ? Pour tenter de m'expliquer un petit peu, je vais faire une _explication détournée_ : semblerait-il que tous les langages assembleurs possèdent une instruction ```add``` (et plus généralement celles de l'arithmétique (binaire ou pas) de base). Fondamentalement, si je ne suis pas trop dans l'erreur, dans un assistant de preuve, on ne va _jamais_ "prouver" que _"deux et deux font quatre"_. En revanche, on va prouver que la manière de faire l'addition implique qu'en raisonnant sur un certain alphabet / langage (définit arbitrairement; les nombres usuels par exemple) conduira à obtenir des équivalences / égalités purement numériques ($2 + 2 = 4$).
