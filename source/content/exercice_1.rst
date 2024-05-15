Exercices
==========

.. _wikipedia du mot WEB: https://fr.wikipedia.org/wiki/World_Wide_Web
.. _wikipedia du mot HTML: https://fr.wikipedia.org/wiki/Hypertext_Markup_Language

.. exercice::

    On souhaite réaliser la page web suivante:

    .. figure:: ../img/langage_html.png
        :alt: image
        :align: center
        :width: 100%

    Le contenu de cette page web est dans un fichier texte disponible sur l'ENT.

    #.  Ouvrir ce fichier avec l'éditeur **notepad++** et aussi avec un **navigateur**.
    #.  Ajouter la balise de titre de niveau 1 autour du texte "Fonctionnement du web" et vérifier son affichage.
    #.  Sous le titre principal, ajouter le logo du langage html avec la balise :

        .. code:: html

            <img src="https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg" />

        L'image affichée est trop grande. Ajouter dans la balise ``img`` l'attribut ``width`` qui modifie la largeur avec une valeur de ``200px``.
    #.  Ajouter les balises de titre de niveau 2 (en bleu sur l'image ci dessus).
    #.  Ajouter les balises pour chaque paragraphe.
    #.  Ajouter la deuxième image dans le paragraphe "Introduction" qui est alors découpé en 2 paragraphes. L'url de l'image est ``https://upload.wikimedia.org/wikipedia/commons/d/db/Spider_web_Belgium_Luc_Viatour.jpg`` et a une largeur de 360 pixel.
    #.  La page web contient 2 liens hypertextes sur les mots ``WEB`` et ``HTML``.

        a.  Ajouter le lien hypertexte sur le mot ``WEB`` avec la balise:

            .. code::

                <a href="https://fr.wikipedia.org/wiki/World_Wide_Web">WEB</a>

        b.  Ajouter sur le mot ``HTML`` le lien hypertexte vers la page `wikipedia du mot HTML`_ dans le paragraphe "langage HTML".

    #.  L'affichage des mots ``<balise>`` et ``</balise>`` n’est pas correct. Cela s'explique par le fait que le navigateur essaie d'interpréter ces balises comme de vraies balises html sans y parvenir. Pour afficher des caractères spéciaux, appelés **entités html**, il faut utiliser un encodage propre au html.

        Le site de `mozilla`_ vous guide pour afficher correctement ces balises html dans votre document.


.. exercice::

    *On poursuit avec la page web commencée dans l'exercice précédent.*

    Il existe deux types de listes : les listes numérotées et les listes à puces. Les contenus d'une liste sont appelés des **items**. Il y a donc autant d'items que de numéros ou de puces qui sont toujours placés avant.

    La balise ``<ol>liste numérotée</ol>`` crée une liste numérotée et la balise ``<ul>liste à puces</ul>`` crée une liste à puces. Chaque item de liste est entouré par les balises ``<li>item</li>``.

    #.  Créer la liste numérotée dans le paragraphe "Langage du web" avec les trois items associés au trois langages utilisés dans le web.
    #.  Créer la liste à puces dans le dernier paragraphe sur les types de balises html.

.. exercice::

    Une page web se décompose en 2 parties:

    -  Une partie non affichée qui contient des informations sur la page web utiles au navigateur pour afficher correctement la page. Cette partie est l'entête du document html balisée par ``<head>...</head>``
    -  Une partie affichée par le navigateur qui contient le contenu du document. C'est le coprs du document html balisé par ``<body>...</body>``.

    Les deux parties ``entête`` et ``body`` sont contenues dans la balise ``<html>...</html>`` qui indique au navigateur que le contenu à afficher est en langage ``html``.

    On obtient un document dont la structure est la suivante:

    .. code:: html

        <!doctype>
        <html>
            <head>
                ...
            </head>
            <body>
                ...
            </body>
        </html>
    
    *On poursuit avec le document web créé dans les exercices précédents.*

    #.  Structurer votre document web avec les balises html, d'entête et de corps. Vérifier que celle-ci s'affiche toujours correctement dans le navigateur.
    #.  Un navigateur ouvre un onglet pour chaque page web. 
        
        a.  Quel est le titre de l'onglet de votre document html affiché par le navigateur ?
        b.  Pour afficher un titre sur l'onglet, on utilise la balise ``<title>...</title>``. Ajouter le titre *Première page web* pour qu'il apparaisse sur l'onglet.
    #.  Les balises ``<meta />`` sont des balises vides qui informent le navigateur sur le document à afficher. Elle est accompagnée d'un attribut qui contient les informations à transmettre au navigateur.
    
        Par exemple l'attribut ``charset`` indique l'encodage de caractères que doit utiliser le navigateur. 
    
        a.  Ajouter à votre fichier une balise ``meta`` indiquant l'encodage ``utf-8`` utilisé.
        b. Modifier l'encodage par ``iso-8859-1`` et actualiser votre page web. La page web s'affiche-t-elle correctement ?

.. exercice::

    La partie cours sur "Le langage html" contient un tableau.

    #.  En utilisant les outils de développement du navigateur, retouver la structure html et les balises utilisées pour créer un tableau.
    #.  Créer une page web qui contient le tableau ci-dessous:

        .. figure:: ../img/tableau_pays.png
            :align: center

