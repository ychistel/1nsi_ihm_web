Exercices
==========

.. _wikipedia du mot WEB: https://fr.wikipedia.org/wiki/World_Wide_Web
.. _wikipedia du mot HTML: https://fr.wikipedia.org/wiki/Hypertext_Markup_Language
.. _mozilla: https://developer.mozilla.org/fr/docs/Glossary/Entity

.. exercice::

    On souhaite réaliser la page web suivante:

    .. figure:: ../img/activite_sans_css.png
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

    On obtient une structure de code:

    .. code:: html
        :caption: Liste numérotée

        <ul>
            <li>premier item</li>
            <li>deuxième item</li>
            <li>Wtroisième item</li>
        </ul>

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

    #.  Restructurer votre document web en insérant tout le contenu de votre page entre les balises ``<body>`` et ``</body>`` puis vérifier que votre page web s'affiche bien.
    #.  Un navigateur ouvre un onglet pour chaque page web. 
        
        a.  Quel est le titre de l'onglet de votre document html affiché par le navigateur ?
        b.  Pour afficher un titre sur l'onglet, on utilise la balise ``<title>...</title>`` placées entre les balises ``<head>`` et ``</head>``. 
        
            Ajouter le titre *Première page web* pour qu'il apparaisse sur l'onglet.

    #.  On appelle **metadonnée** toute information contenue dans le document ``HTML`` qui ne sera pas directement visible sur la page affichée par le navigateur. Ces métadonnées sont placées dans des balises vides ``<meta />`` et leurs valeurs sont associées à des attributs.
    
        Une balise ``<meta />`` est  placée entre les balises ``<head>`` et ``</head>``. Il peut y avoir plusieurs balises ``<meta />`` dans un même document. Les 

        Par exemple, l'encodage de caractères du document est une métadonnée utile au navigateur pour afficher correctement le document ``HTML``. C'est avec l'attribut ``charset`` que l'encodage de caractères sera transmis au navigateur. Le code ``HTML`` est :

        .. code:: html

            <meta charset='...' />
    
        a.  Quel est l'encodage de caractères utilisé par les documents sur le web ?
        b.  Ajouter à votre fichier une balise ``meta`` indiquant l'encodage ``utf-8`` utilisé.
        c.  Modifier l'encodage par ``iso-8859-1`` et actualiser votre page web. La page web s'affiche-t-elle correctement ?

.. exercice::

    Réaliser un tableau en ``HTML`` se fait avec la structure suivante:

    .. code:: html
        :caption: Tableau HTML

        <table>
            <thead>
                <tr><th>colonne 1</th><th>colonne 2</th>...</tr>
            </thead>
            <tbody>
                <tr><td>...</th><th>...</th>...</tr>
                <tr><td>...</th><th>...</th>...</tr>
                ...
            </tbody>
        </table>

    -   La balise ``<table>...</table>`` définit le tableau,
    -   La balise ``<thead>...</thead>`` définit l'entête du tableau c'est à dire la première ligne,
    -   La balise ``<tbody>...</tbody>`` définit le corps du tableau c'est à dire toutes les lignes sauf la première,
    -   La balise ``<tr>...</tr>`` définit une ligne de tableau,
    -   Les balises ``<th>...</th>`` et ``<td>...</td>`` définissent les colonnes du tableau.

    Créer une page web qui contient le tableau ci-dessous:

    .. figure:: ../img/tableau_pays.png
        :align: center

