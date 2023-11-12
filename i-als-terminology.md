This topic will cover the next level of ALS set logic by adding more Sets of ALS and figuring out what we can do logically with more sets in sequence.

To understand the more advance concepts in this topic please familiarize your self with previous topics
[Almost Locked Sets - Beginners Methodology](https://www.reddit.com/r/sudoku/wiki/ALS-terminology/)

# Joining ALS together via shared candidates
- Each ALS can add new ALS   
   - With the same ideas in the last topic we find a New RCC between these sets
   - If they have one ADD another letter and we go From A),B),C)* <- new
   - each letter can be intrepid as a node in terms of chaining

 ## Shared Candidates are a "Weak inference" in terms of chaining 
   - A collection of ALS can be considered a chain weakly inferences by the shared candidates 

## ALS is a Strong Link 
   - Strong link in that its (Shared digit is True or it is N candidates in N cells ) 

 ## Construction Restriction 
  - Each New set Uses a Different RCC  then the previous connection 
   - Eg:  if sets A & B  x:3  then B & C cannot use 3

     *why?* 
     - Same idea as ALS-xz we want the Als to reduce each other by 1 candidate 
     - if A & B x:3, and B & C x:3 
        -The only information we gain:
            - (A & B) have a potential Z restriction 
            - (B & C) have a potential Z restriction 
             -  Effectively performing two als-xz rules {gaining nothing new}

  ## concepts     
    - By adding the Construction restriction we gain something new math wise

   - If x is in A then B is reduced by one candidate becoming (n cells with N candidates)     
   - If x is in C then B is reduced by one candidate becoming (n cells with N candidates) 
   
*This is the most important view point Gained* 

- If A & C both solve for X, B will have been reduced twice for (N cells with n-1 candidate) a construction rule violation. 
   
  ## Piecing it together: 

     *How do we use this knowledge?*

         eg  (A & B) x:3, (B & C) x:4 
                    
         If A is 3 then B is reduced to N cells with N candidates 
         - B must contain 4 other wise a construction error occurs
          thus 4 is in B, then C is reduced by 1 candidate for (N cells with N digits.

        If C is 4 then B is reduced to N cells with N candidates 
         - we know B must contain 3 other wise a construction error occurs
         - since we proved 3 is in B, then A is reduced by 1 candidate for (N cells with N digits

        IF B is 3 & 4 then A & C are both reduced by 1 candidate each for N cells with N digits 

 ###Finding a commonality,
 - The three scenarios all show something useful,
  - X's are fixed to A or B or C so they aren't useful
  - However depending on where they fall we find that A & C end up as N cells with n candidates 
 - If those fixed cells of A & C have a nRCC we find the next level of ALs eliminations: The ALS - XY Rule.  

 #### Als - XY Rule: 
   - The nRCC of A & C is labelled "Y"    
   - All peers of "Y" of A & C may be excluded 
   - Any peer cell of All y's of A and C if solved as Y reduced A and C to less digits then Containers so they can be excluded else the puzzle has a construction rule violation. 

 #### what about the "Z" exclusions 
     - Yes, "Z" eliminations are still applicable between each pair of sets (A & B), (B & C) etc
     -Also there is:  "Z" nRCC to all als [A,B,C] peers of A,b,c for this Z may be excluded 
    
    ##### Can each linked als have 2 RCC 
      - Yes these eliminations are still applicable to each pair (A & B), (B & C) etc
 - normally "Z" eliminations are skipped as they should be found by the ALS-XZ rule in hierarchy searching 

##### The N ALS N RCC rule:
  - Yes, this is applicable to ALS - XY wings
  - Called the Triple Linked Rule

###### How do we identify this feature  to use it?
- Just like the als xz version with 3 als, we need Each ALS to have 1 link
 
- In the Als-xy wing A & B & C  have 2 links we need one more. 

- The als-zy wing A & C aren't linked 
  - If (A & C) has a 3rd RCC that isn't used in (a & B's) and (b & C's) 
     - We can add this the 3rd RCC 
       - Adding this link allows each als to reduced all others to locked set        so that we have N sets of N+1 candidates is reduced by N RCC to be N sets of n candidates in N cells satisfying  the container

   ###### Can A & C have 2 RCC 
   - Yes these eliminations are applicable to (A & C)

 ###### How to use the Triple Linked Rule 
   - X's of (A & B ) are locked to cells of A & B
   - X's of ( A & C ) are locked to cells of A & C
   - X's of ( A & C ) are locked to cells of B & C 
    - Exclude all peers for each nRCC of als a)
    - Exclude all peers for each nRCC of als B) 
    - Exclude all peers for each nRCC of als C) 
    - All three sets can be a & C respectively 
     - Identify and perform "Y" elimination for (A & B), (A & C), (B & C), (A & B & C)
      - "z" eliminations can be skipped as "Y" mimics it exactly
 
#Working Logic: Putting it together
   - Identify Three ALS : a,b,c
   - X) Find a RCC between (two or three) als 
   - y) Identify nRCC between (A & C)
   - => eliminations all Peer cells for Y of Als A and ALS B
   - Check for triple link rule trigger     

*if you choose to have this feature.* 

   - Identify "z"s from (a & b), (b & C) (a & C), (A,B,C) 
   - => eliminations all Peer cells for Z of Als A and ALS B
   - => eliminations all Peer cells for Z of Als A and ALS C
   - => eliminations all Peer cells for Z of Als B and ALS C
   - => eliminations all Peer cells for Z of Als A and ALS B and Als C

# ALS - Chain 
 - This is the final phase of ALS Logic
 - A collection of ALS nodes greater then 3 is a Chain
 - Expanding each new ALS via RCC rules outlined here in
 - The Rules of eliminations do not change First and last node = Y eliminations
 - Z elimination Rules for each set joined by a RCC
 - Z elimination for Common candidate for all the ALS used 
 - Check the last Node if it can have a RCC to the first one 
      - If there is N RCC links we have trigger the N AlS N Rcc Rule 
 
# smallest AlS - chain 
  - Uses only Bivalves 
  - Acts identically as an a.i.c - xy chain.
  - XY - wing  is also an als-xy rule as its constructed from 3 ALS  
    
# The conclusion 
  -  ALS & AIC  can overlap and perform identical eliminations the choices is which version of logic is easier to convey your point, or easier for you to find.

# Practice Puzzles 

## Example: XY - Wing
31...2958629538471..81.9623..3.9781...18.359.89..1536.736981245142356789985724136

- XY - Wing: 
 - als A) (46)r5c5
 - als B) (67)r5c2
 - als C) (47)r6c3  
 - X: 6,7
 - Y: 4
   -  => r5c1,r6c4 <> 4

## Example: ALS - XY rule

317289645569314827248756913.2.9.7...9...2.7.4.7.6..2..4..86237.73249..86....734.2

- Almost Locked Set XY - Wing:
 - als A) (189) r47c9 
 - als B) (59) r7c2 
 - als C) (158) r5c2,r6c1 
 - X:9,8 
 - y:1,8 
   - => r6c9<>1, r4c1<>8

#### Remarks 
  * Some solvers  make a distinction of "x" RCC between sets with another letter
  * Hodoku for example uses  x,y to indicate specific shared and "z" for  eliminations: Get to know how a visual aid/solver displays information goes along way in learning.  
 * like the one above looks like this in Hodoku
 - Almost Locked Set XY-Wing: A=r47c9 {189}, B=r5c2,r6c1 {158}, C=r7c2 {59}, X,Y=5,9, Z=1,8 => r6c9<>1, r4c1<>8

## Example: ALS - Chain  {N als N RCC rule}
  
..761.2..263475.........67.3....1789.....7...75.8.....685....271327.64..479.2....

 - XY - Ring
 - ALS A) (19)r2c8
 - ALS B) (18)r2c9 
 - ALS C) (58)r8c9 
 - ALS D) (59)r8c8
 - X: 1,8,5,9
 - Y: 1,8,5,9 
 - => R2c7 <> 1, r8c5,r9c789 <> 5, r9c9 <> 8

