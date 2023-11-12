A recap and extensions on the Terms covered [here](https://www.reddit.com/r/sudoku/wiki/b-terminology/#wiki_locked_set_aka_subset)
 
# Locked set aka subset  
 - A collection of N Cells that have the same N Digits 

  - Mathematically:  N cells with N digits  whereby  any of these digits are exclusive limited to solving in one of these cells, when they are not then the puzzle would be invalid  as one cell or more would have no candidates left to place in it thus a puzzle construction rule violation. 

 - There is two types of locked sets: Naked & Hidden 

##  Hidden & Naked subsets : identifying names
- N is the subset size is (1 - 9): 
- N is any combination of 1-9 digits where N are  selected. 
- A collection of N cells that contain the N candidates exclusively 
- N has a name associated with it everything passed size 4 is rarely if ever used

N Size | subset Name 
:- | -: 
 1 | Single 
 2 | Pair
 3 | Triple
 4 | Quadruple
 5 | Quintuplet
 6 | Sextuplet
 7 | Septuplet
 8 | Octuplet
 9 | Nonuplets

# Hidden 
- A collection of digits obscured by other candidates when using full pm's
- A hidden set can be any combination of 1-9 digits
- A hidden set uses whats left on for a sector. 

## How a Hidden subset works
 - Identify a sector with N Cells with N Digits 
 - The N Cells are restricted to satisfying these Digits
 - Remove all cells of the set from all other digits in the sector

# Naked 
- A collection of candidates that are exclusively left in cells 
- A Naked set can be any combination of 1-9 digits
- A Naked set uses whats left on in specific cells. 

## How naked subset work
 - Identify a sector with N digits in N cells 
 - The N Digits are restricted to satisfying these cells 
 - Remove all Peers of each Digit in subset

The reason we do not use size greater then 4 is from the nature of Sudoku puzzles 

There is always an equal balance in Naked and Hidden sets in every sector
 - a  Naked Pair has a hidden septuplet for 9 digits in 9 cells
 - a  Naked quintuplet has a hidden quadruple for 9 digits in 9 cells
 - Given & Solved Digits are a Naked set. 

From this we can see  the reasons why we don't search past size 4 for either hidden or naked subsets although they are possible.

