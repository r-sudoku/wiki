This Chapter we will  be an expansion of topics covered under [Almost Locked Sets - Begginers](https://www.reddit.com/r/sudoku/wiki/als-terminology/) and 
[Almost Locked Sets - Intermediate](https://www.reddit.com/r/sudoku/wiki/I-ALS-terminology/) 

Specifically this chapter will cover [Degrees of Freedom](https://www.reddit.com/r/sudoku/wiki/als-terminology/#wiki_degrees_of_freedom):

# Degrees of Freedom 
 - Can be N size with N+x digits
   - x has a limit just like a puzzle, there is only 9 candidates
   - if we have N cells x at most can be (9 - n) 
       - eg. 1 cell can have at most 8 extra candidates
       - 1 cell with 1+8 => 1 cell with 9 candidates
 - written out for each (X-1) we add another "a" in-front of the almost  
 -  AAAAAAA almost locked set  {using the 1 cell with 8 extra candidates)
 - or short hand A^8 lmost locked set {not a common practice as few use size beyond the AAls}
- X size +1 is already covered in the last 2 chapters these will not be found herin.

* Just like the last chapter we are looking to construct a method that will allow us to deduce some where with in connected sets a common digit can be found.

* Unlike last chapter how we can connect them is dependant on the number of freedoms the first A*ls has. 

# Freedom of x: 
  * The more freedoms of x we have the more almost locked sets are required to reduce the first set down to a locked set.
 * Specifically each added ALS is a degree of freedom 1 ie n cells with N+1 digits

## Building freedom of x: 
* select N cells that house N+x candidates where x > 1 (label it A)

### Connecting to Freedom of x: 
* For each x we need to add a new als, with a new RCC to the first als picked.
* Each Als may have overlapping cells as long as a new cell is added,
* The RCC does not occur in the overlap of the 1 set and the new one added 
* Each als may have 2 digits in common to the A)
* Each als may have 1 common candidate (Z) this may not used as the RCC as this candidate will be locked to the x+1 sets.  
* label the new als (b -> z)
* Each new RCC added may be given a designation I will us X for all of them. 

## Application of X added ALS
* For each RCC added (labelled x) set then A) is reduced by 1 digit 
* When there is x als each with 1 RCC, with the RCC placed in all the adjoining als we reduced the first set by x digits leaving it as n cells with N digits. 
* if the A) holds all x digits then each of the x als linked to it are also reduced by 1. 
 * Thus any common nRCC (labelled Z) of all als used is restricted to occurring with in cells selected where by any cell that sees all copies of the nRCC may be excluded.

### Freedom of x Rule  - [Math](http://forum.enjoysudoku.com/almost-locked-rules-for-now-t2510.html)
* If A is an Als  with degrees of freedom of x
* and we have a collection S of x disjoint ALS (that are also disjoint with A) 
* each of the ALS has different restricted common with A
* and z common to A and all the members of S
* then we cant have z in a cell that can see all the z candidates in A and all the members of S.

* Example Puzzle: 

*  ALS{ DOF X}  N * X RCC rule    

+--------------------+---------------------+---------------------+

| 39-1  (1379)  2579 | (17)  1247    8     | 1459  123459  6     |

| (16)  4       257  | 3     1267    9     | 8     125     12    |

| 8     (1369)  29   | 5     1246    46    | 7     12349   1234  |

+--------------------+---------------------+---------------------+

| 39    3589    1    | 679   345679  34567 | 2     4679    478   |

| 7     (39)    4    | 2     8       36    | 169   169     5     |

| 2     589     6    | 179   14579   457   | 3     1479    1478  |

+--------------------+---------------------+---------------------+

| 4     267     3    | 8     567     1     | 56    2567    9     |

| 169   1679    79   | 4     35679   2     | 156   8       137   |

| 5     12679   8    | 679   3679    367   | 146   123467  12347 |

+--------------------+---------------------+---------------------+

* ALS{ DOF x}  N * X RCC rule  
* A)13679 @ r235c2 { size 2 DOF }  
* b) 17 @ r1c4      [b & c are the collection of S with 2 DOF worth of RCC] 
* c) 16 @ r2c1 
* x: (AB)17 ,(AC)16  [ each b,c has a unique rcc 7,6 ] 
* z is 1, its in A & all members of S [BC] then all peers of all "1"s are excluded 	 
	=>  r1c1 <> 1 

# proof 
  if we place 1 in r1c1, then B & C resolve as a locked set placing 6, and 7 reducing A) to having 3 cells with 2 digits a construction violation.

Just like the last Chapter of basic ALS these too have N als with N RCC elimination rules  where all sets involved become a locked set. 

# Freedom of x:  N digits - N RCC rule {Label M} 
 * Each als Added brings a RCC 
 * When all RCC combined is the same as the digit set of the A)

## Application of N digit - N RCC Rule 
 * A is reduced to no candidates if it A) hold no RCC. 
 * Thus A) must house a digit from each ajoining set.
 * Each adjoining ALS cannot house both digits as that would be N cells holding n+1 digits a construction violation, therefor A) must house at least 1 digit
* because A and each corresponding als RCC are locked to A) or the ALS 
    -  the RCC of each attached Als + A)  peers are excluded for the RCC
* All nRcc candidates are locked to there respective ALS and peers are excluded
* Z nRCC  of all sets peers are also excluded. 

* Example puzzle: 

+-------------------+---------------------+------------------+
| 459    1     479  | 78    3      (89)   | 2     58    6    |
| 59     569   679  | 278   289    4      | 35    1358  13   |
| 8      3     2    | 5     6      1      | 7     9     4    |
+-------------------+---------------------+------------------+
| 139    7     139  | 6     4      5      | 8     123   1239 |
| 6      28    134  | 9     28     7      | 34    13    5    |
| 24     289   5    | 238   1      23-8   | 49    6     7    |
+-------------------+---------------------+------------------+
| 7      4     39   | (23)  59-2   6      | 1     235   8    |
| 12359  2569  1369 | 4     589-2  (2389) | 3569  7     239  |
| 2359   2569  8    | 1     7      (239)  | 3569  4     239  |
+-------------------+---------------------+------------------+



* Aals 
 * A) 2389 @ R89C6 
 *  B)  23 @ r7c4
 *  C)  89 @ r1c6
 *  X: (23), (89) 
 *  Z :   
 *  M : (2,3,8,9)   
     => r6c6 <> 8, r78c5 <> 2, 

### math proof 
* The rule can be put very simple:
* A subset of N cells sharing only N different digits is disjoint, 
* If all occurrences of the same digit share one common sector.
* This means that none of the N digits can be true more than once in the subset,
* because all instances of this digit within the subset can "see" each other.
* Every candidate outside the subset that shares a sector with all occurrences of  
* the same digit within the subset can be eliminated.
* This follows because if such a candidate was true, it would eliminate this digit completely from the subset, leaving us with only N-1 digits for N cells.

# Classification : [Distributed Disjointed Subset](http://forum.enjoysudoku.com/distributed-disjoint-subsets-t5423.html) 
* D.D.S for short
* all the above information derives this solving technique
* it more commonly seen in 2 forms: Sue De coq, Deathbloosom 
* The distinction is the N Digits N RCC rule is the trigger along with some Criteria Sectors used. 

## Sue de Coq 
 - all RCC cells used occupy two sectors 

### Death Blossom 
 - all RCC cells occupy three sectors 

#### D.D.S
 - all RCC cells occupy >3 sectors 

 * Example D.D.S Six sector: 

7.6..5..43......9.......52......943.1....7..8...8....182..9..7.6.9...........3.. 

 +--------------------+-----------------------+--------------------+

| 7      (189)  6    | 239-1   23-18    5    | (138)  (18)  4     |

| 3      5      2    | 1467    14678    1468 | 178-6  9     (67)  |

| (49)   148-9  148  | 13679   13678    168  | 5      2     (367) |

+--------------------+-----------------------+--------------------+

| (25)   678    578  | 156     156      9    | 4      3     (27)  |

| 1      3469   345  | 23456   23456    7    | 29     56    8     |

| 29-45  34679  3457 | 8       3456     246  | 79     56    1     |

+--------------------+-----------------------+--------------------+

| 8      2      1345 | 1456    9        146  | 136    7     35-6  |

| 6      1347   9    | 1457    14578    1248 | 138    148   235   |

| (45)   147    1457 | 124567  1245678  3    | 1268   148   9     |

+--------------------+-----------------------+--------------------+

* D.D.S 
* A) 34679 @ r3c19 
 * b) 1389 @ r1c278
 * c) 245 @ r49c1
 * d) 267 @ r24c9
 * X: (3,9),(4),(6,7)
 * M: (3,4,6,7,9)
 * => R1c45 <>1, r1c5 <> 8, r2c7 <>6 , r3c2 <> 9 , r6c1 <> 45, r7c9 <> 6

# Notes and generalized Comments 
 - The Nature of N als with N+x digits, 
 - Many sets can be combined together to form smaller degrees of freedom sets.
 - however not all sets can be combined to make smaller sets.  
   - this distinction is the reason why many sue de coqs & death blossoms appear identical to als-xz rules  & or als-xy rules.

* Once you are comfortable at this level of solving  you might have a question or two

# can you use a freedom of x to link to a freedom of x ? 
 - yes, i will cover 1 type as the rest are purely academical and usually this search space runs into memory limits. 

for each a) freedom of x  we need to add x als to have it act as a Locked set

 ## Expanding structure: each linked als is a Freedom of x instead.  
  * if we choose to use freedom of x  instead of limiting it to als. (+1)
        * the freedom of x set must have +x RCC to the first set  
        *  ie +1 freedom needs 1 RCC, a +2 freedom needs 2 ect
        * each "x" added has the choice of being any size of freedom of x 
         
 

# Can you use the freedom of x + links  as a node ? 
  - yes its possible to collect the group and use its common restriction in chain like fashion 
 -  i will not cover these in full but i will say they obey the same rules of construction of the als xy - chain with special care for RCC's not being duplicated in similar space.

