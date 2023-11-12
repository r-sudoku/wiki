*Intermediate solving begins when a player has a firm grasp of BLR, Naked & Hidden subsets* 

Please be familiar with all of the terminology and concepts covered in the following topics before preceding
 
[Entry Terminonogy](https://www.reddit.com/r/sudoku/wiki/edit/e-terminology/)

[Beginner Terminology](https://www.reddit.com/r/sudoku/wiki/B-terminology/)

- All logic concepts in basics propagate into higher constructs  

This chapter covers concepts hinted at in [basics:](https://www.reddit.com/r/sudoku/wiki/b-terminology/)

Sudoku logic falls into two categories seen as different approaches with the same outcome. 

# [Graph Theory:](https://en.wikipedia.org/wiki/Graph_theory) 
 - example Naked & Hidden single 
 - how? 81 cells are vertex on a graph and there is only 1 vertex left on in the graph for the digit 

# [Set Theory:](https://en.wikipedia.org/wiki/Set_theory)
- example: Naked & Hidden Subsets  
- how ?  a set of digits and a set of cells  for n digits in n cells is a completed set. 

*This next section will focus on Graphing Theory as it relates to the next level of solving once we have exhausted basics* 

# Truth:
 - a proposition that a candidate or cell is:  on, correct or used. 

# False: 
 - a proposition that a candidate or cell is off, incorrect or not used. 

# Logic Gate: 
 -A testing construct that something is True or False with a single outcome
- (X is true or X is false)
 
# Strong Link:  
- Two Truths may be asserted, in a sector but only 1 may be true at a time. 
- A combination of Two logic gates (A = not A) And (B = Not B) [discussed below](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_using_logic_gates_as_strong_links.)
- Usable Formations of Strong links: 
- Bi-location
- Bivalve
- There is more types of strong links covered in [competent vocabulary](https://www.reddit.com/r/sudoku/wiki/c-terminology/#wiki_grouped_strong_link) 


# Weak Link:
- A weak link is a Single logic gate that A is true or A is false: where A as false has no outcome thus no effect on the next link.
- A weak link can only directly affect something when True so that its is a Implication node. 
- Expansion of this concept covered in [competent volcabulary]https://www.reddit.com/r/sudoku/wiki/c-terminology/#wiki_weak-link_-_update)  

# Using Logic Gates as strong links. 
 - With a strong link we have two out comes A Or B is true in one sector using the puzzles construction Rules.  
 - We know that A is true or when A is false B must be true 
 - We know that B is true or when B is false A must be true 
 - This creates our first step in graphing nodes  (A is true or B is true) 
 - Expressed  as a single node of  ( A = B ),  where "=" indicates its a strong link construct.
- This is a combination of two logic gates ( A or not A) and (B or not B) with a single out put A or B is true. 

# How do we connect logic Gates to do something


# Weak inference:  
- An inference that the next part of a strong link logic gate is not true
- An inference i'm that the next immediate part of a Strong link  logic gate is false
- how do we infer something is "false" 
   - By using the laws of a Sudoku puzzle: a sector can only have 1  of each digit , all sectors must have at least 1 digit to satisfy the constraints, and each cell must have 1 digit.  
- if the first part of a Strong link logic gate is false then the second must be true
  - Not(A = B)  becomes (B = B) as we know NOT A means B
  - in constructs  we  use " - " to indicate the weak inference.
  - the cells before and after a " - " in chain notation means that these two cells can never both be true but both can be false. 

# Working Logic:  Putting it together 

- For each strong link we find we have two options
- For each of its options check that cells peers for the same candidates 
- If it has the same candidate check if its part of a strong link
- If it is we have our next usable strong link. 

* The peer cell we are checking as a friendly reminder automatically will indicate where the weak inference "-" is placed { other cell in the initial sector is assumed false} *

*chain logic is built assuming the first cell is false!, and all subsequent truths infer information until it cannot add any more strong links.  Then the first and last cell can be interpreted for truths as start or end must be true.* 

- ( items inside this bracket are strong links ) 

- Brackets are often skipped in solver output I have it here to draw attention to it

- (x) indicates the digit the strong links are currently using

*A typical chain:*  (x)(A or B) - (C = D)

Read left to right as A or D is true 

     x @ A is true 

        or 

     X @ B is true 

          B infers C is false thus D is  true for x 


The best feature of writing chains like this is they are bi-direction and can be 
Read right to left as D or A is true

    X @ D is true
 
      or 

    X @ C is true 

          C infers B is false thus A is true for x 

The conclusion: 
 X is in D or A cell any cell that is peer to A and D may be excluded for x. 

## Proof of chain concepts  
- all chains can be easily proven as valid:  try the eliminations as true. 
- The chain construct can have puzzle construction rule violations from the following.
   - A Cell with no candidates left
   - A strong link with no candidates that can be true 
   - A cell that must be 2 different candidates at the same time

#Symbols used in intermediate solving

    => implies
    <> not equal to
    =  Strong Link 
    -  Weak Inference

# Node: 
 - A Strong link 

# Network: 
- A sequence of nodes

# Chaining: 
 - constructs using logic gates to build a network of nodes to prove something 

* Below is a list of some of the chaining methods a solver may come across as you grasp how strong and weak links operate* 

## Discontinuous & Continuous Nice Loops: 
- The precursor of A.I.C.'s that start on a weak Link instead of a strong link where the network proves the starting cell can only be false.

 ### Simple Colouring &  X - cycle(s) 
 - Nice loops on single candidates. 
 
 ## Alternating Inference Chain {A.I.C}:
 - A collection of logic gates that starts on a strong link and alternates weak inferences before the next strong link. 
 - Allows TRUE or FALSE propositions to be applied to candidates to determine potential eliminations.
 - There is two types of chains: Continuous  &  Discontinuous 

  ### Continuous aka Loop(s):
 - A descriptor that indicates the end and starting cells share either cells or candidates so they are discreetly connected 
 - Type 1 classification in many solvers 

  ### Discontinuous:  
 - A descriptor that indicates the end and starting cells only share peers 
 - Type 2 classification in many solver 
 
  ## X - Chain 
  - A Single Candidate alternative Inference Chain  

  ## XY - chain: aka Y-chain 
    - An Alternating Inference chain using only Bivalves  

# Entry Level Chaining practice:  

## X - Wing: 
- A Formation of two Strong links with the same candidate 
- Constructed using either Rows or Cols
- A x-wings strong link each have two ways to construct a weak inference to the next strong link yielding four chains
- Is a continuous Alternate Inference chain in the x-Chain class as it is constructed with one candidate 
- for simplicity at this point all valid eliminations comes from the four chains applied at the same time. [ this chapter discuses how to do it easier](https://www.reddit.com/r/sudoku/wiki/create/p-terminology/)  

*Example Puzzle:* 

..47.5...29....15..5891....52.49861....5.1...9.1.3..85..2856931..9...546..51498..

(7) (r2c3 = r2c9) - (r4c9 = r4c3) => r5c3 <> 7 

(7) (r2c9 = r2c3) - (r4c3 = r4c9) => r359c9 <> 7

(7) (r4c3 = r4c9) - (r2c9 = r2c3) => r5c3 <> 7 

(7) (r4c9 = r4c3) - (r23 = r2c9)  => r359c9 <> 7 

![](%%xwing07%%)

## Skyscraper:
- A Formation of two Strong links with the same candidate 
- Constructed using either Rows or Cols
- A Skyscraper has two strong links each with only 1 option to be weakly linked yielding two chains
- Is a Discontinuous Alternate Inference chain in the X-Chain class as it is constructed with one candidate 
- all peer cells of start and end cell are potential eliminations. 

*Example puzzle:* 

..47.5...29....15..5891....52.49861....5.1...9.1.3..85..2856931..9...546..5149872

(6) (r5c3 = r2c3) - (r3c4 = r6c4) => r6c2,r5c5 <> 6 

(6) (r6c4 = r3c4) - (r2c3 = r5c3) => r6c2,r5c5 <> 6 

![](%%skyscraper06%%)
    
## 2 - String Kite:
- A Formation of two Strong links with the same candidate 
- Constructed using one Rows and one Col
- a 2 string kite has two strong links each with only 1 option to be a weak inference
yielding two chains
- Is a Discontinuous Alternate Inference chain in the X-Chain class as it is constructed with one candidate 
- all peer cells of start and end cell are potential eliminations. 

*Example puzzle:* 

..47.5...29....15..5891....52.49861....5.1...9.1.3..85..2856931..9...546..5149872

(6) (r2c3 = r5c3) - (r6c2 = r6c4) => r2c4 <> 6

(6) (r6c4 = r6c2) - (r5c3 = r2c3 ) => r2c4 <> 6

![](%%twostringkite06%%)

## Remote Pair: 
 - A collection of Bivalve strong links all with the same candidates 
 - An Alternating inference chain using only Bivalves that all contain the same two digits.
 - Start and end cells peers may be excluded for both candidates 
 - the simplest remote pair is a naked pair. 

*Example Puzzle:* 

16.3.825.83.256..152.91.3682567931849714856324836219753958.2.1661253.8..748169523

Remote Pair: (7=4)(r2c7) - (4=7)(r7c7) - (7=4)(r7c5) -(4=7)(r1c5)  => r1c9 <> 7

![](%%remotepairs47%%)

## XY - Wing  aka Y-wing
- First introduction to multi digit changes [discussed in full here]
- These are Discontinuous A.i.C 
- A collection of 3 Bivalves as strong link each using partitions of the same 3 digit combination set 
- The first and last bivalves selected share the same  starting and ending digit 
- Peers of first and end cell may be excluded for their common candidate 

*Example puzzle*

 31...2958629538471..81.9623..3.9781...18.359.89..1536.736981245142356789985724136

XY-Wing: (7=6)r5c2 - (6=4)r5c5 - (4=7)r3c5 => r3c2<>7

![](%%xywing467%%)

[Next Lesson: Competent Level Terminology](https://www.reddit.com/r/sudoku/wiki/C-terminology/)

