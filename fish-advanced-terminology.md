Welcome to the pond and a wonderful collection of Fish species and their similarities and subtle differences.

When finished reading this adventures guide hopefully you will be equipped with enough tackle and skilled lines thrown to haul in your first Advanced level fish with some specialty fishing equipment the gaffer & wearing your new fancy hip waders introduced in this topic.   

# Expanding Select-able sectors
* In the last chapter it was discussed using mixed types: Box,Row,Col with no reusable cells in the base. 
* This chapter will expand it by allowing overlapping cells in the Base. 

* With the allowing overlapping cells with mix and matching Row,Col,Box our Base,Cover selector needs some adjusting for this level of fish discussion to keep it simpler and easier follow.

### Base Sector
   - Any Row or Col or Box is selected for a digit
   - Reusing cells is allowed however they must be coloured / marked to identify them

### Cover sector
  - Every cover set used must have at least 1 cell from the base sectors picked.
  - No base sector may be repeated as a cover. 
  - Overlapped base cells only change colour if its covered twice. 

* This chapter will introduce the last special property caused by overlapping Base cells    

# Special Qualities 
  - A n x n fish with base cell(s) not covered completely due to overlaps
  - These coloured cells have a name: Endo Fin 

# Endo Fin
 * When a fish is constructed using a variety of sectors base cells can be used multiple times.
 * When they are used multiple times they increase the counts of n/n math and if they are not accounted for multiplicative our math formula doesn't work.
* To make sure they are accounted for we mark them a different colour, and when adding cover sectors covering it once isn't enough to change it "green" to keep track of it 

# Using endo fins,
- they act the same as sashimi/Finned cells the eliminations can only be within its peers
- so put on your hip waders and climb in the water and lift that big fish out
- yes a endo fish might even be big enough you need both hip waders and a Gaffer to land it
- thankfully since they both use the same rules we can combine them into one process.

### Naming of Fish:
- listed in order
* 1. Special Qualities: (endo)Finned or Sashimi,  {endo name is often skipped in solvers} 
* 2. Shape : if non basic, and N > 1
* 3. Name for N size.
 * note: All Named Aics: Skyscraper,Empty Rectangle, 2-string kites; are all finned or sashimi size 2 fish 

# Colouring for Fishing for Finned / Sashimi / Endo   
* The best approach and fail safe method for Fishing is to uses highly visible Tackle.  
* Pick 6 colours { for reference i will use }
  - Base: = Blue, 
  - Base overlaps: Dark blue
  - Cover:= Red, 
  - Vertices: = Green 
  - Finned cells :  Purple
  - Peers of Finned Cell:  Orange

## Using Colours: updated
  * Pick a Digit {your tackle} the number you will use for this whole process.
  * Pick a Size  { N  the number of Lines to cast} 
  * Cycle each N Base sectors one at a time.  
    - Colour every cell Blue, {that has the digit your after}
    - if the Digit is blue change it to Dark Blue 

  * Cycle N Cover sectors
       - Colour every Cell Red,{that has the digit your after}
          - If the cell is coloured Blue change it to Green
          - if the cell is coloured Dark blue change it to Blue 
  * Check your Net: { Vertices }    

 ### Basic                     
- if all blue cells are Green you have N vertices for N sectors thus your net is full and ready to Haul in 

#### Basic Colour Eliminations
- When the net is full:
- all Red cells are exclusions for the digit selected 

### finned/sashimi/endo 
* if there is only Blue cells left you may have a finned/sashimi/endo
* highlight the remaining Blue cells Purple
* Select all red cells that are peers of all Purple cells, change their colour to Orange. 

- if there is only Purple and Green cells for the base, then we can gaff this fish for targeted eliminations (orange cells). 

#### Gaffed Colour eliminations: 
- all orange Cells are exclusion for the digit selected. 
       
- if the finned/sashimi/endo fish still doesn't work add another N if you can.    

## Proof 
  - Try placing one of the eliminations, doing so one of sectors will have no candidates left to place: a construction rule violation.
  
# Working Logic: Fishing Expedition
* The following is a smattering of examples to show how it works 

 ## (endo) Finned Mutant Jellyfish  
*Example Puzzle: 

..18326.483.....7226....3.86.8.1.42...32.48..142.857.932...8.4..1.423.8.48.1962..

- Finned Mutant Jellyfish: 5 r18c3b3 c78b17 efr1c8 => r59c8<>5
- Tackle: "5"
- N = 4
- Special Char: (Endo)Finned
- Shape: Mutant
- Base r18c3b3 :  (r1c12,r8c17,r39c3,r2c7,r3c8 ) Blue , Dark blue (r1c8)
- Cover c78b17: (r59c8) red,change ( r1c12,r8c17,r39c3,r2c7,r3c8) to green, and change (r1c8) to blue
- Finned: (r1c8 ) change to purple
- Gaffed: ( r59c8) change to orange
- Eliminate: ( r59c8) <> 5

## endo Finned + Finned Mutant Jelly fish
*Example Puzzle: 

..18326.483.....7226....3.86.8.1.42...32.48..142.857.932...8.4..1.423.8.48.1962..

- Finned Mutant Jellyfish: 5 r18c37 c1b139 fr9c3 efr8c7 => r9c89<>5
- Tackle: "5"
- N = 4
- Special Char: (Endo)Finned, Finned 
- Shape: Mutant
- Base r18c37 :  (r1c128,r8c1,r39c3,r2c7) Blue , Dark blue (r8c7)
- Cover c1b139: (r5c5,r3c8,r9c89) red,change (r1c128,r8c1,r3c3,r2c7) to green, and change (r8c7) to blue
- Finned: ( r9c3,r8c7) change to purple
- Gaffed: ( r9c89) change to orange
- Eliminate: ( r9c89) <> 5

#  Tips and Tricks
 * All the tools up to this point when used and practice can land massive fish with no problem

* Finding and constructing them is another matter: the following tips may help reduce the search
 
     * Fish finding tips: 

  - Basic type fish : Base sectors will only have N cells
  - Fish that use base sectors as boxes these sectors can have N+4 cells 
  - size 1 fish base sector may have n+2 cells  
  - Finned/sashimi fish for size  2, only 1 base sectors may have N+2 cells
  - Finned/sashimi fish for size >2 , only 2 base sectors may have N+2 Cells
  - + cells are confined to one box with 1 other base cell for the selected sector. 
  
# Closing Comments 
  - I wouldn't worry about Finding any fish beyond Size Four

  - Everything past size 4 is academic, and usually requires good solving aids and sometimes code to find it. 
  
  - Almost every fish beyond size 4 has been shown to have a smaller complimentary fish in the opposites sectors 

   - eg  squirmbag in rows there's one of these sword / jelly / xwing / blr in cols that does the same elimination. 

   - very few fish have no known smaller eliminations and often the puzzle solves easier with other tools, then searching for the largest fish.

* Largest known Fish with no smaller fish  is a:  7x7  endo + finned monster.
 
* a computer takes 15 minutes to construct it~ 

- Finned Mutant Leviathan: 7 r1458c16b7 r2c2389b58 fr1c5 efr9c1 => r9c5<>7

6.23.915..3.2....6954.16.3.26.5.43.141..235..5.31.....3..4.2.1584..3.6...2....4.3


Fish was designed to explain template omissions: there is cases that do not have answers as a Fish the next topic covers this [here](https://www.reddit.com/r/sudoku/wiki/Fish-Expert-terminology)

