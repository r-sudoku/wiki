Welcome to fishing across the Pond, as previously discussed in [basic fishing](https://www.reddit.com/r/sudoku/wiki/fish-basics-terminology/)
  fish was designed to relatively easily explain template omissions.

* Through exhaustive testing and searching variable grid layouts it was determined some of these patterns have no-fish explanations, the list is short.

* Many attempts to Rectify this small problem lead to the discovery of a few methods to explain the eliminations. 
  
* One of the best methods affectionately called: NxN+K fish, created by  [Obi-Wahn](http://forum.enjoysudoku.com/about-the-arithmetic-of-ultimate-fish-t5256.html#p41058) 

# N x N + K Fish 
* This technique solves a few of the no-fish puzzles, moreover the best part of this method as discussed here in is the way it handles all Fish. 
* It no longer relies on Finned, Sashimi, Endo fins in the determination of Fish eliminations. 
* Instead it adds Finn Sectors, simply put extra covers represented as K
* This method implores simplistic math that's easy to use & best done in excel

# Setup for N x N + K fish
* just like basic fish it uses base sectors and cover sectors with some differences

## Base Sector 
  * Choose N base sectors
  * Any sector may be selected 
  * Sectors may be repeated 

## Cover Sectors 
  * Choose N covers 
  * Any sector may be selected 
  * Sectors may be repeated 
  * Adding more covers past N size is the value of K. 

## using base sectors 
 * pick a digit
 * setup a table in excel with 81 cells {label it base}
 * for each sector selected mark a "1" in the corresponding cell in the table for all the cells of the sector.  
 * if a cell already has a "1" increase it by 1

## using Cover sectors 
 * same digit as the base
 * setup a second table in excel with 81 cells
 * for each sector selected mark a "1" in the corresponding cell in the table for all the cells of the sector.  
 * if a cell already has a "1" increase it by 1

# Construction rule: 
 * We have a Fish pattern if we can construct two sets of sectors, a base set and a cover set, in such a way that every candidate of a given digit belongs to at least as many cover sectors as it belongs to base sectors.

# Calculating K value 
 * Number of fin sectors(K) = Number of cover sectors - Number of base sectors

*With this convention the second rule simply is:

# Exclusion rule: 
 * Any candidate of the digit in question, whose individual excess number of cover sectors is greater than the number of fin sectors(k) in the pattern, can be eliminated.

# math Proof

    for any specific digit,
    a "fish" of order j
    is defined by a "base" of j units
    and a "cover" of j units,

    where the observation is —
    A. each unit of the "base" can only have the digit somewhere in the "cover", and
    B. the digit cannot occur in the overlap of units of the "base" 

    thus we know that the "base" will provide the digit j times in the "cover",
    and the conclusion is —
    exclude the digit in the "cover" outside the "base"


    beyond the "fish" exclusion,
    if there's overlap in the "cover" 
    we have an extra type of exclusion —
    exclude the digit in the overlap of units of the "cover";

    NxN+K extends this new type of exclusion
    by considering order j\J,
    where the "cover" is increased to J units ( j < J )


## Application 
* set up a math table of 81 cells 
* for each cell in the math table  using the same cells do a ( base - cover)

## Reading the math table 
 * all negative numbers cannot have a digit in it
 * if it does the fish is invalid, add more covers and or bases 

### Eliminations - math table. 
  * Where K comes into play

  * K has no value 
     - All positive numbers are the exclusions

  * K has a value
      - All positive numbers  greater then  K are the exclusions

That's it, the beauty is the reusing base sectors and covers allows it to build fish otherwise not possible.

## Working Logic: 
* Now, to give an example I'll show how to calculate the hidden pattern from a list of base and cover sectors.
* I'll take a pattern from The  [Ultimate FISH Guide:](http://forum.enjoysudoku.com/the-ultimate-fish-guide-t4993.html)  r348c8b1 / r12c567b9.
* This pattern has 5 base and 6 cover sectors and therefore K = 1 

Now the number of base sectors / cover sectors for each possible candidate are:

     1/1 1/1 1/1 | 0/1 0/2 0/2 | 0/2 1/1 0/1
     1/1 1/1 1/1 | 0/1 0/2 0/2 | 0/2 1/1 0/1
     2/0 2/0 2/0 | 1/0 1/1 1/1 | 1/1 2/0 1/0
    -------------+-------------+-------------
     1/0 1/0 1/0 | 1/0 1/1 1/1 | 1/1 2/0 1/0
     0/0 0/0 0/0 | 0/0 0/1 0/1 | 0/1 1/0 0/0
     0/0 0/0 0/0 | 0/0 0/1 0/1 | 0/1 1/0 0/0
    -------------+-------------+-------------
     0/0 0/0 0/0 | 0/0 0/1 0/1 | 0/2 1/1 0/1
     1/0 1/0 1/0 | 1/0 1/1 1/1 | 1/2 2/1 1/1
     0/0 0/0 0/0 | 0/0 0/1 0/1 | 0/2 1/1 0/1 

 Since we're only interested in the excess number of cover sectors we can subtract the base numbers from the cover numbers:

      0  0  0 | +1 +2 +2 | +2  0 +1
      0  0  0 | +1 +2 +2 | +2  0 +1
     -2 -2 -2 | -1  0  0 |  0 -2 -1
    ----------+----------+----------
     -1 -1 -1 | -1  0  0 |  0 -2 -1
      0  0  0 |  0 +1 +1 | +1 -1  0
      0  0  0 |  0 +1 +1 | +1 -1  0
    ----------+----------+----------
      0  0  0 |  0 +1 +1 | +2  0 +1
     -1 -1 -1 | -1  0  0 | +1 -1  0
      0  0  0 |  0 +1 +1 | +2  0 +1 

 Now every cell with a negative number must be empty, 
 because a candidate there would violate the construction rule. 
 Since we have a K value of 1, in this case every candidate with an excess number of at least +2 can be eliminated. This leads to the following pattern:

     . . . | . * * | * . .
     . . . | . * * | * . .
     / / / | / . . | . / /
    -------+-------+-------
     / / / | / . . | . / /
     . . . | . . . | . / .
     . . . | . . . | . / .
    -------+-------+-------
     . . . | . . . | * . .
     / / / | / . . | . / .
     . . . | . . . | * . .


    / = empty cell
    . = cell may or may not contain a candidate
    * = possible exclusions

On ward in learning is making presentation more compact featured in the [next level of fish](https://www.reddit.com/r/sudoku/wiki/fishing-professional-terminology/)

