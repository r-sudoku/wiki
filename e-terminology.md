# A Sudoku Grid 
-  a 9x9 matrix of Row,Col,Box  that each house the digits 1 through 9 once. 

# Cell 
- There is 81 cells on a 9x9 sudoku grid listed as a cordial system of Row, Column  (R,C)  or (r,c)
- Every cell represents the junction of three units as it lies in one row, one column, and one box. 
- rx,cx   - where x is values 1-9  
- exemplar:  r1c1 represents the first cell in the upper left hand corner
- exemplar:  r9c9 represents the last cell in the bottom right  hand corner

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |9
r2 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18
r3 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 
r4 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36
r5 | 37 | 38 | 39 | 40 | 41 | 42 | 43 | 44 | 45
r6 | 46 | 47 | 48 | 49 | 50 | 51 | 52 | 53 | 54
r7 | 55 | 56 | 57 | 58 | 59 | 60 | 61 | 62 | 63
r8 | 64 | 65 | 66 | 67 | 68 | 69 | 70 | 71 | 72
r8 | 73 | 74 | 75 | 76 | 77 | 78 | 79 | 80 | 81

![](%%grid01%%)

# Box  aka Block
- Read left to right top down  there is 9 boxes on a Sudoku grid
- B1 is the top leftmost and B9 is the bottom rightmost, 
- Abbreviated  as B or b 
- A box is the cells found within a 3x3 matrix of row/cols intersecting in the same band & stack.

# Row    
-  Read top down there is 9 rows on a Sudoku grid  
-  R1 is the top row, and R9 is the bottom row. 
-  Abbreviated  as R or r 

# Column  {Col}
-  Read left to right  there is 9 columns on a Sudoku grid 
-  C1 is the leftmost column, and C9 is the rightmost column. 
-  Abbreviated  as C or c 

*Row,Col,Box lay out with numbers in the cells for the box they belong to.*

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 
r2 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3 
r3 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 3  
r4 | 4 | 4 | 4 | 5 | 5 | 5 | 6 | 6 | 6 
r5 | 4 | 4 | 4 | 5 | 5 | 5 | 6 | 6 | 6 
r6 | 4 | 4 | 4 | 5 | 5 | 5 | 6 | 6 | 6 
r7 | 7 | 7 | 7 | 8 | 8 | 8 | 9 | 9 | 9 
r8 | 7 | 7 | 7 | 8 | 8 | 8 | 9 | 9 | 9 
r9 | 7 | 7 | 7 | 8 | 8 | 8 | 9 | 9 | 9 

![](%%grid03%%)

# Band  aka Chute
- There is 3 bands on a sudoku grid they are formed as a horizontal collection of 3 rows: [ 1,2,3] , [ 4,5,6 ] , [7,8,9]  covering 3 boxes

# Stack aka  Tower 
- There is 3 stacks on a sudoku grid they are formed as a vertical collection of 3 Cols: [ 1,2,3] , [ 4,5,6 ] , [7,8,9] covering 3 boxes

# Sector aka  House or Unit 
- An unspecified area of 9 cells that must contain all 9 digits. 
- There are 27 sectors in the grid. 
- This may refer to a row, col or Box. 
- Commonly used when communicating a technique that can apply to any type of unit without having to say all three. 

# Given(s)  or Clue(s)
- The clue(s) provided at the start of the puzzle. 

# Grid String 
- 81 characters listed in cell order 1 to 81 
- Spaces or "." or "0" - represents an empty cell 
- Digit listed are the Given for that cell. 
- This is the {varying} position of an unsolved Sudoku 
eg: 
............64519.....8..575....17..2.84573.9..48....149..6.....76534............
- Useful for directly coping into a solving aid. 

# Digit 
- All big numbers that are either given or solved as known solutions.

# Candidate 
- A potential digit solution to a cell notated by a small number.

# Elimination 
- The removal of a candidate which has been determined cannot be true.

# Peer aka See 
- all cells of a sudoku grid  have exactly:  1 row,  1 col,  1 box that it belongs to.
- all cells that have the same: row,col,box are peers 
- each cell has 20 peers 

*exemplar: cell 1 @ r1c1 has the following peer cells: 2,3,4,5,6,7,8,9,10,11,12,19,20,21,28,37,46,55,64,73  
 { all the cells not crossed off}*

![](%%grid02%%)

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 | * | 2 | 3 | 4 | 5 | 6 | 7 | 8 |9
r2 | 10 | 11 | 12 | | | | | | 
r3 | 19 | 20 | 21 | | | | | | 
r4 | 28 | | | | | | | | 
r5 | 37 | | | | | | | | 
r6 | 46 | | | | | | | | 
r7 | 55 | | | | | | | | 
r8 | 64 | | | | | | | | 
r8 | 73 | | | | | | | | 

# Pencil Markup {pm} aka Full Notation  or Potential markup
- Cycling each of the 81 cells, one at a time 
- Checking this cells 20 peer's for Givens and making a note in the cell for what isn't given 
- Represents Potential candidates that could be solved in the cell. 

*example:*  

............64519.....8..575....17..2.84573.9..48....149..6.....76534............

- r2c1: checking its peer cells  you will find Digits: 1,2,4,5,6,9 as Given
- Thus r2c2 has Pm of 3,7,8  { the numbers we didn't find}

![](%%grid04%%)

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 |   |   |   |   |   |   |   |   |
r2 | 378  |   |   | 6 | 4 | 5 | 1 | 9 |    
r3 |   |   |   |   | 8 |   |   | 5 | 7  
r4 | 5 |   |   |   |   | 1 | 7 |   |  
r5 | 2 |   | 8 | 4 | 5 | 7 | 3 | 6 | 9  
r6 |   |   | 4 | 8 |   |   |   |   | 
   | 
r7 | 4 | 9 |   | 6 |   |   |   |r8 |   | 7 | 6 | 5 | 3 | 4 |   |   | 
r8 |   |   |   |   |   |   |   |   | 

# Candidate display sequence in a cell
 - how we list pencil marks in a cell for easy reading
 - its in a 3x3 matrix keypad style. 

||||   
:- | :-: | -:
1 | 2 | 3
4 | 5 | 6
7 | 8 | 9

*like this* 

![](%%cell01%%)

# Meticulous note taking 
 - Every starting Digit in the starting Grid string effects all three sectors:  Box,Row,Col 
 - Every Cell Solved as your progress from the starting in the Grid string also affects sectors:  Box,Row,Col
 - Don't forget to update your PMs as you solve Cells by removing that placed Digit from affected sectors.  

[next lesson: Beginners terminology](https://www.reddit.com/r/sudoku/wiki/B-terminology/)

