to start this lesson please be familiar with the 
[Entry Terminonogy](https://www.reddit.com/r/sudoku/wiki/e-terminology/)

# Compressed Notation: (rN...cN...)
- Standard notation for cells is rx,cx when we dealing with 1 cell at a time.
- Compressed notation Combines cells from the same sector into 1 readable format by listing the changing sector. 
eg r1,c234: is indicating its using  cells 2,3,4  from row 1. 

![](%%r1c234%%)

# Compressed Box notation: (box,point)
 - Standard compression has limitation for expressing sets contained inside one box that are over multiple rows and cols. 
 - To Facilitate easy expressions of these style of we can use(Box,point) compression as a cardinal system 
 - Compress the cells via listing the Box first then a conjunction of points used 
 - b1p159  as an example is: r1c1,r2c2,r3c6 
 - Referenced as the following chart in the next image. 

||||  
:- | :-: | -:
1 | 2 | 3
4 | 5 | 6
7 | 8 | 9

![](%%cell01%%)


Symbols used in intermediate solving

    => implies
    <> not equal to    


# Set 
 - a collection of digits or cells 

# Hidden 
- A collection of digits obscured by other digits when using full pm's
- A hidden set can be any combination of 1-9 digits
- A hidden set uses whats left on for a sector cells. 

# Naked 
- A collection of digits that are exclusively left in cells 
- A Naked set can be any combination of 1-9 digits
- A Naked set uses whats left on in specific cells. 

# Locked set aka subset  
 - A collection of Cells that have the same number of digits

  - Mathematically:  N cells with N digits  whereby  any of these digits are exclusive limited to solving in one of these cells, when they are not then the puzzle would be invalid  as one cell or more would have no candidates left to place in it thus a puzzle construction rule violation. 

 - There is two types of locked sets: Naked & Hidden 

##  Hidden & Naked subsets : identifying names
- N is the subset size is (1 - 4): 
- N is any combination of 1-9 digits but with  N digits selected. 
- A collection of N cells that contain the N digits exclusively 
- N size has a name associated with it

N Size | subset Name 
:- | -: 
 1 | Single 
 2 | Pair
 3 | Triple
 4 | Quad

### Hidden Single 
- The first logic of reduction a player may discover when learning Sudoku
- These are found by a process of elimination of cells available to a sector 
- Start by selecting any Row,Col,Box and a single digit
- For each cell in that sector 
- Check each of its peers for the selected Digit if it is a Given, remove it from your list of cells 
- when one cell is left you have a Hidden Single as its the last spot for the Digit in the sector. 

*Example Puzzle:* 

............6..49194..8..53..142...6.5.....8.7...963..43..7..25875..3............

Hidden Single: r6c4 = 5 & r19c4,r4c6 <>5

![](%%hidden05%%)


### Naked Single 
- The second logic of reduction a player may discover when learning Sudoku
- These are found by selecting a cell and counting 1-> 9 by checking its peers for givens, if you skipped one number you found a Naked single and this goes in the cell you have selected as there is no other digit that could go here.
 
*If you are using Full Notation these are easier to spot then Hidden singles as a cell only lists one number, but as a manual player with no markups these are deceptively harder to spot.* 

*Example puzzle:* 

............6..49194..8..53..142...6.5.....8.7...963..43..7..25875..3............

 Naked Single: r4c8 = 7 & r5C79,r4c6,r9c8 <> 7 

![](%%naked07%%)

#### Hidden Pair
- The second level of subset logic of reduction a player may discover when learning Sudoku
- These are found by a process of elimination of cells available to a sector 
- Start by selecting any Row,Col,Box and a two digits
- For each cell in that sector 
- Check each of its peers for the selected Digit if it is a Given, remove it from your list of cells 
- when two cell is left you have a Hidden pair as its the last spot for these Digit in the sector. 

*Example puzzle:*

..94815..5.8...........689.32...4.8.87.132.4..9.8....2.8721........48..1..2679..8

Hidden Pair: 2,7 in r8c78 => r8c78<>3, r8c78<>6, r8c7<>9, r8c8<>5

![](%%hiddenpair27%%)

#### Naked pair
- The second Level of subset logic of reduction a player may discover when learning Sudoku
- These are found by selecting two cells and counting 1-> 9 by checking its peers for givens, if you skipped the same two numbers in two cells you found a Naked pair and these go into the cells you have selected as there is no other digits that could go here.

*If you are using Full Notation these are easier to spot then Hidden Pairs as a cell only lists these number, but as a manual player with no markups these are deceptively harder to spot.* 

*Example puzzle*

.7....254345927618862...73929....863.56.3..27738..2.45.17...592.832.547152....386

Naked Pair: 1,4 in r4c36 => r4c45<>1, r4c45<>4

![](%%nakedpair14%%)

##### Hidden Triple
- The third level logic of subset reduction a player may discover when learning Sudoku
- These are found by a process of elimination of cells available to a sector 
- Start by selecting any Row,Col,Box and three digits
- For each cell in that sector 
- Check each of its peers for the selected Digits if they are Given, remove it from your list of cells 
- when three cells are left you have a Hidden triple as its the last spot for these Digits in the sector. 
- note all three cells may not contain all three numbers, what matters is the same three cells are left. 

*Example puzzle*

.......89.68935.47.9781...6951........43596........95.....9876337.24.89...9..3...

Hidden Triple: 6,7,8 in r569c1 => r56c1<>2, r9c1<>1, r9c1<>5

![](%%hiddentriple678%%)

##### Naked Triple
- The third Level of subset logic of reduction a player may discover when learning Sudoku
- These are found by selecting three cells and counting 1-> 9 by checking its peers for givens, if you skipped the same three numbers in three cells you found a Naked Tripe and these go into the cells you have selected as there is no other digits that could go here.
- note: not all three numbers may be in the three cells, as long as there is three digits total among the three cells.
 
*If you are using Full Notation these are easier to spot then Hidden triples as a cell only lists these number, but as a manual player with no markups these are deceptively harder to spot.* 

*Example puzzle*

.98.4.563.328.5914..53..278276.8435..8.5....7.5....82682...3..55634.178...7.58.3.

Naked Triple: 1,7,9 in r46c4,r6c6 => r56c5<>1, r5c56,r6c5<>9, r6c5<>7

![](%%nakedtriple179%%)

###### Hidden Quad
- The forth level logic of subset reduction a player may discover when learning Sudoku
- These are found by a process of elimination of cells available to a sector 
- Start by selecting any Row,Col,Box and four digits
- For each cell in that sector 
- Check each of its peers for the selected Digits if they are Given, remove it from your list of cells 
- when four cells are left you have a Hidden quad as its the last spot for these Digits in the sector. 
- note all four cells may not contain all four numbers, what matters is the same four cells are left. 

*Example puzzle*

4.587...29286.41.7.....2....53....1...158.2...9....57.5..968321.....57.61..7234.5

Hidden Quadruple: 4,5,8,9 in r3c5789 => r3c5<>1, r3c589<>3, r3c78<>6

![](%%hiddenquad4589%%)

###### Naked Quad
- The forth Level of subset logic of reduction a player may discover when learning Sudoku
- These are found by selecting four cells and counting 1-> 9 by checking its peers for givens, if you skipped the same four numbers in four cells you found a Naked quad and these go into the cells you have selected as there is no other digits that could go here.
- note: not all four numbers may be in the four cells, as long as there is four digits total among the for cells
 
*If you are using Full Notation these are easier to spot then Hidden Quads as a cell only lists these number, but as a manual player with no markups these are deceptively harder to spot.*

*Example puzzle*

4.587...29286.41.7.....2....53....1...158.2...9....57.5..968321.....57.61..7234.5

Naked Quadruple: 1,3,6,7 in r3c1234 => r3c5<>1, r3c589<>3, r3c78<>6

![](%%nakedquad1367%%)

# Box - Line Reduction aka BLR 
- The Third level solving a Player may discover when learning Sudoku . 
- A collection of cells for one candidate that all cells for a sector are found in a single Box 
- There is two types of Box Line reduction applications: Claiming & Pointing 
- A Box Line Reduction is the introductory Level to [Fish](https://www.reddit.com/r/sudoku/wiki/fish-basics-terminology/#wiki_cyclopsfish_aka_box_line_reduction)

##Pointing candidates aka Locked Candidates Type 1 
- Happens when the cells land in the Box on one Row / Col with no other cells in the Box as options. 
- This indicates all the cells of the candidate are locked to the Row in the Box   
 then all  other cells of the Row / Col can be eliminated for this candidate 

*Example puzzle:* 

9..74......269.7.......2.9619..265745......8272.4...1365.2..1.9..196.8.5..9513.67

Locked Candidates Type 1 (Pointing): 3 in b2 => r3c1237<>3

![](%%pointing03%%)

##Claiming candidates aka Locked Candidates Type 2
- Happens when the cells land in the Box for one Row / Col with no other cells in the Row / Col as options. 
- This indicates all the cells of the candidate are locked to the Box by the Row   
 then all  other cells of the Box can be eliminated for this candidate 

*Example puzzle:* 

.......46.936.415..467.1329951238.6.437169582.6.547931.894.56...75..6.9.6.4.....5

Locked Candidates Type 2 (Claiming): 3 in r9 => r8c4<>3

![](%%claiming03%%)

# Bi - Location or Bi-local : { Terms are used interchangeably }
- Any sector that has two cells left for a candidate
- The first introduction of Strong link  [Discussed here](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_strong_link.3A)
 
*A Hidden Pair is found by finding two bi-locals in one sector using two different digits as they share the same two cells.*  

# Bivalve or Bi-Value: { Terms are used interchangeably } 
- Any cell with two candidates left 
- The second introduction to Strong Links [Discussed here](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_strong_link.3A)
- The smallest form of an Almost Locked Set [discussed here](https://www.reddit.com/r/sudoku/wiki/als-terminology/#wiki_smallest_als) 

*A Naked Pair is found by finding two bivalves with the same two candidates in one sector*

[next lesson: Intermediate Terminology](https://www.reddit.com/r/sudoku/wiki/I-terminology/)

