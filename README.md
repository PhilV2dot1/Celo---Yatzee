# Celo---Yatzee

Contrat Celo Sepolia testnet : 0xF2Ea8Df89F8C7155b1A2B001f320f2473E7e2452


Fonctionnalités principales :
Gestion des parties :

creerPartie() - Créer une nouvelle partie et devenir le premier joueur
rejoindrePartie() - Rejoindre une partie existante (2 à 4 joueurs)
demarrerPartie() - Le créateur lance la partie une fois tous les joueurs présents
quitterPartie() - Quitter avant le début

Gameplay :

lancerDes() - Lancer les dés (jusqu'à 3 fois par tour), possibilité de garder certains dés
enregistrerScore() - Choisir une catégorie pour enregistrer le score du tour

Les 13 catégories de Yahtzee :

0-5: Uns, Deux, Trois, Quatre, Cinq, Six (somme des dés correspondants)
6: Brelan (3 identiques = somme de tous les dés)
7: Carré (4 identiques = somme de tous les dés)
8: Full (3+2 = 25 points)
9: Petite suite (4 consécutifs = 30 points)
10: Grande suite (5 consécutifs = 40 points)
11: Yahtzee (5 identiques = 50 points)
12: Chance (somme de tous les dés)

Fonctionnalités avancées :

Bonus automatique de 35 points si le total de la section supérieure (1-6) atteint 63+
Calcul automatique des scores selon les règles du Yahtzee
Détermination automatique du gagnant à la fin
Chaque joueur joue à tour de rôle

Consultation :

obtenirInfosPartie() - État actuel de la partie
obtenirScoreJoueur() - Scores détaillés d'un joueur

Nouvelles fonctionnalités :
Création de partie flexible :

creerPartie(nom, modeSolo) - Créer une partie solo (true) ou multijoueur (false)
Les parties solo démarrent automatiquement après création
Les parties multijoueur nécessitent toujours demarrerPartie()

Modes de jeu :

Mode Solo (1 joueur) : Jouez seul pour battre votre meilleur score
Mode Multijoueur (1-4 joueurs) : Affrontez jusqu'à 3 autres joueurs

Fonctions ajustées :

rejoindrePartie() vérifie maintenant que ce n'est pas une partie solo
demarrerPartie() accepte maintenant 1 joueur minimum
quitterPartie() interdit de quitter une partie solo
Les événements incluent l'information modeSolo

Bonus - Nouvelle fonction utile :

calculerScorePotentiel() - Permet de voir combien de points on obtiendrait dans chaque catégorie avant de faire son choix !
