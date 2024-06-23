# jeux DODO

### Instructions de lancement en ligne de commande
#### 1. Pré-requis :
Avoir Pygame installé. Vous pouvez l'installer via pip : 
bash
  pip install pygame

#### 2. Lancer le script
- Ouvrez une ligne de commande 

- Exécutez le script avec la commande suivante :
bash
  python3 DODO.py 

### Méthodes/Algorithmes utilisés dans le projet
#### 1. Création de la grille hexagonale :
  Génère les coordonnées des centres des hexagones formant la grille.

    create_grid(grid_radius, hex_size) 

#### 2. Calcul des coins d'un hexagone :
Calcule les coins d'un hexagone à partir de son centre et de sa taille.

    hex_corner(center, size, i)
    
#### 3. Déplacement des pierres :
Génère des mouvements aléatoires pour le joueur bleu.

    random_player(empty_stones, blue_stones, hex_size)
Génère des mouvements aléatoires pour le joueur rouge.

    random_player1(empty_stones, red_stones, hex_size)

#### 4. Évaluation et génération des mouvements :
Évalue l'état du plateau de jeu : 

    evaluate_board(red_stones, blue_stones, hex_size)
Génère tous les mouvements légaux pour un joueur donné : 

    generate_legal_moves(stones, empty_stones, player, hex_size) 

#### 5. Algorithme Minimax :
 Implémente l'algorithme Minimax pour déterminer le meilleur coup pour un joueur donné : 

    minimax(red_stones, blue_stones, empty_stones, depth, is_maximizing, hex_size) 

#### 6. Vérification de la victoire :
 Vérifie si toutes les pierres d'une couleur sont connectées : 

    get_all_neighbors(move, empty_stones, stones, hex_size):

Détermine si un joueur a gagné en connectant toutes ses pierres : 

    get_winner(stones, move, hex_size): 

#### 7. Gestion du temps :
Arrête le jeu après 5 minutes : 
    
    force_shutdown() 

 Utilisation de ' threading.Timer ' pour mettre en place le minuteur de 5 minutes.

### Points forts du projet :
- #### Création dynamique de la grille hexagonale : 
Le script génère une grille hexagonale et place les pierres automatiquement.
- #### Utilisation de Pygame : 
Permet une interface graphique interactive.
- #### Gestion automatique des déplacements :
 Les joueurs (rouge et bleu) effectuent des mouvements de manière autonome.
- #### Évaluation des mouvements : 
Implémentation de l'algorithme Minimax pour la prise de décision.
### Déroulement du  jeu : 
après le l'exécution de la commande, le jeu commence et les jetons commence a de déplacer, le rouge qui commence après le bleu : 


### Points faibe du projet :
- #### Algorithme de décision simplifié : 
L'algorithme Minimax n'est pas pleinement utilisé pour les deux joueurs ; les mouvements sont majoritairement aléatoires.
- #### Abscence de stratégie pour que le joueur rouge gangne toujours
### déroulement du jeu : 
après l'exécution du jeu, le jetons rouge commence a se décplacer, après le bleu
![DODO1](https://github.com/ihssane20/ia/assets/166599798/956792a8-f29e-403b-8b6c-57b6917fff14) <br> 
lors du jeux il pourra s'ouvrir en fenetre comme si dessous, vous de devez cliquer sur Attendre et e jeu va continuer a jouer normalement. Après la fin du jeu le gagnant sera affiché sur le terminal et vous cliquer sur 'Forcer l'arret ' pour sortir du jeu :
![dodo2](https://github.com/ihssane20/ia/assets/166599798/e14f8f44-76df-4788-8149-46c7fb074333) <br>
dans le terminal, il s'affiche le temps des coups et à la fin il affiche le gagnant : <br>
![dodo3](https://github.com/ihssane20/ia/assets/166599798/7cbc9115-24ef-41a3-8dd4-a2fd45f89007) <br> 
# jeux GOPHER :
Exécutez le script avec la commande suivante :
bash
  python3 GOPHER.py 
### Méthodes/Algorithmes utilisés dans le projet
#### 1. Initialisation et configuration de Pygame :
 Initialise tous les modules Pygame : <br>
    
     pygame.init() 
Crée une fenêtre de jeu avec les dimensions spécifiées :  <br>

    pygame.display.set_mode((screen_width, screen_height))
Définit le titre de la fenêtre de jeu :  <br>

    pygame.display.set_caption('Gopher Game')

#### 2. Calcul des positions des hexagones
Calcule les sommets d'un hexagone à partir de son centre et de sa taille :

    hex_corner(center, size, i): 
 Crée une grille hexagonale basée sur les coordonnées axiales:
 
    create_grid(grid_radius, hex_size)
#### 3. Affichage des hexagones et des pierres
Dessine un hexagone à l'emplacement spécifié :

     draw_hexagon(center, size, color=BLACK)
Dessine une pierre (cercle) sur l'hexagone :

    pygame.draw.circle(screen, RED/BLUE, center, radius)
#### 4. Gestion des interactions de l'utilisateur
Trouve l'hexagone le plus proche de la position cliquée par l'utilisateur :

    find_closest_hex(pos)
 Retourne les coordonnées des hexagones adjacents :
 
    get_adjacent_coords(coord)
Retourne les coups valides pour le joueur actuel :

    get_valid_moves(player)
 Vérifie si le jeu est terminé en analysant les connexions des hexagones :
 
    check_game_end():
#### 5. Boucle de jeu principale
- Écoute les événements tels que pygame.QUIT et pygame.MOUSEBUTTONDOWN. <br>
- Met à jour l'état du jeu en fonction des clics de l'utilisateur. <br>
- Affiche la grille et les pierres à chaque itération de la boucle. <br>

### Points forts :
#### Interface graphique :
L'utilisation de Pygame pour dessiner les hexagones et les pierres offre une interface visuelle attrayante.
#### Validation des mouvements : 
Le projet implémente une logique pour valider les mouvements en fonction des connexions adjacentes.
#### Flexibilité de la grille :
La grille hexagonale est générée dynamiquement, permettant une personnalisation facile de la taille de la grille.

### Points faible :
- on peux jouer manuellement
- abscience de stratégie

## Déroulement du jeu : 
après le lancement du jeu, vous pouvez cliquer sur la grille et commencer a jouer : <br>
![gopher1](https://github.com/ihssane20/ia/assets/166599798/24455efb-23cb-4cb5-9ea6-cfb185afabb0)  <br>
vous continuer a jouer et pour chaque clique il va vous montrer les coups possible en vers que vous pouvez choisir : <br>
![gopher2](https://github.com/ihssane20/ia/assets/166599798/04010e91-91ba-4b55-83b3-54a23e90d8be) <br>
Le terminal affiche le gagnant a la fin du jeu : <br>










