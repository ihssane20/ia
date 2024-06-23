# jeux DODO

### Instructions de lancement en ligne de commande
#### 1. Pré-requis :
Avoir Pygame installé. Vous pouvez l'installer via pip :
bash
  pip install pygame

#### 2. Lancer le script
=> Ouvrez une ligne de commande 

=> Exécutez le script avec la commande suivante :
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
dans le terminal, il s'affiche le temps des coups et à la fin il affiche le gagnant : *



