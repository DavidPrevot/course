# Python3

#### notebooks / cookies / antivirus

* pour l'accès aux notebooks, mieux documenter la configuration des cookies
* il suffit d'ajouter une exception pour `nbhosting.inria.fr`
  ce n'est pas nécessaire d'ouvrir tout en grand
* mentionner aussi les conflits occasionnellement identifiés avec les antivirus


*************

# Plateforme

* Prévoir des mécanismes plus conviviaux pour échanger le code (miniprojets) - étudier un mini-github
  * MOF, pas évident à mettre en place

* montrer dans une vidéo comment publier du code
  * l'icone '010010' dans la barre de menu
  * Control-K
  * les back quotes `x`
  * 4 espaces
  * parler aussi de la possibilité de publier les notebooks (liens statiques)
  * et donc du point précédent (un site pour exposer le code ?)

# Général

* la mise à disposition au format html
  une idée sans doute intéressante, proposée dans les questionnaires:
  ce serait bien si les cellules pouvaient être **évaluées avant de
     générer le html** - mais ça semble peut-être un peu dur à faire

* un élève a suggéré un tableau de synthèse pour rappeler / comparer
  les types de base; ça pourrait faire du sens..
* un autre aurait apprécié un glossaire...

* exercices sans doute trop difficiles en moyenne
  on observe un taux de 1 succès pour 3 échecs dans les stats

* les quelques séquences qui ont 2 vidéos : des gens sont arrivés à
   rater la deuxième; il suffirait de reprendre un peu la présentation
   pour rendre ça + explicite (un message AVANT la première vidéo).


# Séquelles python2

### w1

 * installation sur windows
   * donner un peu plus d'indications a propos du PATH
   * idem peut-être pour le shebang sur windows
 * le notebook sur le shebang ne doit pas être tout à fait clair par rapport au PATH, pas mal de monde en effet n'a pas '.' dans son PATH

### w2

 * W2-S6-E1 : dans le quiz on parle de l'opérateur `is` qui n'a pas
   encore été introduit à ce stade du cours
 * W2-S8-C3-la-fonction-raw_input.ipynb : il semble que `readline` ne
 soit pas par défaut sur windows
  * w2-s8-e2-chaines : voir la correction dans
  corrections/w2s8_strings.py - un étudiant a remarqué une erreur - on
  est trop laxiste
 * vérifier qu'on montre au moins une fois un exemple de `if` sans `else`

### w3

 * je ne suis plus très sûr de la semaine, mais la digression sur les clés de dictionnaires qui doivent être globalement immutables est assez erronée en ce qui concernent les objets, qui peuvent être utilisés dans les ensembles, donc sans doute comme clé de dictionnaires.

### w4

 * voir `pgcd_ter`, faut-il le publier dans les corrigés ?

### w5

* quiz 'modules et espaces de nommage' : beaucoup d'émoi suscité par
  la formule 'toutes les variables du module'; j'avoue que je suis
  d'accord que la formulation est ambigüe.

* exercice bateau : voir s'il ne serait pas mieux d'utiliser une librairie ?
  * le module LatLon est pour 2.7 seulement

### w6

 * le complément sur les décorateurs : plutoôt que de rediriger vers
   https://wiki.python.org/moin/PythonDecoratorLibrary#Singleton à la
   fin, ce serait mieux de le refaire en le commentant; rien que
   d'utiliser des noms un peu moins space ça va rendre le tout déjà beaucoup + lisible.

 * il semble que dans une vidéo on a annoncé un complément sur le
   binding avec C/C++, qu'on n'a jamais fait.. faire a minima un
   erratum là-dessus

### Exos

* shipdict.py - il faudrait enlever les doublons (même mesure dans 2
  fichiers) - voir bateaux "ENFORCER" et le "SANTA CRUZ" d'après un
  post étudiant

* prévenir + clairement la toute première fois qu'on fait un exo sur
  les bateaux qu'il peut y avoir des bateaux de même nom


### Notebooks et process

 * un bouton pour faire kernel_restart + clear_all_cells + run_all_cells serait très appréciable
 * un bouton pour faire clear_all_cells + remove_empty_cells serait très appréciable
 * avoir git mieux intégré à IPython serait cool
 * un outil dans IPython pour gérer les annotations (notebookname et version)
 * comprendre les signatures entre mac et windows
 * revoir l'utilisation de RawNbConvert
   * a. dans l'état, on n'utilise que le rendu html dans le notebook qui est plutôt sympa
   * b. il y a d'autres voies pour rendre la même chose (genre 'code' avec les 4 espaces en markdown)
   * avec a. on a un html sympa, mais tous les nbconvert sont pourris (on ne peut pas lancer latex par exemple)
   * avec b. c'est mieux pour les exports mais c'est dommage de perdre le rendu
   * j'ai essayé plusieurs voies pour essayer d'obtenir le même rendu
   avec un autre type que RawNbConvert mais sans succès. par exemple
   si je mets moi-meme un `<pre>` avec un `style=` dans un markdown,
   le style ne passe pas très bien (apparemment certains flags css passent et d'autres non...)
   * trouver un autre rendu permettrait d'éditer du pdf plus fidele.
 * produire les PDFs localement et du coup produire des bundle (tar ou
   zip) par semaine

 * ce serait bien si on pouvait lier les notebooks entre eux (mettre des URLs de l'un vers l'autre)
   * apparemment c'est possible déjà sauf que MH ne m'a pas passé la recette magique.
   * dans tous les cas il faudrait dans ce cas garder le libellé de la référence (Semaine x Séquence y)
   * XXX: à bien y réfléchir, c'est très casse gueule car ça rend le
     notebook dépendant du 'run' FUN, c'est sûrement une idée à la
     noix en fait.

Exercices
====================
* ai rencontré une mention aux tags MP3 (Id3) qui pourrait peut-être
  faire un bon exo, surtout dans la perspective de python3 et
  bytes ?


Notes on python3
====================

* subprocess & universal_newlines=True, so that the module knows it
  should return a `str` and not a `bytes`

* XMLRPC & `<base64>` tags vs `<string>` - or whatever it is

* Un étudiant de session2 nous fait remarquer que la technique qui consiste à définir `__repr__` sur une instance ne fonctionne pas telle quelle en python3.


* idée d'exo : calculer la suite dérivée d'une suite; la série de la suite

Librairies
====================

Une liste des librairies dont il va falloir parler; je ne sais pas si/ou Arnaud a commencé quelque chose dans ce genre...

## transverse

* PyPI : pas vraiment une librairie, un repository de modules
-> pip install ...

* mentionner aussi les autres systemes de packaging
rpm / apt-get / macports

## petits modules pratiques

* argparse
* json
* csv
* pprint

## grosses libraries et autres frameworks

### PyQt5

* pour faire des UIs cross-platform: http://www.riverbankcomputing.co.uk/software/pyqt/download5
* le site original Qt http://qt-project.org

## math
NumPy http://www.numpy.org
SciPy http://scipy.org
pandas
sklearn
...
