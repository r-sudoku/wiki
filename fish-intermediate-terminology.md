Welcome to the pond and a wonderful collection of Fish species and their similarities and subtle differences.

When finished reading this adventures guide hopefully you will be equipped with enough tackle and skilled lines thrown to haul in your first intermediate level fish with some specialty fishing equipment the gaffer.  

# Expanding Select-able sectors
* In the last chapter it was discussed using only 1 type of Base or Cover
* This chapter will expand it to mixing: Box,Row,Col types for: Franken,mutant

## Shape of Fish:
* 1. Basic: N row sectors x N column sectors or vv.
* 2. Franken: N (rows+box) sectors x N (columns+box) sectors or vv. 
* 3. Mutant: N sectors x N sectors (That is not Basic nor Franken )

* With the unlocking of mix and matching Row,Col,Box our Base,Cover selector needs some adjusting for this level of fish discussion to keep it simpler and easier follow.

### Base Sector
   - Any Row or Col or Box is selected for a digit
   - No cells may be reused 

### Cover sector
  - Every cover set used must have at least 1 cell from the base sectors picked.
  - No base sector may be repeated as a cover. 

* In the last topic it is discussed via [colouring methods](https://www.reddit.com/r/sudoku/wiki/fish-basics-terminology/#wiki_colouring_for_fishing) to check for valid fish
* Non usable fish  have blue cells still showing from the base sectors
* There is two ways to cover these blue cells, 
 * Increase the size of the fish as suggested in the last chapter 
 - or 
 * As this chapter will show another method: Recognizing special qualities

# Special Qualities 
  - A n x n fish with blue cell(s) not covered 
  - these blue cells have a names depending on how they are positioned: Finned, Sashimi

## Finned Fish
  * A collection of blue cells.

## Sashimi Fish
 * A collection of blue cell(s) that: 
 * in the absences of all blue cells these fish will degenerate through basic techniques and/or smaller fish and still have the same exclusions.

### Naming of Fish:
- listed in order
* 1. Special Qualities: Finned or Sashimi
* 2. Shape : if non basic, and N > 1
* 3. Name for N size.

* note: All Named Aics: Skyscraper,Empty Rectangle, 2-string kites are all finned or sashimi size 2 fish" 

 ### Gaffing finned/sashimi fish
   - these fish are too big to fit in your net 
   - the only way to net these fish is to bring out the specialized tool for a precision strike: 
   - to Gaff a finned/sashimi fish we use the peers of the blue cells. 
   - Peer cell(s) to all blue cells may be eliminated from the focused strike on the blue cells.

# Colouring for Fishing for Finned / Sashimi  
* The best approach and fail safe method for Fishing is to uses highly visible Tackle.  
* Pick 5 colours { for reference i will use }
  - Base: = Blue
  - Cover:= Red 
  - Vertices = Green
  - Finned cells  - Purple
  - Peers of Finned Cell - Orange 

## Using Colours: updated
  * Pick a Digit {your tackle} 
  * Pick a Size  { N  the number of Lines to cast} 
  * N Base sectors - Colour every cell Blue, that has the digit your after
  * N Cover sectors - Colour every Cell Red, that has the digit your after 
      - If the cell is coloured Blue change it to Green 
  * Check your Net: { Vertices }

### Basic                     
- if all blue cells are Green you have N vertices for N sectors thus your net is full and ready to Haul in 

#### Colour Eliminations
- When the net is full:
- all Red cells are exclusions for the digit selected. 

### finned/sashimi 
* if there is any blue cells left you may have a finned/sashimi 
* highlight the remaining Blue cells Purple
* Select all red cells that are peers of all Purple cells, change their colour to Orange. 

- if there is only Purple and Green cells for the base, then we can gaff this fish for targeted eliminations (orange cells). 

#### Gaffed Colour eliminations: 
- all orange Cells are exclusion for the digit selected. 
       
- if the finned/sashimi fish still doesn't work add another N if you can.    

## Proof 
  - Try placing one of the eliminations, doing so one of sectors will have no candidates left to place: a construction rule violation.   


# Working logic: Fishing Expedition
* The following is a smattering of examples to show how it works

## Skyscraper 
* A combination of 2 sashimi x-wings
* Example puzzle

..47.5...29....15..5891....52.49861....5.1...9.1.3..85..2856931..9...546..5149872

  Sashimi X-Wing: 6 c34 r25 fr6c4 => r5c5<>6

- Tackle : " 6 "
- N = 2
- Special char: Sashimi 
- Shape: Basic
- Base c34: ( r25c3,r26c4 ) blue
- Cover R25: ( r5c6 ) red & changes ( r2c34,r5c3 ) to Green
- Vertices: ( r2c34,r5c3 ) green, blue cells ( r6c4 )
- Sashimi: (r6c4) change to purple
- Gaffed:  (r5c5) changes to orange
- Eliminate: ( r5c5 ) <> 6

 Sashimi X-Wing: 6 c34 r26 fr5c3 => r6c2<>6 

- Tackle : " 6 "
- N = 2
- Special char: Sashimi 
- Shape: Basic
- Base c34: ( r25c3,r26c4 ) blue
- Cover R25: ( r6c2 ) red & changes ( r2c34,r5c3 ) to Green
- Vertices: ( r2c34,r6c4 ) green, blue cells ( r5c3 )
- Sashimi: ( r5c3 ) change to purple
- Gaffed:  ( r6c2 ) changes to orange
- Eliminate: ( r6c2 ) <> 6 

## Finned X - wing
* Example puzzle

..47.5...29....15..5891....52.49861....5.1...9.1.3..85..2856931..9...546..5149872

- Finned X-Wing: 6 c35 r25 fr1c5 => r2c4<>6
- Tackle : " 6 "
- N = 2
- Special char: Finned
- Shape: Basic
- Base c35: ( r25c3,r125c5 ) blue
- Cover R25: ( r2c4 ) red & changes ( r25c3,r25c5 ) to Green
- Vertices: ( r25c3,r25c5 ) green, blue cells ( r1c5 )
- Finned:  ( r1c5 ) change to purple
- Gaffed:  ( r2c4 ) changes to orange
- Eliminate: ( r2c4 ) <> 6

## 2 - String Kite
* Example puzzle 

..47.5...29....15..5891....52.49861....5.1...9.1.3..85..2856931..9...546..5149872

- Finned Mutant X-wing: r6,c3  b4,r2 fr6c4 => r2c4 <> 6 
- Tackle : " 6 "
- N = 2
- Special char: Finned
- Shape: mutant
- Base r6,c3: (r6c24,r25c3) blue
- Cover b4,r2: ( r2c4 } red & change (r2c3,r5c3,r6c2) to Green 
- Vertices:  (r25c3,r6c2) Green , blue cells (r6c4)
- Finned: ( r6c4) change to purple
- Gaffed: ( r2c4 ) change to orange
- Eliminate: r2c4 <> 6

## Empty Rectangle
* Example Puzzle

5.1..3.....7..415..89.15.6..15..7346.2364157.67435....15643.78..925.......81....5

- Finned Franken X-Wing: 9 r7b6 c69 fr6c7 fr6c8 => r6c6<>9
- Tackle: "9"
- N = 2
- Special Char: Finned
- Shape: Franken
- Base b6,r7 (r6c789,r5c9) blue
- Cover c69 (r6c6) red & changes (r7c59,r56c9) to green
- Vertices: (r7c59,r56c9) green, blue cells (r6c78) 
- Finned:(r6c78) Change to purple 
- Gaffed: ( r6c6 ) change to orange
- Eliminate: r6c6 <> 9

## Sashimi Sword Fish
* Example Puzzle

913....4..752..3....6..3.755........6394.28.77......9416.5..7....7..6......7....1

- Sashimi Swordfish: 1 r358 c457 fr5c8 => r46c7<>1
- Tackle "1"
- N = 4
- Special Char: Sashimi
- Shape: Basic
- Base r358:  ( r3c458,r5c58,r8c45 ) Blue
- Cover c457: ( r354c4,r236c5,r46c7 ) red and change ( r3c457,r5c58,r8c45 ) to green  
- Finned: ( r5c8 ) change to purple
- Gaffed: ( r46c7 ) change to orange
- Eliminate: ( r46c7 ) <> 1

## Finned Sword Fish
* Example Puzzle

913....4..752..3....6..3.755........6394.28.77......9416.5..7....7..6......7....1

- Finned Swordfish: 1 r258 c458 fr2c6 => r3c45<>1
- Tackle "1"
- N = 4
- Special Char: Finned
- Shape: Basic
- Base r258:  ( r2c568,r5c58,r8c45 ) Blue
- Cover c458: ( r346c4,r346c5,r4c8 ) red and change ( r2c58,r5c58,r8c45 ) to green  
- Finned: ( r2c6 ) change to purple
- Gaffed: ( r3c45 ) change to orange
- Eliminate: ( r3c45 ) <> 1

## Sashimi Jellyfish 
* Example Puzzle

.42.53187758.4..3.3.1.....4.83.2.......8.4....2439.6782........41..3.8258354.279.

- Sashimi Jellyfish: 6 r1249 c1469 fr9c5 => r7c46,r8c46<>6
- Tackle "6"
- N = 4
- Special Char: Finned
- Shape: Basic
- Base r1249:  ( r1c14,r2c469,r4c146,r9c59 ) Blue
- Cover c1469: (r5c1,r278c4,r378c6,r8c9 ) red and change (r1c14,r2c469,r5c146,cr9c9  ) to green  
- Finned: ( r9c5 ) change to purple
- Gaffed: ( r7c46,r8c4 ) change to orange
- Eliminate: ( r7c46,r8c46 ) <> 6

## Finned Jellyfish 
* Example Puzzle

..18326.483.....7226....3.86.8.1.42...32.48..142.857.932...8.4..1.423.8.48.1962..

- Finned Jellyfish: 5 r1459 c1289 fr9c3 => r8c1<>5
- Tackle "5"
- N = 4
- Special Char: Finned
- Shape: Basic
- Base r1459:  ( r1c128,r4c29,r5c1289,r9c389 ) Blue
- Cover c1289: (r8c1,r3c8,r78c9 ) red and change (r1c128,r4c29,r5c1289,r9c89 ) to green  
- Finned: ( r9c3  ) change to purple
- Gaffed: ( r8c1 ) change to orange
- Eliminate: ( r8c1) <> 5

If comfortable netting & Gaffing these style of fish a player can move on to: [more exotic fish species](https://www.reddit.com/r/sudoku/wiki/Fish-Advanced-terminology)

