Exercices
==========

.. exercice::

    L'image ci-dessous est notre premier document web écrit en langage html. Nous n'avons pas encore obtenu le résultat final attendu.

    .. figure:: ../img/style_css.png
        :alt: image
        :align: center
        :width: 100%

    On reprend notre document html pour appliquer les règles CSS pour obtenir l'affichage souhaité.

    #.  Ajouter la balise ``<style>...</style>`` dans votre document html.
    #.  On va réduire la largeur de la page web et centrer son contenu avec une règle CSS sur le sélecteur ``body``. 
    
        Ajouter dans votre document, entre les balises ``<style>`` et ``</style>`` les propriétés CSS suivantes sur le sélecteur ``body``.

        .. code:: css

            body{
                font-family: Verdana,sans-serif;
                font-size:1em;
                line-height:1.5em;
                width:1080px;
                margin:auto
            }

    #.  Le titre de la page "Fonctionnement du web" doit être centré et avoir une taille plus importante.

        Ajouter le sélecteur associé au titre de niveau 1, puis la propriété ``text-align`` qui a pour valeur ``center`` et la propriété ``font-size`` qui a pour valeur ``3em``.

    #.  Les titres de niveau 2 ont une couleur bleue. La propriété CSS qui définit la couleur est ``color``. Les valeurs pour les couleurs peuvent avoir plusieurs écritures.

        -   le nom de la couleur en anglais : ``cyan``
        -   le code couleur RGB en hexadécimal précédé du signe # : ``#00ffff``
        -   le code couleur RGB en décimal écrit entre parenthèses et précédé par rgb : ``rgb(0,255,255)``

        a.  Rechercher sur le WEB les trois écritures possibles pour la couleur "bleu royal" ?
        b.  Ajouter la propriété CSS qui modifie la couleur des titres de niveau 2 en bleu royal.

    #.  Les images du document sont centrées. Pour centrer une image sur la page, ajouter la règle CSS sur le sélecteur ``img`` suivante:

        .. code:: css

            img{
                display:block;
                margin:16px auto;
            }

.. exercice::

    *on reprend le document de l'exercice précédent*.

    La photo de toile d’araignée est encadrée avec un effet ombré. Pour obtenir cet effet, on applique la règle CSS suivante:

    .. code:: css

        border:solid 1px #eee;
        box-shadow:4px 4px #aaa;
        padding:8px;

    #.  Peut-on appliquer ces règles au sélecteur ``img``? Justifier.
    #.  Créer la classe CSS ``toile`` et ajouter les propriétés CSS définies ci-dessus.
    #.  Ajouter la classe ``toile`` à la photo de toile d'araignée et vérifier que son apparence est modifiée.
    #.  On souhaite modifier l'apparence du premier paragraphe (au-dessus de la photo de toile d'araignée) pour :

        -   afficher le texte en couleur bleu royal,
        -   afficher le texte en gras,
        -   encadrer le texte en bleu gris.

        Apporter les modifications nécessaires au document sans modifier les autres paragraphes.

.. exercice::

    *on reprend le document de l'exercice précédent*.

    On veut rassembler toutes les propriétés CSS dans un fichier externe.

    #.  Créer une feuille de style CSS sous le nom ``feuille_style.css``.
    #.  Ajouter les propriétés CSS du document HTML dans la feuille de style.
    #.  Modifier le document HTML pour relier la feuille de style au fichier HTML.

    #.  Ajouter un lien vers une feuille de style permet de créer des liens vers des feuilles de style se trouvant sur le WEB.

        Un usage possible est l’application d’une police de style proposée par google.

        a. Rendez vous sur le site des `font google`_,
        b. Choisissez une police et copiez le lien de la feuille de style dans votre document.
        c. Ajouter dans le sélecteur body la propriété CSS font-family associée.
        d. Vérifiez que la police choisie est bien appliquée à votre document html.

.. exercice::

    Dans un précédent exercice, on a créé un document HTML contenant un tableau.

    .. figure:: ../img/tableau_pays.png
        :align: center

        Figure 1

    On souhaite ajouter des règles CSS pour obtenir l'apparence suivante:

    .. figure:: ../img/tableau_pays_css.png
        :align: center

        Figure 2

    #.  Créer la classes CSS ``tableau`` pour avoir une bordure noire au tableau et une largeur de 400px.
    #.  Créer la classe CSS ``centre`` pour centrer les contenus dans les colonnes du tableau.
    #.  Créer la classe CSS ``entete`` pour que les descripteurs du tableau en première ligne soient écrits en blanc sur fond gris.
    #.  Ajouter les trois classes CSS à votre code HTML pour obtenir le tableau illustré par la figure 2.