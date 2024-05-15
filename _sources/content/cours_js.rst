Les événements en JAVASCRIPT
============================

Une page WEB s’affiche sur le navigateur d’une machine cliente. On rappelle que l’affichage de cette page WEB fait suite à une requêtre HTTP de la machine cliente vers le serveur qui dispose de la page WEB.

Le serveur répond à la requête HTTP en renvoyant la page WEB demandée au format HTML et avec un code d’état égal à 200 et un statut OK.

La page WEB est au format HTML, contient des propriétés CSS pour l’affichage et aussi (éventuellement) des scripts en langage ``JAVASCRIPT``.

.. figure:: ../img/requete_http.png
   :alt: image
   :align: center

Un script ``JAVASCRIPT`` chargé avec la page web est un programme exécuté par le navigateur du client qui permet d’agir sur la page WEB affichée.

Un script JAVASCRIPT peut:

-  modifier le contenu de la page et ses balises HTML.
-  modifier l'affichage en ajoutant ou en modifiant les propriétés CSS,
-  interagir avec l'utilisateur avec les **événements** JAVASCRIPT.

Lorsqu'un script est chargé dans une fenêtre ou un onglet du navigateur, celui-ci s'exécute dans la fenêtre ou l'onglet qui l'a chargé.

Introduction au JAVASCRIPT
--------------------------

Un script JAVASCRIPT peut être placé n'importe où dans la page HTML. Néanmoins, il est préférable de l'ajouter :

-  soit dans l'entête du document HTML entre les balises ``<head>`` et ``</head>``,
-  soit à la fin du document juste avant la balise ``</html>`` ou la balise ``</body>``.

Un script ``JAVASCRIPT`` est toujours placé entre les balises ``<script type="text/javascript">`` et ``</script>``. La structure du document HTML devient:

.. code:: html
    :caption: Script javascript dans un document HTML

    <!doctype>
    <html>
        <head>
            <link type="text/css" href="mon_style.css" rel="stylesheet" />
            <script type="text/javascript">
                ...
            </script>
            ...
        </head>
        <body>
            ...
        </body>
    </html>


Gestion des événements en JAVASCRIPT
------------------------------------

Le langage JAVASCRIPT permet la gestion des événements. Il est à l'écoute des interactions de la personne avec la page WEB. Voici quelques événements en ``JAVASCRIPT``:

-  Le clic de la souris : ``onClick``,
-  le survol par la souris d'une partie de l'écran, d'un mot, d'une image, etc : ``onMouseover``,
-  le chargement complet de la page : ``onload``,

La gestion d'un événement en ``JAVASCRIPT`` se déroule en 2 étapes:

#.  On crée un script ou une fonction en javascript qui agit sur la page WEB affichée,
#.  On ajoute un déclencheur de cette action en plaçant dans une balise HTML l'événement JAVASCRIPT.

Par exemple, une page WEB permet de changer la couleur du titre principal lorsqu'on clique dessus. On écrit une fonction ``colore`` qui change la couleur du titre puis dans dans la balise ``h1`` on ajoute le déclencheur de l'événement ``onClick="colore()"``. On obtient le code suivant:


.. code:: html
    :caption: Événement en javascript

    <!doctype>
    <html>
        <head>
            <script type="text/javascript">
                function colore(){
                    document.getElementById('titre').style.color = 'red';
                }
            </script>
            ...
        </head>
        <body>
            <h1 id="titre" onClick="colore()">Changer la couleur du titre</h1>
            <p>La gestion d'un événement javascript...</p>
        </body>
    </html>

.. raw:: html
    :class: demo

    <!doctype>
    <html>
        <head>
            <script type="text/javascript">
                function colore(){
                    document.getElementById('titre').style.color = 'red';
                }
            </script>
        </head>
        <body>
            <h1 id="titre" onClick="colore()">Changer la couleur du titre</h1>
            <p>La gestion d'un événement javascript...</p>
        </body>
    </html>

Agir sur le contenu du document
-------------------------------

Le langage javascript permet de modifier le contenu d'une page web. Pour cela, il faut utiliser des identifiants pour les balises HTML. Chaque identifiant est unique dans le document WEB. Cela permet aux scripts ``JAVASCRIPT`` d'agir sur le document sans risque de conflit.

On peut agir sur un document de différentes manières. Par exemple,

-   En modifiant son apparence  (comme vu précédemment),
-   En modifiant le contenu du document,
-   En ajoutant du contenu à un document.

Prenons l'exemple d'un document qui ajoute la date du jour et l'heure. En voici le code:

.. code:: html
    :caption: Afficher la date et l'heure en javascript

    <!DOCTYPE html>
    <html lang="fr">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Afficher la Date et l'Heure</title>
        <style>
            #datetime{
                text-align:center;
                font-size: 2em;
            }
        </style>
        <script>
            function updateDateTime() {
                var now = new Date();
                var optionsDate = { year: 'numeric', month: 'long', day: 'numeric' };
                var optionsTime = { hour: '2-digit', minute: '2-digit', second: '2-digit' };
                var dateStr = now.toLocaleDateString('fr-FR', optionsDate);
                var timeStr = now.toLocaleTimeString('fr-FR', optionsTime);
                document.getElementById('datetime').innerText = dateStr + ' ' + timeStr;
            }

            // Mettre à jour l'heure chaque seconde
            setInterval(updateDateTime, 1000);

            // Appeler immédiatement la fonction pour afficher la date et l'heure sans attendre 1 seconde
            updateDateTime();
        </script>
    </head>
    <body>
        <h2>La date et l'heure du jour</h2>
        <div id="datetime"></div>
    </body>
    </html>


.. note::

    #.  Le document HTML contient une balise ``div`` qui crée un emplacement dans le document. On remarque que cette balise n'a pas de contenu.
    #.  La balise a un identifiant ``datetime`` qui est utilisé par la script javascript.
    #.  Le script javascript crée la date et l'heure en l'actualisant toutes les secondes.

.. raw:: html
    :class: demo

    <!DOCTYPE html>
    <html lang="fr">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Afficher la Date et l'Heure</title>
        <style>
            #datetime{
                text-align:center;
                font-size: 2em;
            }
        </style>
        <script>
            function updateDateTime() {
                var now = new Date();
                var optionsDate = { year: 'numeric', month: 'long', day: 'numeric' };
                var optionsTime = { hour: '2-digit', minute: '2-digit', second: '2-digit' };
                var dateStr = now.toLocaleDateString('fr-FR', optionsDate);
                var timeStr = now.toLocaleTimeString('fr-FR', optionsTime);
                document.getElementById('datetime').innerText = dateStr + ' ' + timeStr;
            }

            // Mettre à jour l'heure chaque seconde
            setInterval(updateDateTime, 1000);

            // Appeler immédiatement la fonction pour afficher la date et l'heure sans attendre 1 seconde
            updateDateTime();
        </script>
    </head>
    <body>
        <h2>La date et l'heure du jour</h2>
        <div id="datetime"></div>
    </body>
    </html>