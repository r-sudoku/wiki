Competent solving begins when a player has a firm grasp of BLR, Naked & Hidden subsets, Entry level X-Chain, Remote pairs, XY - Wings.  

Please be familiar with all of the terminology and concepts covered in the following topics before preceding

* I strongly advise to use Dark Mode on browser for viewing this page
 

[Entry Terminonogy](https://www.reddit.com/r/sudoku/wiki/edit/e-terminology/)

[Beginner Terminology](https://www.reddit.com/r/sudoku/wiki/B-terminology/)

[Intermediate Terminology](https://www.reddit.com/r/sudoku/wiki/i-terminology/)

#Symbols used in intermediate solving

    => implies
    <> not equal to
    =  Strong Link 
    -  Weak Inference

*All logic concepts in basics & Intermediate propagate into higher constructs*

# Recap on last topic: 
- In the Previous topic we discussed using candidates as inferences between strong links, in this topic we will add to it bringing you into Competent chaining

*To understand this topic in full improvement for our existing vocabulary is needed*

#Value 
 - A candidate used in a chain that affects through inference the next set of strong links so that x position(s) are off.

#Location 
 - A Cell that is inferred to as 0n for one value and off in another strong link
 - Location changes are the next level of Chaining 
 - A bivalve is also a location change 

*To understand Location better and how to use it more effectively more constructs for the grid are needed.*  

# Mini Line:
 - A Grid has 27 sectors, each containing 9 cells 
 - These 9 cells are broken down into groups of 3 cells
 - Mini Lines area Mental Construct to in-vision while solving 
 - There are 4 types: 

## Mini Row by Box  
 - a group of three Cols on one Row in a Box  

Example: 

 Three groups [r1c123],[r2c456],[r3c789] for the mini Row by Box 
  
| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 | 1 | 1 | 1 |  |  |  |  |  |
r2 | 2 | 2 | 2 |  |  |  |  |  | 
r3 | 3 | 3 | 3 |  |  |  |  |  |  
r4 |  |  |  |  |  |  |  |  | 
r5 |  |  |  |  |  |  |  |  | 
r6 |  |  |  |  |  |  |  |  | 
r7 |  |  |  |  |  |  |  |  | 
r8 |  |  |  |  |  |  |  |  | 
r8 |  |  |  |  |  |  |  |  | 

## Mini Col by Box  
 - a group of three rows on one Col in a Box  

Example: 

  Three groups [r123C1], [r123c2], [r123c3] for the mini Col by Box 
  
| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 | 1 | 2 | 3 |  |  |  |  |  |
r2 | 1 | 2 | 3 |  |  |  |  |  | 
r3 | 1 | 2 | 3 |  |  |  |  |  |  
r4 |  |  |  |  |  |  |  |  | 
r5 |  |  |  |  |  |  |  |  | 
r6 |  |  |  |  |  |  |  |  | 
r7 |  |  |  |  |  |  |  |  | 
r8 |  |  |  |  |  |  |  |  | 
r8 |  |  |  |  |  |  |  |  | 

## Mini Row by Col
 - a group of three Cols on one Row in a Box  

Example: 

 Three groups [r1c123], [r1c456], [r1c789] for Mini Row by Col
  
| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 | 1 | 1 | 1 | 2 | 2 | 2 | 3 | 3 |3
r2 |  |  |  |  |  |  |  |  | 
r3 |  |  |  |  |  |  |  |  |  
r4 |  |  |  |  |  |  |  |  | 
r5 |  |  |  |  |  |  |  |  | 
r6 |  |  |  |  |  |  |  |  | 
r7 |  |  |  |  |  |  |  |  | 
r8 |  |  |  |  |  |  |  |  | 
r8 |  |  |  |  |  |  |  |  | 

## Mini Col by Row
 - a group of three Cols on one Row in a Box  

Example: 

 Three groups [R123C1], [456C1], [r789c1] for Mini Row by Col
  
| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 | 1 |  |  |  |  |  |  |  |
r2 | 1 |  |  |  |  |  |  |  | 
r3 | 1 |  |  |  |  |  |  |  |  
r4 | 2 |  |  |  |  |  |  |  | 
r5 | 2 |  |  |  |  |  |  |  | 
r6 | 2 |  |  |  |  |  |  |  | 
r7 | 3 |  |  |  |  |  |  |  | 
r8 | 3 |  |  |  |  |  |  |  | 
r8 | 3 |  |  |  |  |  |  |  |

# Using Mini - Lines
- A Mini line brings with it a very useful feature for chaining 
- it has 3 potentially Truths with in the 3 groups 
- when one of them is Off we are left with two! 
- Two Truths we can use to build another type of Strong link and expand our definitions : Grouped Strong link

## Grouped Strong Link 

Example: { Using Mini Row by Box }

 - R1 has [1 & 3] left as active
 - Using the same ideas found in [strong links](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_strong_link.3A) 
 - We know that R1 is true or R3 is true
 - Based on construction limitations if 1 is off 3 must be true
 - Based on construction limitations if 3 is off 1 must be true
 - We call these Grouped strong links as each mini line potentially contains 3 active cells
 -There is four ways to make Grouped strong links based on the 4 types of Mini lines
- Grouped links will have at least 3 active cells other wise they are basic strong links
- Grouped links have two types of transference,
  - Value, this one is always applicable 
  - Location can be used but care must be utilized
    - This type is only applicable on mini lines with one cell 

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 | 1 | 1 | 1 |  |  |  | 3 | 3 |3
r2 |  |  |  |  |  |  |  |  | 
r3 |  |  |  |  |  |  |  |  |  
r4 |  |  |  |  |  |  |  |  | 
r5 |  |  |  |  |  |  |  |  | 
r6 |  |  |  |  |  |  |  |  | 
r7 |  |  |  |  |  |  |  |  | 
r8 |  |  |  |  |  |  |  |  | 
r8 |  |  |  |  |  |  |  |  |

## Empty Rectangle Intersection {ERI} 
- This is a special case of Grouped Strong links
- ERI's can only be used as Value inferences  
- A Grouped strong link in a Box can also be true as a Row or Col
- An ERI is a check used to determine if all the cells in a box are exactly on 1 row and 1 col and that the overlap of the row * col isn't the only active cell. 
  
- Marking the centre cell of the intersecting row/col as a reminder of where to build links from as these are directional changes row to col or col to row.

-Important:  IF an ERi has * as an active cell they cannot be used to start chains 
 
- Method to Find an ERI 
  -A counting method: pick a candidate and 1 Row and 1 Col in a Box.

   *sum of (Row + Col) cells  - (the centre cell if active) = total number of cells in a box* 

- If the box has greater then 5 its invalid.
- If the total is less then 2 its invalid.  
- If the row or col has no cells its also invalid.
- This concept is a very old one Created by u/strmckr & lost all documentation on this and its practical usage during the enjoysudoku forum crash in 2007 very few people know about it asides a niche group of programmers that added it to there chain building methods.

# Strong link the 6 types exemplars: 
 - Remember the 4 mini-line versions above, these maybe remapped to those types

*Bivalve*

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 |  | 12 |  |  |  |  |  |  |

*Bi-location*

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 |  | 1 |  |  |  |  |  | 3 |

*Grouped & one cell*

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r2 | 1 | 1 | 1 |  |  |  | 3 |  | 

*One cell & Grouped*

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r3 |  | 1 |  |  |  |  | 3 | 3 | 3

*Grouped & Grouped*

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r7 | 1  | 1  | 1 |  |  |  | 3 | 3 | 3 

*ERI*

| |c1 | c2 | c3 | c4 | c5 | c6 | c7 |c8 |c9
:- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | -: 
r1 |   | 1  |   |    |  |   |    |   | 
r2 | 1 | 1* | 1 |   |  |  |   |  | 
r3 |   | 1  |   |    |  |   |   |   | 
r4 |   |   |   |    | 2 |   |    |   | 
r5 |   |   |   |  2 | * | 2 |   |  | 
r6 |   |   |   |    | 2 |   |   |   | 
r4 |   |   |   |    |  |   |    |   | 
r5 |   |   |   |   |  | |  3 |  | * 
r6 |   |   |   |    |  |   |  * |   | 3

*Legend:* 

 - (1) Max ERI   <- cannot be used to start chains 
 - (2) ERI * cell is Missing  <- can be used to start chains 
 - (3) Minimal ERI  <- can be used to start chains 

 - " * " is the reminder mark discussed in ERI description.*
 - note: There is others between Max and Minimal not depicted as long as they hold  the requirements they are valid.  

#[Weak-link](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_weak_link.3A) - update
- Just like strong links a weak link can also include Grouped candidates from one mini sector. 
- A weak link is A Single logic gate that Group A is true or Group A is false: where A as false has no outcome thus no effect on the next link.
- Since A Weak link can only affect when True it is an Implication node.

# Working Logic: Putting it together - updated
 - For each Grouped strong link, strong links and ERI we have two options A or B is true For Value
 - the same concepts in [working links](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_working_logic.3A__putting_it_together) is used for value please read for clarity. 
 
 - For Grouped & strong links with 1 cell in A or B the second inference option is  introduced in this topic: Location 
 - If we are using Location we search Candidates in the selected cell for another strong link or grouped link  with 1 cell using this same selected cell. 
- If it has the required conditions we change candidates and select this as the next strong link 
- The cell we are checking as a friendly reminder automatically will indicate where the weak link "-" is placed when building a chain.

*Chain logic is built assuming the first cell is false!, and all subsequent truths infer information until it cannot add any more strong links. Then the first and last cell can be interpreted for truths as start or end must be true.*

Example: {value & location change}

(1=2)r1c1 - (2)(r2c3 = r4c3) - (1)(r4c3 = r4c5) 

Read left to right as r1c1 or r4c3 is true for candidate 1

    1 @ r1c1 is true 
        or 
    2 @ r1c1 is true 

       2 @ r1c1 infers  2 @ r2c3 is false and 2@ r4c3 is true
                  2@ r4c3 infers  (1) @ r4c3  is false  and 1 @ r4c5 is true 

The best feature of writing chains like this is they are bi-direction and can be Read right to left as  r4c5 or r1c1 is true for candidate 1

    1 @ r4c5 is true 
        or 
    1 @ r4c3 is true 

       1 @ r4c3  infers  2 @ r4c3 is false and 2 @ r2c3 is true
                  2@ r2c3  infers  (2) @ r1c1  is false and 1 @ r1c1 is true

*The conclusion:*
the chain proves 1 is in (R1c1 or R4c5) then all peers of (R1c1 and R4c5)  may be excluded for 1     => r1c5 <> 1

* Writing it out*

(1=2)r1c1 - (2)(r2c3 = r4c3) - (1)(r4c3 = r4c5) => r1c5 <> 1

## Proof of Chain concepts  
- all chains can be easily proven as valid:  try the eliminations as true. 
- (1=2)r1c1 - (2)(r2c3 = r4c3) - (1)(r4c3 = r4c5) => r1c5 <> 1
- What happens if r1c5 is a 1. 
   - r1c1 & r4c5 cannot be 1 
   - Follow the inference and conclude r4c3 must be both 2 and 1  
 
- The chain construct can have puzzle construction rule violations from the following when checking for validity.
   - A Cell with no candidates left
   - A strong link with no candidates that can be true 
   - A cell that must be 2 different candidates at the same time
   - A sector will require to place a candidate twice for 1 sector which is impossible on a weak inference:
      - Any weak inference cannot be both true at same time.
 they both can only be false or one of the other is true. 


# Practice for single Value Chaining:  ERi's  
## Empty Rectangle
- Single Value X-cycle that uses ERI's 
- Structured as ( ERi - Value)
- Peers of First and Last cell(s) may be excluded for Value

*Example:*

5.1..3.....7..415..89.15.6..15..7346.2364157.67435....15643.78..925.......81....5

Empty Rectangle: (9) (r6c789 = r56c9) - (r7c9 = r7c6) => r6c6 <> 9 

![](%%emptyrectangle09%%)

# Practice competent chaining:     Discontinuous A.i.C 
 - The named three strong link and two weak inference A.I.C  "wings" 
 - Don't worry so much about the name
 - They have names because  all chains combinations of Value and Location have been explored for their class and structures of:  Three strong links with 2 weak inferences
- Names and formal constructs will be Discussed in its own page. 
- These are good to know as the "pattern or shapes" they form are easy to spot with practice
 
## XY - Wing  aka Y - Wing
- Structured as (Bivalve - Bivalve - Bivalve) 
- The first and last bivalves selected share the same  starting and ending Candidate
- Peers of first and Last cell may be excluded for their common candidate 

*Example puzzle*

 31...2958629538471..81.9623..3.9781...18.359.89..1536.736981245142356789985724136

  XY - Wing: (4=6)r5c5 - (6=7)r5c2 - (7=4)r6c3 => r5c1,r6c4<>4

![](%%xychain467%%)

## W - Wing 
- Structured as (Bivalve  - Value - bivalve)
- First and last cell share the same Value 
- Peers of first and Last cell may be excluded for the value 

*Example:*

.2...7..6.35641..7.6782...1......7....37.....679412..831.974..5.98.56.7375..839..

W - Wing: (4=2)r8c1 - (2)(r7c3 = r7c78) - (2=4)r9c9 => r9c3,r8c7 <> 4 

![](%%wwingchain24%%)

## M - Wing
- Structured as ( bivalve - Value  - Location)
- First and last share the same Value 
- Peers of first and Last cell may be excluded for the value

*Example:*

...67..242..4....1..4512..874.3..269..27..485..82.43178579361424..127856.2.845793

M - Wing: (1=8)r4c6 - (8)(r1c6 = r1c2) - (1)(r1c2 = r5c2) => r4c3,r5c6 <> 1

![](%%mwingchain18%%)

## {split} S - Wing  
- Structured as ( Value - bivalve - Value ) 
- First and last are peers  
- First and last do not share Values
- Value of first cell cannot appear in the last cell
- Value of last Cell cannot appear in first cell.

*Example:* 
 
 ..8.4....2..9..45...9..5..7824519...976382541...47698239265.....85.23.......9.235

S-wing: (4)(r9c6 = r7c6) - (4=8)r7c9 - (8)(r2c9 = r2c6) => r9c6 <> 8  

![](%%swing48%%)

## {Local} L - Wing {type: 1 } 
  - structured as {value - value - value}
  - uses 1 value 
  - first and last are peers 
  - first and last may overlap 

* Example:*

000382000030000080708000523340096050900050006000103000020608095006000400503070061

L - wing {type: 1}:(R78c1 = r1c1) - (r1c8 = r5c8) - (r4c7 = r4c3) => r7c3 <> 1

![](%%l1wing01%%)

## {Local} L - Wing {type: 2 } 
- Structured as ( Value - Value - location)
- Uses two values
- First and last are peers  
- First and last do not share Values
- Value of first cell cannot appear in the last cell
- Value of last Cell cannot appear in first cell. 

*Example:*

3.2...4.565.....914...57623..32.41...21.8..4.7465192381.46....2.3.....64.65...317

L- Wing (type 2):(7)(r8c4 = r5c4) - (3)(r5c4 = r5c6) - (3)(r7c6 = r7c5) => r7c5 <>7

![](%%l2wing37%%)

## {Local} L - Wing {type: 3 } 
- Structured as ( Value - Location - location)
- Uses Three values 
- First and last are peers  
- First and last do not share Values
- Value of first cell cannot appear in the last cell
- Value of last Cell cannot appear in first cell.
 
*Example:*

3.2...4.565.....914...57623..32.41...21.8..4.7465192381.46....2.3.....64.65...317

L- Wing (type 3): (7=6)r4c5 - (6=3)r5c6 - (3)(r7c6 = r7c5) => r7c5 <> 7

![](%%l3wing367%%)

## {Hybrid} H - Wing  {type 1} 
- Exact Same as Local Wing type 3 
- Structured as ( Value - Location - Location)
- Uses Three Values
- First and last are peers  
- First and last do not share Values
- Value of first cell cannot appear in the last cell
- Value of last Cell cannot appear in first cell. 

*Example Puzzle:*

.5....964467915283928364175.42.........4...27.7...63417.6.534.2...6..7..21.7.....

H - wing {type 1}: (5=9)r4c8 - (9=1)r7c8 - (1)(r7c4 = r4c4) => r4c5 <> 5

![](%%hwing159%%)

## {Hybrid} H - Wing  {type 2}
- Structured as ( Bivalve - Value - location)
- Uses Three Values
- First and last are peers  
- First and last do not share Values
- Value of first cell cannot appear in the last cell
- Value of last Cell cannot appear in first cell. 

*Example Puzzle:*

.5....964467915283928364175.42.........4...27.7...63417.6.534.2...6..7..21.7.....

H - wing {type 2}: (8=2)r1c4 - (2)(r1c6 = r8c6) - (1)(r8c6 = r7c4) => r7c4 <> 8

![](%%h2wing138%%)

## {Hybrid} H - Wing  {type 3}
- Structured as ( Bivalve - Bivalve - Value)
- Uses Three Values
- First and last are peers  
- First and last do not share Values
- Value of first cell cannot appear in the last cell
- Value of last Cell cannot appear in first cell.

[next lesson: Proficient Vocabulary](https://www.reddit.com/r/sudoku/wiki/P-terminology/)

