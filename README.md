# Sudoku Generator in pygame

<p align="center" >
   <a href="">
    <img alt="react-native-gifted-chat" src="https://media.giphy.com/media/PkirsH2XFiLrZ3iofH/giphy.gif" width="900" height="510" />
 </a>

</p>

<h3 align="center">
  🔢 Générateur du sudoku
</h3>
<p align="center">
  Générateur du Sudoku sur l'interface pygame <br/>
  <small></small>
</p>

## Manuel d'utilisation

- Lancer la commande "python ./pysat/src/sudoku.py ./pysat/src/rules.cnf"
- A chaque éxécution la grille est différente car elle est générée aléatoirement
- Pour toutes modifications:
  - __screenSize__ = Taille de la fenêtre
  - __cellSize__ = Taille d'une case du sudoku
 
    
   
    
    
    

## Détails de l'implémentation de la génération de sudoku


Une brief description de l'algorithme de génération de sodoku : 
- On place aléatoirement un nombre de chiffre (par défaut entre 1 et 3 mais il suffit de modifier la variable num_clauses) sur une grille et on appel le solveur pour la résoudre (on réitère tant que le solveur n'as pas de solution)
- Une fois la solution trouvé, on récupère tous les chiffres positifs du solveur qui représente les coordonnées de la solution
- On place dans un tableau la négation de la solution
- On instantie ensuite un nouveau solveur avec une grille au départ vide (sans clauses) qui va regarder s'il existe des solutions (la solution originale est en négation)
- Tant que des solution différentes de la solution originale existe :
  - On vas ajouter une clause, c'est à dire, une position de la solution originale dans celle que nous sommes en train de créer
  - On vas mettre en négation les positions restantes (celles que l'on a pas mis en clause)
  - On réitère




## License

- [MIT](LICENSE)

## Contributors

- Nicolas Martin
