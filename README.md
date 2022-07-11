# Exercice technique - candidature à Grand-Poitiers

## Rappel des Instructions
* Créer une représentation graphique des résultats du premier tour des élections présidentielles 2022 à Poitiers.
* Dans un **canvas**, pour chaque candidat : placer forme géométrique pleine (de couleur distinctes) dont la surface est proportionelle à son score au premier tour.
* Les formes géométriques représentant les scores ne doivent pas se chevaucher et doivent remplir la totalité de l'espace disponible dans le canvas.
* Afficher à un autre endroit de la page web (en dehors du canvas) la liste des candidat ordonnée par leur score obtenu. 
* Autres instructions :
  * Utilisation des technologies web **au sein d'un seul fichier html** ;
  * Le canvas aura l'**`id` `shapesCanvas`**
  * Les données seront récupérées par le client à chaque chargement de la page depuis l'API open data de Grand Poitiers sur le jeu de données [Citoyenneté - Election Présidentielle - Poitiers 2022 - 1er tour - Résultats](https://data.grandpoitiers.fr/explore/dataset/resultats_election_fichier_eirel_definitif/information/?dataChart=eyJxdWVyaWVzIjpbeyJjb25maWciOnsiZGF0YXNldCI6InJlc3VsdGF0c19lbGVjdGlvbl9maWNoaWVyX2VpcmVsX2RlZmluaXRpZiIsIm9wdGlvbnMiOnt9fSwiY2hhcnRzIjpbeyJhbGlnbk1vbnRoIjp0cnVlLCJ0eXBlIjoiY29sdW1uIiwiZnVuYyI6IkFWRyIsInlBeGlzIjoiYW5uZWUiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiIjOTYxNDU0In1dLCJ4QXhpcyI6ImJ1cmVhdV92b3RlIiwibWF4cG9pbnRzIjo1MCwic29ydCI6IiJ9XSwidGltZXNjYWxlIjoiIiwiZGlzcGxheUxlZ2VuZCI6dHJ1ZSwiYWxpZ25Nb250aCI6dHJ1ZX0%3D) ;
  * le rendu sera dynamique et prendra en compte les données fraîches reçues depuis l'open data ;
  * vous utiliserez l'API canvas ou webGL pour dessiner dans le canvas ;
  * vous devrez implémenter vous-même votre fonction de tri et la methode `Array.sort()` est donc bannie ;
  * le code doit être déposé sur git sur la plateforme de votre choix, vous nous ferez parvenir le lien vers votre projet.

Voici un exemple de rendu qui respecte les règles (les proportions et les scores sont totalement érronées) :

*Note : d'autres types de représentations sont possibles, tant que les règles sont respéctées*

![exemple de rendu](https://i.ibb.co/hYPGymd/Exo-de-code.png)


## Solution proposée
* Une représentation graphique des résultats du premier tour des élections présidentielles 2022 à Poitiers.
* Type de la représentation : Vertical slices treemap diagram.  
  * *Ce type de représentation est proche du squarified treemap donné en exemple. Dans un canvas, pour chaque candidat : un rectangle vertical plein (de couleur distinctes) dont la surface est proportionnelle à son score au premier tour est placé de la gauche vers la droite, en respect de l'ordre décroissant. Le total remplissage du canevas permet d'avoir en un seul coup d'oeil une lecture de la proportionalité des résultats.*
  * Les formes géométriques représentants les scores ne se chevauchent pas et remplissent la totalité de l'espace disponible dans le canvas.
* La liste des candidat ordonnée par leur score obtenu est affichée à côté (version desktop) ou au-dessous (versions tablette et téléphone) du canvas. *La liste, en reprenant les couleurs utilisées dans le canvas, sert de légende de la représentation graphique tout en étant une alternative à l'élément canvas qui n'est pas reconnu par les lecteurs d'écrans*
* L'exercice utilise des technologies web (HTML5, CSS3, JavaScript, Babel pour ES6, API canvas) et est rendu au sein d'un seul fichier html *(index.html)*.
* Le canvas a l'`id` `shapesCanvas`.
* Les données sont récupérées par le client à chaque chargement de la page depuis l'API open data de Grand Poitiers sur le jeu de données Citoyenneté - Election Présidentielle - Poitiers 2022 - 1er tour - Résultats. *Vérification faite via l'onglet réseau des outils de développement de Mozilla firefox.*
* Le rendu est dynamique et prend en compte les données fraîches reçues depuis l'open data.
* L'API canvas est utilisée pour dessiner dans le canvas.
* Une fonction récursive de tri a été implémentée (pas d'utilisation de la méthode native Array.sort() mais de *sortData() cf. ligne 528*).
* Le code est déposé sur git sur la plateforme github.
* ***Test :***
  * *Affichage, étape par étape, des résultats dans la console.*
  * *Contrôle des résulats et affichage dans le console de message d'alerte via des if - else.*
  * *Contrôle de l'affichage dans Firefox, Chrome et Edge.* 
* ***En bonus :***
  * *Dans un souci d'accessibilité, j'ai utilisé un gamme de couleurs adaptée aux personnes présentant les défauts de vision du daltonisme.*
  * *Comme la représentation graphique en tranches n'est pas vraiment habituelle pour l'ensemble des visiteurs potentiels, j'ai créé une seconde représentation à barres horizontales (non demandée) qui, si elle ne répond pas à l'ensemble des instructions, se rapproche plus des types de représentations habituelles ce qui permet d'offrir une alternative qui ne "perde" pas le visiteur tout en "éduquant". Cette seconde représentation est accessible via un formulaire à input radio placé au-dessus des résultats.*
  * *Afin de mieux percevoir ce à quoi cette représentation graphique des résultats pourraient ressembler une fois en ligne, je l'ai placée au sein d'une page reprenant "très grossièrement" l'aspect des pages du site grandpoitiers.fr. J'avoue avoir utilisé les onglets Inspecteur et Editeur de style des outils de développement de mozilla firefox pour trouver le nom de la police utilisée et la pipette pour les couleurs. Par ailleurs, j'ai effectué des captures d'écran pour les logotypes.* ***Je n'utiliserai pas ces informations en dehors de cet exercice.***
