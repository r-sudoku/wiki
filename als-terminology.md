In [Locked sets](https://www.reddit.com/r/sudoku/wiki/L-terminology/) we introduced the concept of N cells with N candidates

This topic and all subsections under this category are functioning within the other side of Sudoku logic mentioned earlier

#[Set Theory](https://en.wikipedia.org/wiki/Graph_theory) 
 - why is this set theory? 

   -  N Cells is a set, N candidates is a container full-filling the container  satisfies the set thus restrictions may be made to those that see the container.

   -  N Candidates is a set, N Cells is a container full-filling the container satisfies the set thus restrictions may be made to those that see the container.


# Intro 

 *What happens if A locked set has more digits then cells?*
- We have a case that it almost has N cells and N candidates 
- The "almost" part is key to the name that this topic covers.  

This topic will only focus on the Naked type of Locked set extended into Almost locked sets types

#Almost locked set - ALS for short
 - An Almost locked set has one extra candidate in N cells
 - An Als is constructed in a single sector common to all cells. 
 - Mathematically written as:  N cells with N+1 candidates

## Can an Als have more then one extra digit 
 - Yes, this will be covered [here *to be added]
 - Refereed to as:  Degrees of Freedom

 ### Degrees of Freedom 
 - They can be N size with N+x digits
   - x has a limit just like a puzzle, there is only 9 candidates
   - if we have N cells x at most can be (9 - n) 
       - eg. 1 cell can have at most 8 extra candidates
       - 1 cell with 1+8 => 1 cell with 9 candidates
 - written out for each (X-1) we add another "a" in-front of the almost  
 -  AAAAAAA almost locked set  {using the 1 cell with 8 extra candidates)
 - or short hand A^8 lmost locked set {not a common practice as few use size beyond the AAls}  
 
# Smallest ALS 
  - 1 cell with 2 digit { N cells with N+1 candidates }
 - is a bivalve as mentioned [here](https://www.reddit.com/r/sudoku/wiki/b-terminology/#wiki_bivalve_or_bi-value.3A_.7B_terms_are_used_interchangeably_.7D)

# Using ALS
- How do we use ALS since it has extra candidate(s)
 -  We need a way to have it contain N Cells for N digits so that we can use the set and container satisfaction of set theory.
 - The answer to this question is by Sharing X candidate(s) between different ALS.  

## Sharing candidates: 
 - How do Als share candidates 
 - First we need at least 2 different ALS  labelled for demo as A,B
  - These ALS need to have a common candidate 

     - A) One candidate within A ALS that can be isolated to one sector
        - The cells carrying the candidate have a row,box,col common to them all

     - B) Candidate within an ALS that can be isolated to one sector
        - The cells carrying the candidate have a row,box,col common to them all

     * When the Candidate picked in A & B are the Same and the sector it resides in is the same for both sets* 

- This forms the sharing aspect of two als we call this the Restricted Common Candidate, as one candidate is isolated to one common sector. 

### Restricted Common Candidate (RCC)
   - A candidate in two ALS that can only be placed in A or B and not both as it is restricted to 1 sector.
   - This is bases of all ALS techniques 
   - RCC is Labelled { X }   
       - in all solving software and descriptions

#### What does the RCC do? 
  - Acts as another type of [Strong link](https://www.reddit.com/r/sudoku/wiki/c-terminology/#wiki_strong_link_the_6_types_exemplars.3A)  as it forms (A or B) logic as x is restricted to A or B and cannot be in both

   - Each RCC added we change the mathematics of 1 set by 1 candidate
   *How?*
  
   - Als A has N cells with N+1 candidate but we know x is in B then A is reduced by 1 Digit and has N cells with N candidate making it a Locked set

 *OR* 

   - Als B has N cells with N+1 candidate but we suppose x is in A then B is reduced by 1 Digit and has N cells with N Digits  making it a Locked set

##### Can we have more then one RCC ?
   - yes for each Als we use it can bring with it 1 RCC
   - Called The N ALS N RCC rule, discussed in detail [here  - add link later] 

   *why is it limited to 1 per RCC?* 
        - since we have two RCC both of the following cases apply at the same time:   

    - Als A has N cells with N+1 candidate but we know x is in B then A is reduced by 1 Digit and has N cells with N candidate making it a Locked set

   *And* 

   - Als B has N cells with N+1 candidate but we suppose x is in A then B is reduced by 1 candidate and has N cells with N candidate making it a Locked set

- Since both sets are now Locked sets, adding any more RCC would make 1 of them have more cells then available Candidates a construction rule violation: 
   (N cells  with  (N-1) candidates)

###### Can sets share cells?   
  - yes, als sets can Overlap and share cell as long as two limitations are strictly followed 

  - ALs must contain new cells so they cannot be full copies of each other

  - RCC cannot be used in any Shared cells between sets

    - if they share a cell any candidate in that cell is an invalid RCC
      - why ALS logic focused on A or b logic, overlaps allows A & B as possible so we cannot use the logic

# Working Logic: Putting it together
- Identify two ALS
- Find a RCC between the sets

 *now that we have a RCC and know that A or B can be a locked set what does it mean?* 

  - Since we know that A or B can be a locked set the Non RCC play's the next roll

*what is a non RCC?*

## Non Restricted Common Candidate {nRCC}
 - All Als used share a second Candidate
 - This candidate cannot be the RCC
 - Labelled Z

*What does Z candidates do*

 - When we have 1 RCC in a set
 - We know that A or B cells can be a locked set,
 - What we cannot discern is where those candidates are going to be 
 - If A and B have a Z candidate we gain some usable knowledge 
 - With Z being in both sets, and either set being locked we know that z will be somewhere in A or B 
 - Given this information we arrive out our first type and Named ALS function
 - All cells of A and B containing Z could have a Z 
 - Any  peer cell of All Z's of A and B  if solved as Z reduced A and B to less digits then Containers so they can be excluded else the puzzle has a construction rule violation. 
 - This is called the ALs - XZ exclusion rule 

 ### Als - XZ:   Rule 
 - Als A) N cells with N+1 candidate
 - Als B) N cells with N+1 Candidate 
 -  X) at least 1 RCC 
 -  Z) at least 1 non RCC 
 -  =>  eliminations all Peer cells for Z of Als A and ALS B

 #### Als - XZ: Double Link  Rule 
 - Application of the N ALS N RCC rule for 2 als's
 - Als A) N cells with N+1 candidate
 - Als B) N cells with N+1 Candidate 
 -  X) 2 RCC 
 -  Z) both X's and any Non RCC 
 -  =>  Eliminations all Peer cells for Z of ALS A and ALS B

*Additionally:*  
   
Als A non RCC are Restricted to ALS A:

- All peers of als A non RCC cells are eliminated

Als B all non RCC are Restricted to ALS B:

- All peers of Als B non RCC candidates are eliminated

# Symbols used in ALS &  How to read an ALS 
   - Als A) (14) r4c6, B) (14) r4c3, x: 1,2 , z: 1,2   => r4c45<>1, r4c45<>4
    - ALS tells us the class we are using
    - A & B...etc are letters representing the individual als 
    - ( ) or { } Shows the Candidates the set uses
   -  Cells its using listed  before or after the  ( ) 
   - X: RCC
   - Z: Elimination Candidates 
   - =>  implication

#Checks in reading or writing an ALS
  - The number of A's before the LS tell us the size {N}
  - We can verify that each als is correct size by counting the cells 
    - Making sure the  N cells with N+1 candidates is correctly build.     

#Practice Examples: 
.7....254345927618862...73929....863.56.3..27738..2.45.17...592.832.547152....386

##Naked Pair:
- The smallest possible ALS-xz 
- Is the smallest possible ALS-xz Double linked rule  

Als a) (14) r4c6

Als B) (14) r4c3 
 
x: 1,2 

z: 1,2 

=> r4c45<>1, r4c45<>4

 
### Does this mean other subsets are also ALS - xz Rules ? 
  - Yes it does 
  - Subsets can be  ALS-xz constructs 
  - When each cell(s) of the subset can be viewed as N cells with N+1 Candidates 

  #### Can naked subsets as an als-xz do more? 
    - Yes & No
    - Specifically it does something the Subsets can do but is missed in every single solver. 
    - ALs-Xz double linked considers the position of candidates in the set 
    - Where Subsets only care about the set matching the container and applying its reductions to the sector its found in for the set it used.

eg puzzle 
......4......63..1.8.9...576..7...8949.....3525...9..484...1.7.9..43......3......

Naked Quadruple: (1,2,6,9) in r1268c8 => r9c8<>1, r9c8<>2, r9c8<>6, r9c8<>9

*The same move as an als:* 

Almost Locked Set XZ-Rule: A=r6c8 {16}, B=r128c8 {1269}, X:1,6 Z:1,6 => r9c8<>6, r9c8<>1, r9c8<>2, r2c7,r9c8<>9

- These missed eliminations are left out because its easier and faster to execute logic in a easy -> harder  fixed order
- Then trying to program all of potential eliminations of a move and let smaller logic clean it up where possible.
 - Subsets should be applying eliminations for each candidate individually, most coders use the full set for eliminations. 
- I.E the extra r2c7 <> 9 would be found immediately after the Naked quadruple as a BLR
- Thus these can be intentionally missed
- But as a player, these should be included.

##### two ALs's using two sectors 
   - Constructing an als uses one sector 
   - They can use the same sector as in the examples of the Naked Pair

   * What happens if the two ALS's use two different sectors? 
       - We exampled a naked quad from 1 sector using two als
      - Can a subset be bent over 2 sectors? 
       - Yes the idea of Bending subsets created the next set of 
Named techniques: Bent Almost Restricted Naked subset. {barns for short} 
  
###### Open the B.a.r.n(s) Door
  - Barns is a overt topic that I u/strmckr created and do not recommend independently studying as all of it is relevant to als-xz 
- Barns calculate size based on total digits used and total cell counted once
  - In-which N cells and N digits are formed between two ALS-xz: {Barn size is N}
    - which means we count the cells and digits if they are 1:1 we have a Barn and could use
      - The "xxx - Wing" Name or "Barn(size)" and follow it with the normal als jargon.           

# Named ALS-wings 
 - Includes the barn size for reference
 - Every wing past size 4 is rarely used few bother to convert it to a name
 - XY-Wing {size 3 barn} 
 - XYZ-Wing  {size 3 barn} 
 - WXYZ-Wing  {size 4 barn}  also XY - Rings 
 - VWXYZ-Wing  {size 5 barn} 
 - UVWXYZ-Wing  {size 6 barn}
 - TUVWXYZ-Wing  {size 7 barn}
 - STUVWXYZ-Wing  {size 8 barn}
 - RSTUVWXYZ-Wing  {size 9 barn} 
  
 ## Barns(3,4) are the stepping stone into the world of ALS-XZ 
 - These hone the skills needed to find larger sets.

### Practical Applications

#### XY - Wing

*Example Puzzle:*

 31...2958629538471..81.9623..3.9781...18.359.89..1536.736981245142356789985724136

XY - Wing: A=r5c25 {467}, B=r6c3 {47}, X=7, Z=4 => r5c1,r6c4<>4

#### XYZ - Wing 

*Example Puzzle:*
957834621412.....7863172459146....75378516942295..71..5347912..681...794729..8513

XYZ - Wing: A=r4c46 {239}, B=r8c4 {23}, X=2, Z=3 => r6c4<>3

#### WXYZ - Wing

*Example Puzzle:*

31...2958629538471..81.9623..3.9781...18.359.89..1536.736981245142356789985724136

WXYZ Wing: A=r5c125 {2467}, B=r5c1,r6c3 {247}, X=7, Z=2 => r4c1,r5c9<>2

*Example Puzzle: Double linked rule*

..1.5...883.146.57.5798..4.5......8...6..5.....461.7.5..8..15791.35..862.95.6.314

WXYZ - Wing: A=r3c1 {26}, B=r79c1,r8c2 {2467}, X=2,6, Z:2,6 => r1c1<>6, r156c1<>2, r7c2<>4

#### XY - Ring 
Example: 

..761.2..263475.........67.3....1789.....7...75.8.....685....271327.64..479.2....

XY - Ring: A=r28c8 {159}, B=r28c9 {158}, X=1,5 z:1,5 => r8c5,r9c789<>5, r2c7<>1, r9c9<>8  

[next lesson: Almost Locked Sets - Intermediate Methodology ](https://www.reddit.com/r/sudoku/wiki/I-ALS-terminology/)

