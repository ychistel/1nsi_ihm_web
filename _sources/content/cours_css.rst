.. _font google: https://fonts.google.com/

Les styles en CSS
====================

Le langage HTML structure le contenu d'un document WEB mais pas son apparence. Pour modifier l'apparence d'un document, on lui applique des règles de style avec le langage CSS (Cascading Style Sheet).

Les règles de style CSS sont définies dans l'entête du document dans la balise ``<head>...</head>``. Toutes les règles CSS seront comprises entre les balises ``<style>`` et ``</style>``. Cette balise doit contenir l'attribut ``type`` qui a pour valeur ``text/css``.

On obtient la structure suivante:

.. code:: html
    :caption: Structure du document html

    <!doctype>
    <html>
        <head>
            <style type="text/css">
                ...
            </style>
            ...
        </head>
        <body>
            ...
        </body>
    </html>

Style sur un sélecteur
-----------------------

Un **sélecteur** en CSS est une balise html. Par exemple, les balises ``h1``, ``h2`` et ``body`` sont des sélecteurs. On peut modifier l'apparence d'un sélecteur dans un document html en lui appliquant des règles CSS.

Une règle CSS s'écrit toujours avec la même syntaxe :

.. code:: css
    :caption: Syntaxe d'une règle en CSS

    selecteur { propriété 1 : valeur 1 ; propriété 2: valeur 2; }

.. note::

    On peut définir plus de 2 propriétés pour une règle CSS. Les propriétés se terminent toujours par un point-virgule.

Par exemple, pour centrer un titre de niveau 1 sur un document web, on lui applique la propriété ``text-align`` avec la valeur ``center``. Cela donne alors le code suivant:

.. code:: css

    <style type="text/css">
    h1{
        text-align:center;
    }
    </style>

Si on veut augmenter la taille de la police du titre de niveau 1, on ajoute une seconde propriété ``font-size`` de valeur ``3em``.

.. code:: css

    <style type="text/css">
    h1{
        text-align:center;
        font-size:3em;
    }
    </style>

.. note::

    La valeur ``3em`` signifie que la taille de police définie pour le document est multipliée par 3.

Les classes en CSS
-------------------

L'attribution de règles CSS sur un sélecteur peut poser problème lorsqu'un sélecteur est présent à plusieurs endroits du document comme les balises de paragraphes ``p``.

Par exemple, on veut que le premier paragraphe d'un document soit affiché en gras et encadré. Si on définit les règles CSS sur le sélecteur ``p``, les règles CSS seront appliquées à tous les paragraphes, donc tous nos paragraphes seront affichés en gras et encadrés.

Pour éviter cela, on définit une classe dans la balise html et on crée des règles CSS pour cette classe. 

-   On ajoute dans la balise html la classe avec le mot ``class`` suivi du nom qu'on donne à la classe.
-   Dans la partie ``style``, on crée les règles CSS pour la classe en faisant précédé le nom de la classe par un point.

Reprenons notre exemple de premier paragraphe affiché en gras et encadré. On crée une classe ``chapo`` qu'on ajoute à la première balise ``p`` du document html et on difinit les règles CSS. On a le code suivant:

.. code:: html
    :caption: Classe dans un document html

    <!doctype>
    <html>
        <head>
            <style type="text/css">
                .chapo{
                    font-weight: bold; /*affichage en gras*/
                    border: solid 1px black; /*encadrement du paragraphe*/
                }
            </style>
        </head>
        <body>
            <p class="chapo">Le premier paragraphe en gras et encadré.</p>
            <p>Le second paragraphe.</p>
        </body>
    </html>

ce qui donne le résultat suivant:

.. raw:: html
    :class: demo

    <!doctype>
    <html>
        <head>
            <style type="text/css">
                .chapo{
                    font-weight: bold; /*affichage en gras*/
                    border: solid 1px red; /*encadrement du paragraphe*/
                }
            </style>
        </head>
        <body>
            <p class="chapo">Le premier paragraphe en gras et encadré.</p>
            <p>Le second paragraphe.</p>
        </body>
    </html>

Feuille de style
-----------------

Si la méthode utilisée pour définir des styles à appliquer à un document html est parfaitement valable, il est préférable d'utiliser des feuilles de styles externes. 

Un site WEB contient plusieurs fichiers HTML. Si on définit les mêmes styles dans chaque fichier, il devient très difficile de maintenir le site. Une erreur de style à corriger dans un fichier implique qu'il faut modifier tous les fichiers ! Il est donc préférable de rassembler toutes les règles CSS dans un même fichier et de faire un lien vers cette feuille de style depuis tous les documents HTML.

#.  On crée un fichier dont l'extension est ``.css`` et on rassemble toutes les règles CSS dans ce fichier.
#.  On supprime les règles CSS dans les différents fichiers HTML.
#.  On remplace la balise ``<style>...</style>`` par la balise vide ``<link type="text/css" href="..." rel="stylesheet" />``

Par exemple, si on crée un fichier ``mon_style.css`` contenant toutes les règles CSS, le document HTML est alors modifié en:

.. code:: html
    :caption: Feuille de style externe

    <!doctype>
    <html>
        <head>
            <link type="text/css" href="mon_style.css" rel="stylesheet" />
            ...
        </head>
        <body>
            ...
        </body>
    </html>
