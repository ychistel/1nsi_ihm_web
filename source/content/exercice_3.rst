Exercices
==========

.. exercice::

    *On reprend le document web créé dans les 2 parties précédentes*

    #.  Ajouter les deux balises pour créer un script ``JAVASCRIPT`` entre les  ``<head>`` et ``</head>`` de votre document HTML.

    #.  On donne un premier script JAVASCRIPT:

        .. code-block:: javascript

            alert('mon premier script');

        Placer ce script entre les balises "javascript" de votre document puis actualiser la page web.

    #.  On propose de compléter le script précédent avec l'instruction:

        .. code-block:: javascript

            console.log('mon premier script');

        Actualiser la page web puis ouvrir les outils de développement (F12 ou CTRL MAJ I) et sélectionner l'onglet "Console". Afficher les journaux et actualiser la page si nécessaire.

        .. important::

            Cette astuce utilisant l'instruction ``console.log()`` est très utile pour debugger les programmes !

    #.  On remplace notre script par les instructions suivantes:

        .. code-block:: javascript
    
            nom = prompt('Quel est ton nom ?');
            alert(nom);

        a.  Modifier votre document HTML avec ce nouveau script puis actualiser votre page dans le navigateur.

            .. figure:: ../img/prompt_nom.png
                :alt: image
                :align: center
                :width: 400
            
        c.  Compléter le script avec une troisième ligne de code pour afficher le nom en console.
        d.  On peut améliorer l'affichage en concaténant la variable ``nom`` et un texte grâce au signe d'addition.
            
            Ajouter le texte ``Votre nom est `` pour obtenir l'affichage d'alerte ci-dessous.

            .. figure:: ../img/alert_nom.png
                :alt: image
                :align: center
                :width: 400
                :class: border-style-solid border-width-1 border-color-gray

.. exercice::

    *On reprend le document web créé dans les 2 parties précédentes*

    #.  On peut utiliser des scripts javascript placés dans un fichier externe. Dans ce cas, on ajoute dans la balise ``<head>...</head>`` la balise suivante.

        .. code-block:: javascript

            <script type="text/javascript" src="script.js"></script>
            
    #.  Télécharger sur l'ENT le fichier ``script.js`` dans le même dossier que votre fichier html. Ce fichier contient de petites fonctions en javascript pour agir sur le document HTML.

    #.  L'événement ``onclick`` écoute le clic de souris dans le document WEB. Celui-ci est limité à une zone du document.

        a.  Remplacer la balise ``<body>`` par la balise suivante:

            .. code-block:: javascript

                <body onclick="colorer()">

        b.  Recharger la page puis tester votre événement en cliquant dans le corps de la page WEB. Vous pouvez supprimer cet événement après les tests.
        
    #.  Il n'y a qu’une seule balise ``<body>`` ! Mais certaines balises sont multiples comme les titres, les paragraphes ou les images. On peut identifier les balises d'un document html par un identifiant. Un identifiant est un mot unique du document HTML qui se note dans la balise par ``id="identifiant"``.

        a.  Ajouter l’identifiant ``logo`` dans la balise ``<img>`` contenant le logo HTML de votre document.
        b.  L'événement ``onmouseover`` écoute le survol d’un élément HTML du document pour exécuter la fonction associée.

            Ajouter dans la balise ``<img>`` de l’image qui a l’identifiant logo l'instruction ``onmouseover="encadrer()"``.

        c.  Vérifier dans votre document web que le survol du logo ajoute un cadre à l'image.

    #.  En HTML, on peut ajouter des boutons qui permettent de créer de l’interactivité. Pour ajouter un bouton, il faut appliquer la syntaxe suivante:

        .. code-block:: html

            <button>Texte sur le bouton</button>

        a.  Ajouter dans votre document HTML un bouton avec l'identifiant ``btn`` et contenant le texte "Cliquer".
        b.  Ajouter l’événement ``onClick`` sur le bouton en associant une instruction d’alerte qui affiche le message "Tu as cliqué sur le bouton !".

    #.  Ouvrir avec l’éditeur notepad++ le fichier ``script.js``. Ce fichier contient des fonctions écrites en javascript qui vont nous servir de modèle.

        a.  Compléter la fonction ``alerter`` pour afficher le message "Tu as cliqué sur le bouton !" puis associer cette fonction au bouton ``btn``.

        b.  Modifier la fonction ``alerter`` pour afficher le message en console.

.. exercice::

    *On reprend le document web créé dans les 2 parties précédentes*

    Nous allons écrire un script qui ajoute un message dans le document HTML.

    #.  Dans la page web, ajouter sous le bouton la balise ``<p id ="message"><\p>``. Actualiser la page web sur votre navigateur et vérifier que rien n'apparait puisque la balise est vide.
    #.  En javascript, on peut accéder à une balise de la page html grâce à son identifiant. L'instruction est la suivante:

        .. code-block:: javascript

            msg = document.getElementById('identifiant de balise');

        Ajouter dans la fonction ``saisir_nom()`` cette instruction pour accéder à la balise ``<p>`` d'identifiant ``message``.

    #.  On peut ajouter un contenu dans le document html par l'instruction suivante:

        .. code-block:: javascript

            msg.innerHTML = "nouveau contenu";

        Ajouter dans la fonction ``saisir_nom()`` cette instruction pour ajouter le contenu ``"Mon nom est Bob !"`` dans la page web.

    #.  Remplacer l'événement ``onclick='alerter();'`` pour obtenir l'affichage de notre message lorsqu'on clique sur le bouton.
    #.  Modifier le script de la fonction ``saisir_nom()`` pour provoquer la saisie d'un nom et afficher le message précédent en remplaçant "Bob" par le nom saisi.