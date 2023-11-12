In [Locked sets](https://www.reddit.com/r/sudoku/wiki/L-terminology/) we introduced the concept of N cells with N candidates

This topic and all subsections under this category are functioning within the other side of Sudoku logic mentioned earlier

#[Set Theory](https://en.wikipedia.org/wiki/Graph_theory) 
 - why is this set theory? 

   -  N Digits is a set, N candidates is a container full-filling the container  satisfies the set thus restrictions may be made to those that see the container.

   -  N Candidates is a set, N Cells is a container full-filling the container satisfies the set thus restrictions may be made to those that see the container.


# Intro 

 *What happens if A hidden set has more cells then candidates?*
- We have a case that it almost has N Candidates and N Cells 
- The "almost" part is key to the name that this topic covers.  

This topic will only focus on the Hidden type of Locked set extended into Almost Hidden sets types

* Forewarning: this topic covers the inversion of a Almost locked set, and since it flipped we are no longer removing candidates at x location. Instead these remove cells from candidate lists. 

* AHS naturally have an easier ALS technique as they are directly related to each other. 

#Almost Hidden set - AHS for short
 - An Almost Hidden set has one extra Cell in N Candidates
 - An Ahs is constructed in a single sector common to all cells. 
 - Mathematically written as:  N Candidates with N+1 Cells

## Can an Ahs have more then one extra digit 
 - Yes, this will be covered [here *to be added]
 - Refereed to as:  Degrees of Freedom

 ### Degrees of Freedom 
 - They can be N size with N+x Cells
   - x has a limit just like a puzzle, there is only 9 Cells
   - if we have N Digits x at most can be (9 - n) 
       - eg. 1 Digit can have at most 8 extra cells
       - 1 Candidate with 1+8 => 1 cell with 9 Cells
 - written out for each (X-1) we add another "a" in-front of the almost  
 -  AAAAAAA almost Hidden set  {using the 1 cell with 8 extra Cell)
 - or short hand A^8 lmost Hidden set {not a common practice as few use size beyond the Ahs}  
 
# Smallest AHS 
  - 1 cell with 2 digit { N candidates with N+1 cells }
 - is a bi-local as mentioned [here]

# Using AHS
- How do we use AHS since it has extra candidate(s)
 -  We need a way to have it contain N candidates for N cells so that we can use the set and container satisfaction of set theory.
 - The answer to this question is by Sharing X cells(s) between different AHS.  

## Sharing Cells: 
 - How do AHs share cells
 - First we need at least 2 different AHS  labelled for demo as A,B
  - These AHS need to have a common cell

     - A) One Cell within A AhS that can be isolated to one sector
        - The candidate carrying the cell have a row,box,col common to them all

     - B) Cell within an AHS that can be isolated to one sector
        - The candidate carrying the cell have a row,box,col common to them all

     * When the cell picked in A & B are the Same and the sector it resides in is the same for both sets* 

- This forms the sharing aspect of two aHs we call this the Restricted Common Cell, as one Cell is isolated to one common sector. 

### Restricted Common Cell (RCC)
   - A Cell in two AhS that can only be placed in A or B and not both as it is restricted to 1 sector.
   - This is bases of all AhS techniques 
   - RCC is Labelled { X }   
       - in all solving software and descriptions

#### What does the RCC do? 
  - Acts as another type of [Strong link](https://www.reddit.com/r/sudoku/wiki/c-terminology/#wiki_strong_link_the_6_types_exemplars.3A)  as it forms (A or B) logic as x is restricted to A or B and cannot be in both

   - Each RCC added we change the mathematics of 1 set by 1 candidate
   *How?*
  
   - Ahs A has N candidates with N+1 cells but we know x is in B then A is reduced by 1 cell and has N candidates with N cells making it a hidden set

 *OR* 

   - Ahs B has N candidates with N+1 cells but we suppose x is in A then B is reduced by 1 cell and has N candidates with N cells  making it a hidden set

##### Can we have more then one RCC ?
   - yes for each Ahs we use it can bring with it 1 RCC
   - Called The N AhS N RCC rule, discussed in detail [here  - add link later] 

   *why is it limited to 1 per RCC?* 
        - since we have two RCC both of the following cases apply at the same time:   

    - Ahs A has N candidates with N+1 cells but we know x is in B then A is reduced by 1 cell and has N candidate with N cells making it a hidden set

   *And* 

   - Ahs B has N candidates with N+1 cells but we suppose x is in A then B is reduced by 1 cell and has N candidate with N cells making it a hidden set

- Since both sets are now hidden sets, adding any more RCC would make 1 of them have more candidates then available cells a construction rule violation: 
   (N candidates  with  (N-1) cells)

###### Can sets share candidates?   
  - yes, ahs sets can Overlap and share candidates as long as two limitations are strictly followed 

  - Ahs must contain new candidates so they cannot be full copies of each other

  - RCC cannot be used in any Shared candidate between sets

    - if they share a candidate any cell with that candidate is an invalid RCC
      - why AhS logic focused on A or b logic, overlaps allows A & B as possible so we cannot use the logic

# Working Logic: Putting it together
- Identify two AHS
- Find a RCC between the sets

 *now that we have a RCC and know that A or B can be a hidden set what does it mean?* 

  - Since we know that A or B can be a hidden set the Non RCC play's the next roll

*what is a non RCC?*

## Non Restricted Common Cell {nRCC}
 - All Ahs used share a second cell
 - This cell cannot be the RCC
 - Labelled Z

*What does Z candidates do*

 - When we have 1 RCC in a set
 - We know that A or B candidates can be a hidden set,
 - What we cannot discern is where those candidates are going to be 
 - If A and B have a Z candidate we gain some usable knowledge 
 - With Z being in both sets, and either set being locked we know that z will be somewhere in A or B 
 - Given this information we arrive out our first type and Named AHS function
 - All Candidates of A and B containing Z could have a Z 
 - Any  peer Candidate of All Z's of A and B  if solved as Z reduced A and B to less cells then Containers so they can be excluded else the puzzle has a construction rule violation. 
 - This is called the Ahs - XZ exclusion rule 

 ### Ahs - XZ:   Rule 
 - Ahs A) N candidates with N+1 cells
 - Ahs B) N candidates with N+1 cells 
 -  X) at least 1 RCC 
 -  Z) at least 1 non RCC 
 -  =>  eliminations all Peer candidates for Z of Als A and ALS B

 #### AHs - XZ: Double Link  Rule 
 - Application of the N AHS N RCC rule for 2 als's
 - Als A) N candidates with N+1 cells
 - Als B) N candidates with N+1 cells 
 -  X) 2 RCC 
 -  Z) both X's and any Non RCC 
 -  =>  Eliminations all Peer candidates for Z of ALS A and ALS B

*Additionally:*  
   
Als A non RCC are Restricted to AhS A:

- All peers of ahs A non RCC Candidates are eliminated

Als B all non RCC are Restricted to AHS B:

- All peers of Ahs B non RCC candidates are eliminated

# Symbols used in AhS &  How to read an AhS 
   - Ahs A) 1 (r4c36)  , B) 4 (r4c36) , x: r4c46, z: r4c46   => r4c46<> 2,3,4,5,6,7,8,9 
    - AhS tells us the class we are using
    - A & B...etc are letters representing the individual ahs 
    - ( ) or { } Shows the Cells the set uses
   -  Candidates its using listed  before or after the  ( ) 
   - X: RCC
   - Z: Elimination Candidates 
   - =>  implication

#Checks in reading or writing an AhS
  - The number of A's before the hS tell us the size {N}
  - We can verify that each ahs is correct size by counting the cells 
    - Making sure the  N candidate with N+1 cells is correctly build.     

#Practice Examples: 

##Hidden Pair:
- The smallest possible AhS-xz 
- Is the smallest possible AhS-xz Double linked rule  

 
### Does this mean other subsets are also AhS - xz Rules ? 
  - Yes it does 
  - Subsets can be  AhS-xz constructs 
  - When each candidate(s) of the subset can be viewed as N Candidate with N+1 cells 

  #### Can hidden subsets as an ahs-xz do more? 
    - Yes & No
    - Specifically it does something the Subsets can do but is missed in every single solver. 
    - Ahs-Xz double linked considers the position of cells in the set 
    - Where Subsets only care about the set matching the container and applying its reductions to the sector its found in for the set it used.

eg puzzle 


*The same move as an ahs:* 

- These missed eliminations are left out because its easier and faster to execute logic in a easy -> harder  fixed order
- Then trying to program all of potential eliminations of a move and let smaller logic clean it up where possible.
 - Subsets should be applying eliminations for each cells individually, most coders use the full set for eliminations. 

- Thus these can be intentionally missed
- But as a player, these should be included.

##### two Ahs's using two sectors 
   - Constructing an ahs uses one sector 
   - They can use the same sector as in the examples of the hidden Pair

   * What happens if the two AhS's use two different sectors? 
       - We exampled a hidden quad from 1 sector using two ahs
      - Can a subset be bent over 2 sectors? 
       - Yes the idea of Bending subsets created the next set of 
	   
Named techniques: Bent Almost Restricted hidden subset. {barhs for short} 

   - probably going to remove this section as i haven't seen anyone out side my own solvers attempt to do these. 

### practice Applications: 
 
example: 
3..6.79...7..12385....3....76.3..89...9.6..1343.....56.9.2.35...4.19..3..23..6..9

AHS - xz: 
a) 16 (r389c7)
b) 128 (r7c9,r8c79,r9c7)
x: r8c7
z: r9c7 
=> R9C7 <> 4 

### practice Applications: 
example: 

764..592.291.67..3538..267.387.261..942....676157.423.4762..395129..3786853679412

AHS-XZ: Double restricted Common elimination:
 
Ahs a)  4,9 (r2c4,r3c45)

ahs b)  1,3,8 (r1235c4 )

x: r2c4,r3c4

z: r2c4,r3c4 

=> r3c5 <> 1 , r5c4 <> 5

### Practice Application 
.45.........1...7.8...23......9.71........3...8.4.6.2...3.....5.7.8...36..83..9..

 AHS-XZ: Double restricted Common elimination:
A=123 {r1c1789}

B=1278 {b9p12489}

X=(1)r19c8,(2)r18c7 

=> r1c1<>679,r1c9<>89,r27c7<>2,r37c8<>1,b9p129<>4

### Practice application 
.........2.....3495...3926..9.........41..98....598..4..182...6......7....3..6...

AHS-XZ: Double restricted Common elimination:
A) 2,3,4,6,9 @ R1C123456

B) 1,5,8 @ R1C56,R2C56

X: R1C5,R1C4

Z: R1C5,R1C4

=>> r1c123<>8, r1c12<>1, r2c5<>6, R1C123456,r2c56<>7

### Practice application

.........2.....3495...3926..9.........41..98....598..4..182...6......7....3..6...
 AHS-XZ:
 
A) 1,5,8 @ R2C2345

B) 1,3,4,6,9 @ R1C12,R2C12,C3R2

x: R2C3

Z: R2C2

=> R2C2 <> 7

### practice Application 
..1...3.9.6...41.....13.5.64563287917....68..2.....6...9....263.....2418.24..39..

Ahs-xz Double restricted Common elimination:
set a ) 268 @ R12C45
Set B ) 359 @ R2C1345
x : R2C45
z: r2c45 
=> r2c1345 <> 278, r1c45 <> 75 

[next lesson: Almost hidden Sets - Intermediate Methodology ]

