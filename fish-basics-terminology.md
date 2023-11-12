Welcome to the pond and a wonderful collection of Fish species and their similarities and subtle differences. 

When finished reading this adventures guide hopefully you  will be equipped with enough tackle and skilled lines thrown to haul in your first fish.

# [The Ultimate Fishing Guide](http://forum.enjoysudoku.com/the-ultimate-fish-guide-t4993.html)
 - An all encumbering topic dissecting and explaining everything fish related
 - This guide will break it down into subtopics for easier digestion. 

#How did fishing come to exist? 
  - To answer this we first have to understand the nature of a Sudoku puzzle and its Templates
 
  ## Template 
   - Templates are a collection of every possible arrangement of all 9 cells for 1 digit
    - There is 46656 Different templates for each digit.
    - A Sudoku puzzle has exactly 9 templates, one for each digit when it solves to 1 solution. 

     ### What can Templates do?
- Based on the opening Grid construct the total number of templates is reduced by a large volume, still this is a very large number  impractical for a human to manually compare tiles one to figure out which 1 is left for the digit
       #### Computer aids:
- With code we can compare all remaining Templates for a single digit pretty quickly.  
- When we compile a full list of all templates and look for similarities 
- similarity cell(s)  missing from all templates:
        ##### Nisho - single digit template omission 
-  Every template is a a potential solutions 
- Comparing all templates for cells used to active cells for the same digit 
- The missing cell(s) are not part of any solution and can be removed from the PM's

        ###### Fish - Explaining Template omissions. 
- Template form of Constraint satisfaction using 1 digit, in-order for a deletion to be made some kind of constraint was satisfied some where.
- Fishing was created as a method to mathematically Prove the set and container caused the eliminations. 

        ###### [Set Theory](https://en.wikipedia.org/wiki/Graph_theory)
- Why is this set theory? 
- Fish use sets and containers to prove reductions by balancing sets fitting exactly into a container. 
 
# Fish Constructs:
 * A Fish is constructed using Sectors,Row,Col,Box and a single digit
 * A Fish has two components to form the math equations: Base & Cover
  - This topic will focus on Row,Col,Box  (Non Mixed types only)   

## Base Sector 
* Any Row or Col or Box is selected for a digit
* Basic Fish uses copies of the initial Sector type.    
 
## Cover sector 
* As a basic fish its cover sectors are the opposite of the base, if you selected row covers it will use Cols or Box only (do not mix cover sets types)
* Every cover set used must have at least 1 cell from the base sectors picked.    

### Picking Base and Cover sets: 
* in basic fish we look for N base sectors and N Cover sectors
* this creates the balance and sets up the following math 

 # Fish Math 
   * "Base" and "Cover" 

   * for any specific digit,
   * a "fish" of order N
   * is defined by a "base" of N units and a "cover" of N units,

   - Where the observation is 
   * A. each unit of the "base" can only have the digit somewhere in the "cover", and
   * B. the digit cannot occur in the overlap of units of the "base" 

    - thus we know that the "base" will provide the digit N times in the "cover",
    and the conclusion is 
    — exclude the digit in the "cover" outside the "base"

 *[extensions from NxN +K fish] 
   - beyond the "fish" exclusion,
   - if there's overlap in the "cover"
   - we have an extra type of exclusion —
   - exclude the digit in the overlap of units of the "cover";   
   - by considering order N\N,
   - where the "cover" is increased by K units ( N < K )

## How does the math actually work? 
  * Operationally every base and cover set form an intersection
  * The cells in the intersection are called a : Vertices 

### Vertices 
  * each vertices provides 1 cell{s} per sector, and only 1 vertices can be true sector at any one time, so that we can have  N vertices for N sectors.  a 1 to 1  satisfied container construct.

# N Size Fish by Name 

  * Fish are named after the number of N sectors the base and cover use.
  * N = 1, CyclopsFish   (AKA Box line Reduction)
  * N = 2, X - Wing
  * N = 3, Swordfish
  * N = 4, Jellyfish
  * N = 5, Starfish ( aka Squirmbag )
  * N = 6, Whale 
  * N = 7, Leviathan

* This guide will only give demos for size 1 - 4 at this stage of learning as larger construct do function under the same outlines here in, but becomes increasingly difficult to navigate as the sectors needed to keep track of double with size.

## Shape of Fish:
* 1. Basic: N row sectors x N column sectors or vv. 
* 2. Mutant: N sectors x N sectors (That is not Basic ) 

#### Naming of Fish:
* listed in order
- 1. Special Qualities {covered in later topics} 
- 2. Shape : if non basic, and N > 1 
- 3. Name for N size. 

# Colouring for Fishing 
* The best approach and fail safe method for Fishing is to uses highly visible Tackle.  
* Pick 3 colours { for reference i will use }
  - Base: = Blue
  - Cover:= Red 
  - Vertices = Green

## Using Colours
  * Pick a Digit {your tackle} 
  * Pick a Size  { N  the number of Lines to cast} 
  * N Base sectors - Colour every cell Blue, that has the digit your after
  * N Cover sectors - Colour every Cell Red, that has the digit your after 
      - If the cell is coloured Blue change it to Green 
  * Check your Net: { Vertices }

   - if there is any blue cells left you have no fish. 
      - if the fish doesn't work add another N if you can. 

   - if all blue cells are Green you have N vertices for N sectors thus your net is full and ready to Haul in 

    ## Colour Eliminations
      - When the net is full:
         - all Red cells are exclusions for the digit selected. 

### Proof 
  - Try placing one of the eliminations, doing so one of sectors will have no candidates left to place: a construction rule violation.   
   
# Working Logic: Fishing Expedition 
 
## CyclopsFish aka [box line reduction](https://www.reddit.com/r/sudoku/wiki/b-terminology/#wiki_box_-_line_reduction_aka_blr) 

- size 1 fish, uses 1 base and 1 cover 

* Example Puzzle: 

9..74......269.7.......2.9619..265745......8272.4...1365.2..1.9..196.8.5..9513.67

 - Tackle : " 3 "
 - N = 1
 - class: Mutant  
 - Base B2:  ( r3c45 ) blue
 - Cover R3:  ( r3c1237 ) red  & changes ( r3c45 ) to Green 
 - Vertices: ( r3c45 ) is green, no blue cells we have a fish
 - Eliminate: ( R3c1237 ) <> 3 

* Example Puzzle: 

.......46.936.415..467.1329951238.6.437169582.6.547931.894.56...75..6.9.6.4.....5

 - Tackle : " 3 "
 - N = 1
 - Class: Mutant  
 - Base r9:  ( r9c46 ) blue
 - Cover B8:  ( r8c4 ) red  & changes  ( r9c46 ) to Green 
 - Vertices:  ( r9c46 ) is green, no blue cells we have a fish
 - Eliminate: ( r8c4 ) <> 3

## [X - Wing](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_x_-_wing.3A) 
 - size 2 fish uses 2 base & 2 covers

* Example Puzzle

..47.5...29....15..5891....52.49861....5.1...9.1.3..85..2856931..9...546..51498..

 - Tackle : " 7 "
 - N = 2 
 - Class: basic   
 - Base:  r24 (r239,r4c39) blue
 - Cover: C39 (r3c9,r5c39,r9c9 ) red & changes (r239,r4c39 ) to Green 
 - Vertices:  (r239,r4c39 ) is green, no blue cells we have a fish
 - Eliminate: (r3c9,r5c39,r9c9 ) <> 7

## SwordFish
 - size 3 fish uses 3 base & 3 covers
* Example Puzzle

7.9.684.....91..671.6..7.9.61.79..48.9..8..2.3...41....7.1..6848...56....6187...2

 - Tackle : " 2 "
 - N = 3  
 - Class: basic  
 - Base:  c157 (27c1,r37c5,r25c7) blue
 - Cover: r237 (r2c235,r3c24,r7c36) red & changes (r2c17,r3c57,r25c7) to Green 
 - Vertices:  (r2c17,r3c57,r25c7) is green, no blue cells we have a fish
 - Eliminate: (r2c235,r3c24,r7c36 ) <> 2

## JellyFish
- size 4 fish uses 4 base & 4 covers
* Example Puzzle

7.9.684.....91..671.6..7.9.61.79..48.9..8..2.3...41....7.1..6848...56....6187...2

- Tackle : " 2 "
- N = 4
- Class: basic  
- Base: r1468 ( r1c24,r4c36,r4c234,r8c234 ) blue
- Cover c2346 ( r23c2,r27c3,r3c4,r27,c6 ) red & changes ( r1c24,r4c36,r4c234,r8c234 ) to Green 
- Vertices:  ( r1c24,r4c36,r4c234,r8c234 ) is green, no blue cells we have a fish
- Eliminate: (r23c2,r27c3,r3c4,r27,c6) <> 2

# Tip:
* When searching for Basic fish beyond Size 1, all base sectors may only Have a Max of N candidates. 

 If comfortable netting these style of fish  a player can move on to: 
 [more exotic fish specices](https://www.reddit.com/r/sudoku/wiki/Fish-Intermediate-terminology)

