# Projet-Info-CY-BER-PATH

Compte rendu du projet d'info 

Bonjour à tous bienvenue sur notre Github, Nous vous présentons notre projet scolaire nommé Cyber-Path.

Un projet nous est demandé par l'école CY-Tech. 
Ce projet est un jeu en 2D dont la grille de jeu est semblable graphiquement à pac man.
Il se base sur la prédiction d'un nombre de déplacement et le déplacement en lui même vers une cible. 
Il y a des priorités et un système de points.

(NOTICE) UTILISER LE CODE :
Télécharger le fichier .c
Allez sur le terminal et allez au répertoire du fichier
Tapez la commande gcc -o nom_executable nom_fichier.c
Tapez enfin ./nom_executable






ETAPE DU CODE :

Création d'une grille 2D : les murs des bordures, deux murs à chaque bordure, les joueurs, des cibles et des murs autours des cibles.  

Affichage de la grille : mise en beauté de la grille avec des couleurs.

Ensemble des règle des déplacements des joueurs : La manière dont il peut parcourir la grille avec les cibles et les murs.

Ensemble des règles de point : la distribution des points en fonction des accomplissements fait


FONCTIONS DU CODE :

initializergrille

displaygrille

movePlayer

playGame

main


REGLE DU JEU :

Nombre de joueur (max=4) : (à choisir)

Manche : (à choisir)

Prédictions des déplacement: (à choisir)

Effectuer un déplacment : (haut/h, bas/b, gauche/g, droite/d)

REGLE DE POINT : Si le joueurs atteint avec le bon nombre de coup, il gagne 2 points, si il l'atteint avec un nombre de coup inférieur à celui renseigné il perd un points, si il n'atteint pas sa cible à la fin de ses coups tous les autres joueurs gagne 1 points. Le gagnant est celui qui a le plus point.



////////////////////////


COMPTE RENDU :


Nous avions commencé le projet après les vacances de pâque nous étions au début perdu sur la manière de commencer notre projet 
(site ou logiciel à utiliser pour coder, par quelle fonction commencer et quelle seront les étapes ?).
On a finalemnt décider de coder sur le site en ligne onlinegdb et de sauvegarder à chaque mise à jour pour réutiliser une prochaine fois.

En discutant du jeu, en groupe de deux, on a d'abord pensé à la grille du jeu et la manière de le créer.
On a directement penser à un tableau à 2 dimmensions mais on ne savait pas quelle était la meilleur modélisation grilles.

tab[][]    =    ([][][][][][][][][][][][][])
		            ([][][][][][][][][][][][][])
		            ([][][][][][][][][][][][][])
		            ([][][][][][][][][][][][][])
		            ...

On a finalement choisi une grille avec 1 caractère pour 1 case.
On a su à ce moment que le tableau pourra poser plus de problème que prévu notamment pour les murs des cibles.


Ensuite on a pensé à mettre les cibles en les attribuant aux joueurs. On a fait attention à ce qu'ils ne touchent pas les murs du bord.
Les murs autours des cibles étaient une partie compliqué à mettre en place mais on a finalement réussi en faisant les 4 cas possibles.



Pour l'esthétique de la grille on a mis des couleurs similaire à pacman.(On n'a pas eu besoin de mettre des "define de couleurs". 

La position des joueurs n'étaient pas très difficile.
En revanche les erreurs bêtes nous mettaient en difficulté comme les '' pour un caractère, la déclaration de type et certaines fonctions ne marchaient pas car on s'y prennait mal ou
parce qu'il y avait des instructions qu'on devait chercher.

Ex: Le Robot (Joueur) traversait les murs -> ajouter une d'autre condition sur la règle de déplacment.

On a cherché le moyen d'effacer la grille dans le terminal grâce à la fonction system("clear") et le type "static" sur le site StackOverflow.
Pour la couleur on a demandé au professeur de td.

Pour finir on a mis en place la robustesse dans les derniers jours avant le délais.
