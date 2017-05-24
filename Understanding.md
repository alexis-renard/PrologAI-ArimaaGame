# Compréhension du jeu

Les pièces sont placées aléatoirement sur le jeu

## Game state
Side : à qui le tour ? et quelles pièces capturées pour les deux camps

## Board
L'état du plateau :
[ligne, colonne, type, couleur]

On a un plateau de 8x8 indicée de 0 à 7

## Move
Retourner les 4 moves des pièces qui sont sous la forme :
[[ancienneposition],[nouvelleposition]]

# Elaboration des règles

## Règles préétablies :
Qui provoquent une erreur :
* Une pièce ne peut pas sortir du board
* Gestion des pièges et de la capture ok
* Le push est implémenté côté humain

### Todo
* Movement possible ?
    * N'est pas entourée d'une composition d'alliés et de bordures (une case adjacente est donc soit libre soit ennemie)
    * Il y a une piece ennemie
        * Est-elle plus forte ?
            * A-t-on un voisin allié ?
        * Est-elle bougeable ?
    * La case est donc libre, il peut bouger (si il a assez de step)

* Elle bouffe tout ce qui se trouve sur sa case d'arrivée
* Aucune contrainte de déplacement
* Du nombre de step par l'IA
* Pas de pousse possible si on a moins

### Done
* Récupérer tous les voisins d'une case
* Récupérer les pièces ennemies ou alliées  