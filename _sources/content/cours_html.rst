.. _wikipedia du mot WEB: https://fr.wikipedia.org/wiki/World_Wide_Web
.. _wikipedia du mot HTML: https://fr.wikipedia.org/wiki/Hypertext_Markup_Language
.. _mozilla: https://developer.mozilla.org/fr/docs/Glossary/Entity

Le langage html
===============

Le document ci-dessous est une image représentant une page Web. Son apparence ne laisse rien apparaître du
langage utilisé. Ce langage est le ``HTML`` acronyme de ``HyperTexte Markup Language`` qui signifie "Langage de Balisage Hypertexte".

.. figure:: ../img/activite_sans_css.png
   :alt: image
   :align: center
   :width: 100%

   Page en langage html
   

Le contenu d'une page web est structuré par les éléments qu'elle contient. Sur la figure ci-dessus, la page contient:

-  un titre "Fonctionnement du web",
-  des sous-titres "Introduction", "Langages du WEB", etc,
-  des paragraphes placés après chaque sous-titres
-  des images,
-  une liste numérotée et une liste à puces.

Le contenu d'une page web peut également contenir des mises en forme permettant de mettre en évidence des mots du texte avec:

-  des mots en caractères **gras**,
-  des mots en caractères *italiques*,
-  des liens hypertextes pour accéder à d'autres contenus web,
-  une police et une taille de police différente.

On obtient cette structure et cette mise en forme avec des ``balises``. Il existe 2 types de balises:

-  les balises ouvrantes et fermantes qui se placent avant et après le contenu: ``<balise>le contenu</balise>``
-  les balises dites vides qui ne contiennent pas de contenu: ``<balise />``.

Les balises peuvent contenir des attributs. Un attribut est une propriété qui permet d'agir sur le contenu. La syntaxe est la suivante: ``<balise attribut="valeur">contenu</balise>`` ou ``<balise attribut="valeur" />``.

Le tableau ci-après donne les principales balises du langage ``html`` pour structurer et mettre en forme un texte.

.. csv-table::
   :file: ../csv/balise_html.csv
   :header-rows: 1
   :widths: 10, 15,20
   :delim: ;
   :class: bordure border-style-solid border-width-1
