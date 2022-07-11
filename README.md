# Exercice technique - candidature à Grand-Poitiers

## Rappel des Instructions
* Créer une représentation graphique des résultats du premier tour des élections présidentielles 2022 à Poitiers.
* Dans un **canvas**, pour chaque candidat : placer forme géométrique pleine (de couleur distinctes) dont la surface est proportionelle à son score au premier tour.
* Les formes géométriques représentants les scores ne doivents pas se chevaucher et doivent remplir la totalité de l'espace disponible dans le canvas.
* Afficher à un autre endroit de la page web (en dehors du canvas) la liste des candidat ordonée par leur score obtenu. 
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
* Type de la représentation : Vertical slices treemap diagram. Dans un canvas, pour chaque candidat : un rectangle vertical plein (de couleur distinctes) dont la surface est proportionelle à son score au premier tour.
* Les formes géométriques représentants les scores ne se chevauchent pas et remplissent la totalité de l'espace disponible dans le canvas.
* La liste des candidat ordonnée par leur score obtenu est affichée à côté (version desktop) ou au-dessous (versions tablette et téléphone) du canvas.
* L"exercice ustilise des technologies web et est rendu au sein d'un seul fichier html.
* Le canvas aura l'id shapesCanvas.
* Les données seront récupérées par le client à chaque chargement de la page depuis l'API open data de Grand Poitiers sur le jeu de données Citoyenneté - Election Présidentielle - Poitiers 2022 - 1er tour - Résultats. 
* Le rendu est dynamique et prend en compte les données fraîches reçues depuis l'open data.
* L'API canvas est utilisée pour dessiner dans le canvas.
* Une fonction récursive de tri a été implémentée (pas d'utilisation de la méthode native Array.sort()).
* Le code est déposé sur git sur la plateforme github.
