# 2 - Premier compilateur miniature


    LET x = 0

    FUNCTION(STRING) mafonction (NUMBER i, STRING s, NUMBER j) DO
        PRINT i * 2
        RETURN s
    ENDFUNCTION


    FUNCTION(NUMBER) mafonction2 (NUMBER l, STRING k, NUMBER m) DO
        PRINT l * 2
        RETURN l
    ENDFUNCTION


Yeahhh, ça compile (ou plutôt transpile...). Il ne se passe pas grand chose mais c'est mon [premier (grand) pas](https://github.com/MathiasGarnier/Algorithms-All---Old/blob/master/tinyCompiler.py). C'est aussi la première fois que j'avoisine les mille lignes de code (cela m'a permis de me rendre compte que quand j'étais petit je voulais faire des projets inutilement longs et désormais : plus c'est court et bien pensé, mieux ce sera).

J'ai suivi un magnifique petit tutoriel de [Austin Z. Henley](https://austinhenley.com/index.html) qui se décomposait en trois parties : [*le lexer*](https://austinhenley.com/blog/teenytinycompiler1.html), [*le parser*](https://austinhenley.com/blog/teenytinycompiler2.html) et [*l'emitter*](https://austinhenley.com/blog/teenytinycompiler3.html). J'ai pu un petit peu parlé avec lui, et, il m'a notifié la sortie (imminente) d'un livre de sa confection sur le sujet (yeahhh). Une fois fini, il invite à aller plus loin (en implémentant la notion de `FUNCTION` par exemple). Il reste pas mal de choses à faire mais je crois avoir compris la logique. Essayons de la résumer :

## Fonctionnement (naïf) d'un compilateur

On oublie les histoires d'optimisation etc... On ne se concentre que sur le fonctionnement "primitif" / intrinsèque.

## Quelques sources

Austin Henley a conseillé ce livre : [Crafting Interpreters](https://craftinginterpreters.com/) de Robert Nystrom. Il est juste magnifique !!! (Et accessible [en ligne](https://craftinginterpreters.com/contents.html).) Je suis quasiment convaincu que je vais le lire. Il faudrait aussi lire le [Dragon Book](https://suif.stanford.edu/dragonbook/) (au moins pour la culture, une réédition semble avoir été faite).