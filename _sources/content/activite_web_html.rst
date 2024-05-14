.. _wikipedia du mot WEB: https://fr.wikipedia.org/wiki/World_Wide_Web
.. _wikipedia du mot HTML: https://fr.wikipedia.org/wiki/Hypertext_Markup_Language
.. _mozilla: https://developer.mozilla.org/fr/docs/Glossary/Entity

Le langage html
===============

Le document ci-dessous est une image représentant une page Web. Son apparence ne laisse rien apparaître du
langage utilisé. Ce langage est le ``HTML`` acronyme de ``HyperTexte Markup Language`` qui signifie "Langage de Balisage Hypertexte".

.. figure:: ../img/langage_html.png
   :alt: image
   :align: center
   :width: 100%

   Page en langage html
   
#. Une page web est structurée selon les éléments qu'elle contient. Identifier sur l'image ci-dessus 5 éléments structurel contenu dans la page web.

#. Un texte peut également contenir des mises en forme permettant de mettre en évidence des mots du texte. Citer différents mises en forme applicable à des mots d'un texte.

#. Une page web est écrite en langage **html**. Ce langage utilise des **balises** pour structurer les contenus d’un texte. Le tableau ci-après donne les principales balises du langage html pour structurer un texte.

   .. csv-table::
      :file: ../csv/balise_html.csv
      :header-rows: 1
      :widths: 10, 15,20
      :delim: ;

   Identifier les balises html aux différents éléments structurels et de mise en forme d'un texte.

#. Le contenu de la page web est dans un fichier texte, disponible sur l'ENT et visible sur la figure suivante.

   .. image:: ../img/langage_html_txt.png
      :alt: image

   a. Ouvrir ce fichier avec l’éditeur notepad++ et ajouter les balises html pour structurer le contenu.
   b. Sauvegarder votre fichier avec une extension ``html`` et l'ouvrir avec un navigateur.

#. Afficher votre page html et activer les outils de développement (F12) et sélectionner l'onglet **inspecteur** (vous pouvez aussi faire un clic droit de souris et sélectionner "inspecter").

   Vérifier la présence des balises que vous avez ajouter à votre fichier.

#. Ajouter les liens hypertextes suivants:

   a. Un lien vers la page `wikipedia du mot WEB`_ dans le paragraphe introduction.
   b. Un lien vers la page `wikipedia du mot HTML`_ dans le paragraphe langage HTML.

#. L'affichage des balises ``<balise>`` et ``</balise>`` n’est pas correct. Cela s'explique par le fait que le navigateur essaie d'interpréter ces balises comme de vraies balises html sans y parvenir. Pour afficher des caractères spéciaux, appelés **entités html**, il faut utiliser un encodage propre au html.

   Le site de `mozilla`_ vous guide pour afficher correctement les balises html dans votre document.

#. Une page web se décompose en 2 parties:

   -  Une partie non affichée qui contient des informations sur la page web utiles au navigateur pour afficher correctement la page. Cette partie est l'entête du document html balisée par ``<head>...</head>``
   -  Une partie affichée par le navigateur qui contient le contenu du document. C'est le coprs du document html balisé par ``<body>...</body>``.
   
   a. Ajouter dans votre fichier html les balises de l'entête et du corps du document.
   b. Quel est le titre de l'onglet de votre document html affiché par le navigateur ?
   c. Pour afficher un titre sur l'onglet, on ajoute la balise ``<title>...</title>``. Ajouter le titre *Première page web* pour qu'il apparaisse sur l'onglet.
   d. Les balises ``<meta />`` sont des balises vides qui informent le navigateur sur le document à afficher. Elle est accompagnée d'un attribut qui contient les informations à transmettre au navigateur.
   Par exemple l'attribut ``charset`` indique l'encodage de caractères à utiliser. 
   
      Ajouter à votre fichier une balise ``meta`` indiquant l'encodage ``utf-8`` utilisé.

   d. Modifier l'encodage par ``iso-8859-1`` et actualiser votre page web. La page web s'affiche-t-elle correctement ?
