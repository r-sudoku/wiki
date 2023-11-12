[Automorphism](https://en.wikipedia.org/wiki/Automorphism)

Question that comes up in Sudoku mathematical study:

 * How are two puzzles identical to each other when they appear to be completely different but identified as [isomorphism](https://www.reddit.com/r/sudoku/wiki/index/issomorphism/)  

 * The answer for this question lies within Transformations: 

 * There is 2*6^8 (3,359,232) ways to transform a grid, which preserves the singular solution of the grid. 

# The ways to transform a grid: 
- Transpose - Rows(1-9) and Col(1-9) exchange 
- Bands (1,2,3) a collection of 3 rows are exchanged 
- Stack (1,2,3) a collection of 3 cols are exchanged 
- Row (123,456,789) a collection of 2-3 rows in the same band are exchanged. 
- Col (123,456,789) a collection of 2-3 Cols in the same stack are exchanged

# [Symmetrical properties:](http://forum.enjoysudoku.com/about-red-ed-s-sudoku-symmetry-group-t6526.html#p65454)

* all known Sudoku grid symmetrical identifiers (122 classes) are super-classed in the following 6 types: 

* these example are replicated by applying combinations of Transpose, Stack,Band, row, col: 
 * meaning they do not needs additional identifies to confirm they exist.

## Rotational Symmetry: 
 - Horizontal Mirror:  replicated as stack(1,3),row(1,3),row(4,6),row(7,9)
 - Vertical Mirror:    replicated as Band(1,3),col(1,3),col(4,6),col(7,9)
 - 90 degree Rotation: 
 - 180 degree Rotation 

## Diagonal Symmetries 
  - Diagonal Reflection 
  - Anti-diagonal Reflection

## Fixed Boxes
## Boxes move in bands
## Boxes move Triangular
## Sticks Symmetry
  
 
# How to use Automorphism

* First, we cycle all Transformation properties of a grid

* Next we perform digit exchanges: comparing transformed puzzle B to A if the cells 
contain different digits in B we swap the digits of B to A repeat for all cells

* Then compare all cells of A to B: 

* If they all contain the same digit, then the newly transformed puzzle(B) can be said to be Automorphic to starting puzzle: meaning they can change into each other.

# The Most canonical Grid 
* Example
123456789456789123789123456231564897564897231897231564312645978645978312978312645

* has 648 Automorphic identities 
  
Automorphism is the key factor used to determine the total number of unique solution Sudoku grids by mapping the number of automorphic cells in all possible grid arrangements
