General
=======

 * classes new-style
   * trop de d�calage dans le temps entre le cours semaine 5
     et celui de la semaine 7

 * equilibre cours
   * la semaine 2 est tr�s charg�e
   * les libell�s des diff�rentes semaines sont impr�cis

 * bisect the repo to find out about this
   "nous dirons plus tard que les variables r�f�rencent le m�me objet" thing
   when was it written, by whom, did valerie let this pass ?

W1
===

 * installation sur windows
   * donner un peu plus d'indications a propos du PATH
   * idem peut-�tre pour le shebang sur windows

W2
===

 * Le quiz sur les listes et la copie avec 3 * [[0]] est assez foireux
   il faudrait le supprimer ou le r�crire avec un exemple plus pertinent (sans le '*')

 * W2S8 - l'exercice 'affichage' donne un r�sultat discutable pour Ted Mosby,
   * le dernier champ �tant vide on pourrait s'attendre � afficher ??
   * d'ailleurs la mise en page sur la plateforme pourrait �tre am�lior�e,
     comme de toutes fa�ons on se retrouve avec 2 lignes par input
     autant ne pas abr�ger c'est inutile et confusant

 * le quiz sur le formattage des strings, et 'dans du code nouveau'
   a suscit� pas mal d'�moi, il faudrait pr�ciser mieux l'histoire
   des % qu'on ne compte pas comme corrects.

W3
===

 * W3S2 - dans le quiz on propose une option qui est `'marc' in annuaire and annuaire['marc']`
   quelqu'un remarque que ceci renvoie False au lieu de None
   il faudrait mettre �a en contexte

 * W3S6 dans le notebook la section sur le short-circuit est foireuse,
   il faudrait des trucs + simples comme tout simplement
   True and 0/0
   False and 0/0
   qui est bcp + clair � comprendre - plutot que ces pop() qui sont confusants

 * W3S2 l'exo sur les bateaux (abbreviated et extended et les dictionnaires)
   semble �tre trop raide pour certains
   j'ai rang� dans la branche 'exo' une version 2.0 de cet exercice
   qui se d�cline en deux versions basique et interm�diaire

Notebooks et process
====================
 * un bouton pour faire kernel_restart + clear_all_cells + run_all_cells serait tr�s appr�ciable
 * un bouton pour faire clear_all_cells + remove_empty_cells serait tr�s appr�ciable
 * avoir git mieux int�gr� � IPython serait cool
 * un outil dans IPython pour g�rer les annotations (notebookname et version)
 * comprendre les signatures entre mac et windows
 * revoir l'utilisation de RawNbConvert
   * a. dans l'�tat, on n'utilise que le rendu html dans le notebook qui est plut�t sympa
   * b. il y a d'autres voies pour rendre la m�me chose (genre 'code' avec les 4 espaces en markdown)
   * avec a. on a un html sympa, mais tous les nbconvert sont pourris (on ne peut pas lancer latex par exemple)
   * avec b. c'est mieux pour les exports mais c'est dommage de perdre le rendu
   * j'ai essay� plusieurs voies pour essayer d'obtenir le m�me rendu avec un autre type que RawNbConvert mais sans succ�s. par exemple si je mets moi-meme un <pre> avec un style dans un markdown, le style ne passe pas tr�s bien (apparemment certains flags css passent et d'autres non...)
   * trouver un autre rendu permettrait d'�diter du pdf plus fidele.

 * ce serait bien si on pouvait lier les notebooks entre eux (mettre des URLs de l'un vers l'autre)
   * apparemment c'est possible d�j� sauf que MH ne m'a pas pass� la recette magique.
   * dans tous les cas il faudrait dans ce cas garder le libell� de la r�f�rence (Semaine x S�quence y)