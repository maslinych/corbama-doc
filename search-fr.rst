Corpus bambara de référence
Guide d’utilisation


L’interface de recherche
================

L’interface de recherche du Corpus bambara de référence se trouve en accès libre à l’adresse suivante : http://theschool.spb.ru/bonito/run.cgi/first_form

En haut, se trouvent trois options principales pour la recherche : Corpus, Query Type, Query.

Les sous-corpus
==========

L’option Corpus permet le choix entre trois sous-corpus (plus précisément, il s’agit de deux sous-corpus, dont l’un permet deux types de recherche) :

**corbama-brut**
Il s'agit d'un sous-corpus non-désambiguïsé (à la fin juillet 2012, il comportait environ 1.100.000 mots).

Le sous-corpus corbama-brut est plus volumineux que l’autre sous-corpus (corbama-net), et permet de trouver un nombre beaucoup plus élevé d’exemples, mais sa sélection est incomparablement moins raffinée : il ne faut pas oublier que l’analyseur morphologique automatique de texte bambara produit des analyses multiples pour environ 70% de tous les mots. En fait, une recherche dans ce sous-corpus produit à peu près le même résultat qu’une recherche dans Word, avec les avantages d'une plus grande vitesse, d'une présentation plus confortable des résultats sous forme de concordance, et la possibilité de sauvegarde des résultats dans différents formats.

**corbama-net-non-tonal**
Il s'agit d'un sous-corpus désambiguïsé (à la fin juillet 2012, environ 38.000 mots) dont la recherche ne tient pas compte des tons.

La recherche dans ce sous-corpus produit un résultat plus raffiné, elle peut être beaucoup plus nuancée grâce aux paramètres supplémentaires.

Note :
Il faut tenir compte du fait que la création du sous-corpus désambiguïsé est un travail en cours ; on trouvera dans ce sous-corpus un certain nombre d’erreurs et d’inconséquences. Le groupe de travail du Corpus bambara de référence s’occupe de leur identification et élimination. Prière d’informer Valentin Vydrin, vydrine@gmail.com, des erreurs relevées.

**corbama-net-tonal**
C’est un sous-corpus désambiguïsé (identique au précédent) dont la recherche tient compte des tons.

Ce type de recherche est encore plus raffiné, elle exclue les quasi-homonymes se distinguant de la forme voulue par les tons.

Cf. également : :doc:‘Règles de la notation tonale dans le Corpus <tonal-orthography-fr>`.

L’étiquetage
=========

Tous les textes sont subdivisés en tokens. Un **Token** est un mot ou un signe de ponctuation. Chaque mot et chaque morphème à l’intérieur du mot est doté d’un étiquetage linguistique.

Chaque sous-corpus comporte l’étiquetage linguistique suivant :

1. **Mot-forme** en orthographe bambara de 1982.

Dans le cas où l’orthographe originale du texte est différente, le logiciel de recherche renvoie les exemples dans cette orthographe ; cependant, la base des données contient également la forme convertie dans la nouvelle orthographe, qui est disponible en cas de besoin (voir la subdivision :ref:`View Options <view_options>`).

Cf. également : :doc:`L’approche du groupe de travail du Corpus bambara de référence à la normalisation de l’orthographe dans le Corpus <orthography-fr>`

2. **Lemme** (ou la liste des lemmes) est la forme canonique par rapport au mot-forme.

Les lemmes sont des formes de mots sans flexions. Les mots dérivés lexicalisés et les mots composés dont la formation s’accompagne d’une lexicalisation (autrement dit, les mots dérivés et composés figurant dans la base lexicale des données Bamadaba comme des lexèmes) sont considérés comme des lemmes.

Dans le sous-corpus corbamba-net-tonal, le lemme comporte une marque tonale (cela veut dire qu’une recherche « par lemme » sans indication de marque tonale ne permet pas de trouver le mot). Dans les sous-corpus non-tonaux (corbama-brut, corbama-net-non-tonal) le lemme n’a pas de marque tonale ; par conséquence, lors de la recherche par lemme, il ne faut pas indiquer le ton (sinon, la marque tonale empêcherait la recherche). 

Si un lexème a plus d’une variante tonale, et que ces variantes sont représentées dans la base lexicale Bamadaba, une recherche par chacune de ces variantes permet de trouver les exemples où ce lexème apparaît dans toutes ses variantes phonétiques en question.

3. **Étiquette de partie de discours** (cf. :doc:`La liste des étiquettes des parties des discours du Corpus bambara de référence <pos-tags-fr>`).

En cas d’ambiguïté, les étiquettes admissibles sont présentées séparées par ``|``, ex. : n|adj.

4. **Glose** est une traduction standardisée en français.

A l’origine de la base lexicale Bamadaba se trouve le dictionnaire bambara-français de Charles Bailleul. Cependant, ce dictionnaire a subi une adaptation considérable en tenant compte des besoins du Corpus. En particulier, on a attribué à chaque lexème une glose « canonique » française. Pour les lexèmes polysémiques, un sens le plus prototypique a été choisi (ce qui n’était pas toujours facile ; il se peut que certains choix apparaissent comme insuffisants, ils seront modifiés plus tard). Certains gloses sont représentées par deux mots français (ou plus) séparés par des points (sans espaces), ex. : ɲɛ̀ɲɛ ‘brisure.de.céréales’, ntòmo ‘fétiche.des.garçons’. Pour les noms des espèces biologiques (surtout celles n’ayant pas des noms français établis), la glose comporte le nom latin précédé par un mot désignant l’appartenance générique, ex. : ɲénu ‘arbre.Hannoa.undulata’, ntómi ‘serpent.Eryx.muelleri’.

Cf. également : :doc:`Gloses standards pour les affixes et les mots auxiliaires en bambara <standard-glosses-fr>`

Types de recherche
===========

L’option Query type (qui peut être choisie par un clic sur l’inscription Query type dans le menu à la gauche) offre les types de recherche suivants :

**Simple**
Recherche par une racine qui peut être identique à un mot-forme ou faire partie d’un mot-forme comportant des affixes flexionnels ou d’un mot dérivé ou composé; par un mot-forme.

**Lemma**
Recherche par un lemme (y compris incorporé dans un lexème dérivé ou composé). Lors d’une recherche “Lemma”, à la différence de la recherche “Simple”, on ne trouvera pas des mots-formes où la séquence en question ne représente pas une seule racine. Ainsi, la recherche “Simple” pour sara donne, parmi d'autres, la forme perfective du verbe sà ‘mourir’ (avec le suffixe –ra), tandis que cette forme n’est pas représentée dans la sélection par la recherche “Lemma”. Ce type de recherche n’est pertinent que pour le sous-corpus désambiguïsé, tandis que son résultat pour le sous-corpus non-désambiguïsé serait le même que celui de la recherche “Simple”.

**Phrase**
C’est une recherche par une séquence des mots-formes séparés par des espaces (en fait, une recherche par un seul mot-forme est possible également, son résultat serait identique à celui de la recherche “Simple”). Ce type de recherche est pertinent pour tous les sous-corpus.


**Word Form**
C’est une recherche par un mot-forme. A la différence de la recherche “Simple”, cette recherche ne sélectionne pas les phrases où la racine représentée par la séquence en question comporte des affixes ou fait partie des mots dérivés ou composés. Ainsi, si on cherche mɔgɔ, on ne trouverait pas les formes mɔgɔw, dugukɔnɔmɔgɔw, etc. Néanmoins, on trouvera des mots-formes avec une structure morphologique complexe (ainsi, en cherchant la “Word form” sara, on trouverait, parmi les autres, la forme sara du perfectif du verbe sà). Autrement dit, ce type de recherche est analogue à la recherche dans Word avec l’option « Mot entier », ou une recherche d’un mot entre guillemets sur Internet.

**Character**
C’est une recherche par une séquence des symboles (non-séparés par des espaces) qui peut ne pas être identique à un morphème (une racine ou un affixe) bambara quelconque.

**CQL**
C’est une recherche par tous les paramètres disponibles des mots-formes, mais aussi par des combinaisons de ces paramètres. C’est un type de recherche flexible dont les questions sont formulées dans une langue artificielle `Corpus Query Language (CQL) <https://trac.sketchengine.co.uk/wiki/SkE/CorpusQuerying>`_ 

Lorsqu’on choisit le type de recherche CQL, une fenêtre Default attribute apparaît automatiquement. Cette fenêtre comporte les options Word, Lemma, Tag, Gloss. 

L’introduction de la forme à rechercher
==================

Tous les types de recherche, sauf CQL, supposent une introduction de la forme à rechercher dans la fenêtre Query. Après cela, il faut appuyer sur la touche Enter ou cliquer la touche Make Concordance (en bas de l’écran), et le logiciel créera la concordance.

Pour la recherche dans **corbama-brut** ou **corbama-net-non-tonal**, les formes recherchées ne doivent pas avoir des marques tonales. Pour la recherche dans **corbama-net-tonal**, la forme recherchée peut être soit tonale :doc: ‘<tonal-orthography-fr>`, soit non-tonale.

Pour une recherche du type CQL, la forme recherchée est mise entre guillemets: ``"kuma"``, ``"dòn"``, ``"pp"``, ``"serpent"``, etc.

Une recherche combinée est effectuée par plusieurs attributs d’un lexème à la fois, ce qui permet de nuancer au maximum la recherche et d’obtenir une sélection très pointue. Lors de cette recherche, l’option indiquée dans la fenêtre Default attribute n’est pas pertinente (parce que les mêmes options sont indiquées dans la fenêtre CQL manuellement). La commande introduite dans la fenêtre CQL a le syntaxe suivante (ce qui se trouve entre chaque paire des crochets correspond à un token) :

  [option1="n1" espace & espace option1="n2"]

(n1, n2 correspondent à des séquences recherchées).

Par exemple, si on veut trouver tous les emplois du mot kuma avec une étiquette de partie de discours « verbe » (v), la question est formulée comme suit :

  [word="kuma" & tag="v"]

Une recherche par trois (ou plus) paramètres à la fois est également possible (même si cela ne donne pas souvent grand chose par rapport à une recherche par deux paramètres), ex. :
    
  [word="kɔnɔ" & tag="n" & gloss="oiseau"]

Évidemment, une recherche combinée n’est pertinente que dans le sous-corpus désambiguïsé.

Une recherche combinée est possible, dans le cadre de CQL, pour des expressions à plusieurs mots. Dans ce but, chaque mot (plus précisement, chaque token) doit être mis entre crochets, et les tokens doivent être séparés par des espaces. Ex. :
    
  [word="bara" & gloss="calebasse"] [word="kɔnɔ" & gloss="à.l’intérieur"]

Cette recherche permet de trouver toutes les combinaisons bàra kɔ́nɔ où le promier mot est ‘calebasse’ (plutôt que ‘chez’, ‘dancing’, ‘préféré’), et le deuxième mot est la postposition inessive (plutôt qu’‘attendre’, ‘bouton.de.fleur’, ‘oiseau’, ‘ventre’).

Le régime CQL permet une recherche par modèle grammatical, ce qui peut être utile pour des études syntaxiques. Prenons le modèle suivant :
    
  [tag="adv"] [tag="v"]

Cette recherche devrait sélectionner toutes les occurrences des adverbes préverbaux. Et si cela ne produit pas de résultat voulu, cela révèle soit la rareté des adverbes préverbaux, soit les erreurs des opérateurs de désambiguïsation (ce qui est plus probable).

Le régime CQL permet de trouver des formes redoublées (absentes de la base lexicale Bamadaba). Pour trouver tous les verbes redoublés, il faut introduire la commande suivante :
    
    1:[tag="v"] 2:[tag="v"] & 1.word = 2.word
    
    Et tous les mots redoublés du Corpus peuvent être trouvés par la commande suivante :
    
    1:[] 2:[] & 1.word = 2.word

Introduction des symboles non-standards
~~~~~~~~~~~~~~~~~~~~~~~~~~~

L’introduction de symboles non-standards(ɔ, ɛ, ŋ, ɲ, les signes diacritiques pour les tons) est possible de deux façons alternatives :

1) Par le moyen des jeux de caractères spéciaux (on peut même utiliser le clavier français standard pour les symboles à, è, é, ù…, cependant, ce clavier est insuffisant pour beaucoup d’autres symboles) ;
2) Les symboles non-standards peuvent être remplacés par les combinaisons suivantes :

    ;o = ɔ
    ;e = ɛ
    ;n = ŋ
    ;m = ɲ

L’accent aigu (la marque du ton haut) est remplacé par une virgule après une voyelle, et l’accent grave (la marque du ton bas) est remplacé par l’apostrophe inverse suivant la voyelle. Ex. :

    k;o, -> kɔ́
    su` -> sù
    k;e,n;e -> kɛ́nɛ
    ;m;o` -> ɲɔ̀
    ;n;o`mi -> ŋɔ̀mi

L’option Context
=============

Cette option permet d’effectuer une recherche de la co-occurrence des formes séparées par d’autres formes. Elle est activée (ou désactivée) par un clic sur le mot Context dans le menu à la gauche.

Le mot de référence (par rapport auquel le contexte est indiqué) est introduit dans la fenêtre Query.

La forme déterminant le contexte voulu (donc la forme dont les combinaisons avec le mot de référence doivent être recherchées) est introduite dans Lemma filter. On peut y donner plus d’une forme.

Dans les fenêtres de Lemma filter, on peut indiquer quel est le contexte qui nous intéresse (left, right, both – dans ce dernier cas, à la fois les contextes droit et gauche sont mis en compte). L’option à droite permet d’indiquer la longueur du contexte, de 1 à 15 mots-formes. Si cette longueur est définie à 1, seules les formes adjacentes à la forme de référence seront trouvées (donc le résultat sera le même que pour la recherche du type Phrase). Si la longueur du contexte est 2, on trouvera des cas où les formes contextuelles sont adjacentes à la forme de référence ou séparées par une autre forme, etc. (il faut préciser qu’on trouvera également les cas où la forme contextuelle est séparée de la forme de référence par la limite de la proposition).

A la gauche de la fenêtre Lemma, on trouvera une autre fenêtre contenant les options All, Any, None. 

En sélectionnant l’option All, et en indiquant à même temps deux (ou plus) formes contextuelles, on trouvera les exemples où toutes les trois formes (la forme de référence et les deux formes contextuelles) apparaissent. Ainsi, si la forme de référence est kɛ, et les formes contextuelles sont yɛrɛ et ɲɔgɔn, on trouvera (parmi les autres) les exemples suivants :

Mɔgɔ min bɛ a mɔgɔɲɔgɔn jogin , a ye min kɛ o tigi la , o **ɲɔgɔn** ka **kɛ** a **yɛrɛ** fana la .
|    O de bɛ cikɛla kɛ senyɛrɛkɔrɔbaga ye , i n' a fɔ birokɔnɔbaarakɛla ; i n' a fɔ taɲini julabaw , i n' a fɔ **yɛrɛ** jamanakuntigi n' a **kokɛɲɔgɔnw** , senyɛrɛkɔrɔ siratɛgɛ la 
|    **Jatigikɛ** **yɛrɛ** ɲuman na , a **ɲɔgɔn** cɛ kisɛ t' ale denw na .
etc.

Cette recherche peut être efficace (parmi d'autres) pour une étude de la possibilité de l’emploi des verbes transitifs avec les marques prédicatives (ce qui peut être important, par exemple, pour l’analyse des Aktionsarte), de la combinaison des verbes avec les postpositions, etc.

En sélectionnant la fonction Any, on trouvera tous les cas où kɛ apparaît avec au moins une des formes contextuelles (y compris, bien évidemment, les cas où toutes les trois formes co-occurrent).

Avec l’option None, toutes les occurrences du mot de référence sont sélectionnées avec les contextes où les formes contextuelles en question sont **absentes**. Cette option peut être utile là où une forme apparaît le plus souvent dans le cadre de certains expressions figées, tandis que l’utilisateur veut trouver ses utilisations en dehors de ces expressions.

Text types
==========

Par défaut, le logiciel fait la recherche dans le sous-corpus entier. Dans la division Text types, on peut limiter la liste des textes dans lesquels on veut effectuer la recherche. L’option peut être activée par un clic sur Text types dans le menu à gauche.

La première fenêtre, doc.id, permet indiquer le texte particulier qu’on veut inclure dans le sous-corpus individuel. Si on commence à taper le nom de l’auteur ou le premier mot du titre de l’ouvrage, et si ce texte existe dans le corpus, le nom du fichier apparaît dans l’invite flottante.

Plus bas, on trouve la fenêtre doc.text_genre où on peut indiquer les restrictions par genres de textes.

Il est prévu d’introduire d’autres paramètres pour la création des sous-corpus.

Concordance
===========

Un résultat non-négatif d'une recherche dans le sous-corpus est une concordance, c.-à-d. une liste d’exemples (et leurs contextes) trouvés dans le sous-corpus. Le Corpus bambara de référence n’a pas de limite en ce qui concerne le nombre d’exemples fournis à l’utilisateur. Dans la bande blanche en haut de l’écran, on trouvera l’indication du nombre d’exemples trouvés (Hits). Au-dessous de cette bande, le nombre de pages de la concordance est indiquée (dans le cas où le nombre d’exemples est supérieur à 20; par défaut, le nombre d’exemples par page est égal à 20). On y trouvera également les touches de navigation dans la concordance.

Pour chaque exemple, le nom du fichier est indiqué (où le nom de l’auteur et le titre du texte sont présenté d’une façon suffisamment transparente; cf. :doc:`les principes de la nomination des fichiers <file-naming-ru>`.

La concordance obtenue peut être sauvegardée, en partie ou entièrement, dans le format texte. Pour la sauvegarder intégralement, on choisit l’option Save dans le menu à gauche.

Pour régler la présentation de la concordance, on utilise deux options du menu : KWIC/Sentence et View Options.

En cliquant sur KWIC/Sentence, on change le régime de présentation des exemples : sous « Sentence », des propositions entières sont montrées (« d’un point à l’autre »), et sous le régime KWIC, le contexte droit et gauche d’une longueur déterminé sont montrés (par défaut, 40 caractères à gauche et 40 caractères à droit).

.. _view_options:

L’option View Options permet de régler la présentation de la Concordance d’une façon plus nuancée. On peut, en particulier :

* modifier les attributs de la forme (Attributes). Si on coche les options word, lemma, tag ou gloss, les attributs en question (le lemme, la partie de discours, la glose française) sont montrés (par défaut, l’option « word » est toujours cochée).

* préciser si les attributs en question doivent être montrés pour chaque mot de chaque exemple ou pour le mot recherché seulement (la zone Display Attributes).

Notons que présentement, tous les attributs de la forme sont présentés sous forme linéaire, séparés par une barre verticale. Cette présentation s’avère plutôt encombrante pour le sous-corpus non-désambiguïsé (corbama.brut), car les attributs sont montrés pour chaque variante de l’analyse du mot, et les variantes peuvent être assez nombreuses. Elle est surtout difficile à gérer sous le régime de l’affichage des attributs de chaque mot (Display attributes – For each token). Apparemment, cette option ne peut être récommandée que pour le sous-corpus désambiguïsé.

Plus bas dans l’interface, on trouve les options permettant
 
*le paramètre du nombre d’exemples par page de la concordance (Page size; le nombre par défaut est 20);

*la taille des contextes gauche et droit (KWIC Context size; en principe, le contexte peut être agrandi jusqu’à l’infini; par défaut, la dimension donnée est de 40 caractères).

Les autres fonctions de la zone View Options (Sort good dictionary examples etc.) ne sont pas pertinentes pour notre Corpus.

Sorting

Le tri des exemples est réglé dans la zone Sorting. Les exemples peuvent être rangés par ordre alphabétique de la forme se trouvant à droite de la forme recherchée (Right context) ou à gauche (Left context) ; la distinction entre les lettres majuscules et minuscules peut être ou ne pas être prise en compte (Ignore case). Ils peuvent être rangés par ordre alphabétique inverse (Backward). L’activation des paramètres choisis est effectuée en cliquant sur la touche Sort Concordance.

Le tri à plusieurs niveaux n’est pas pertinent pour notre Corpus pour le moment.

Le menu principal comporte également les options Sorting – References (tri par noms des fichiers comportant les exemples de la concordance) et Sorting – Shuffle (brassage des exemples, de façon à lister les exemples au hasard).

L’option Sample permet de produire un échantillon aléatoire (parmi tous les exemples trouvés dans le corpus).

L’option Filter est analogue, par ses fonctions, à l’option Context, cf. la division 4.

L’option Frequency donne l’accès à la statistique des mots-formes comportant l’élément en question, et la statistique de ses combinaisons avec les éléments voisins.

L’interface de cette option comporte deux zones.

1. Multilevel frequency distribution. Pour chaque niveau hiérarchique du tri, on peut choisir entre :

*Node, ce qui permet de calculer le nombre des mots-formes comportant l’élément en question (en cochant l’option Ignore case, on ne fera pas la distinction entre les lettres majuscules et minuscules);

*les éléments du contexte gauche (1L, 2L, 3L…, en fonction de la dimension du contexte) ou du contexte droit (1R, 2R, 3R…). Dans ce dernier cas, on obtient la fréquence de la co-occurrence avec les formes à gauche et à droit.

A même temps, on peut définir les attributs de l’élément de référence et l’élément contextuel : word, lemma, tag, gloss. Notons qu’un calcul des fréquences du mot de référence dans le sous-corpus non-désambiguïsé par les paramètres lemma, tag, gloss n’est pas pertinent.

2. La zone Text Type frequency distribution permet de définir la fréquence de l’élément recherché dans :

* des fichiers spécifiques, l’option doc.id;

* des textes spécifiques (notons qu’un seul texte peut être représenté dans le Corpus par plusieurs fichiers), l’option doc.text_title;

* des textes des genres différents, l’option doc.text_genre.

Collocation

La section Collocations permet de trouver des candidats aux collocations du mot recherché avec d’autres mots. La recherche est possible par les attributs (Attribute) des mots voisins (word, lemma, tag, gloss). On peut nuancer la recherche en indiquant s’il faut tenir compte du contexte à gauche (In the range from -1, -2, etc.) ou à droite (… to 1, 2, etc.); les chiffres correspondent à la dimension du contexte pris en compte (-1/1: seuls les mots contigus sont pris en compte; -2/2: le mot adjacent et le mot qui le suit/précède sont pris en compte, etc.).

En appuyant sur la touche Make Candidate List, on obtient la liste des candidats aux collocations. En cliquant sur l’étiquette bleue Frec., ils seront rangés par ordre décroissant de fréquence.

Word List
=========

L’option Word List permet de créer un dictionnaire de fréquence. En entrant dans cette option, on peut choisir entre les étiquettes All words, All lemmas. En cliquant sur ces étiquettes, on obtient une liste de fréquences de tous les tokens du sous-corpus (en ordre de décroissance). Les signes de ponctuations (étant des tokens du Corpus) se trouveront dans cette liste aussi.

