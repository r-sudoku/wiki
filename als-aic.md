This topic is the culmination of several techniques combining them into one cohesive logic set. 

In the topics of [Almost locked set](https://www.reddit.com/r/sudoku/wiki/I-ALS-terminology/) it was discussed that it was possible to chain together ALS nodes to form a chain. 

What was not mentioned in the previous topics is that ALS can be written as AIC chains where the RCC is the [weak inference](https://www.reddit.com/r/sudoku/wiki/I-terminology/) between the ALS node. 

- Therefor each and every ALS is actually a Strong link construct. 
 
#ALS + AIC 

- Instead of just limiting ALS chains to use only ALS as nodes, 
- We can expand AIC nodes by using the RCC of an ALS as a weak inference in an AIC
- Combining the two techniques into one powerful yet often hard to spot and use technique to its fullest abilities as it has both als & aic properties to spot.  

## Digesting the above technique easier:
- I developed this expansion of some more common techniques discussed [W,S,M: wing](https://www.reddit.com/r/sudoku/wiki/C-terminology/)
-  by expanding the bivalves {size 1 als}  into >1 size als 

### [ALS - W - Wing:](http://forum.enjoysudoku.com/als-w-wings-rings-t36860.html)
* the first and easiest to expand concept is the W - wing as its fairly common.
* each bivalve of the W wing is an ALS size 1, we change this to be any size
  
-  TYPICAL W -WING:  (a=b) - (b = b) - (b=a)    peers of start and end <> a
-  Expanded W - wing:  (ac=b) - (b = b) - (cb=a)   peers of start and end <> a,c

*example: 

    +--------------------+------------------+---------------------+
    | 1       23   236   | 4      3567  367 | 5678   568(3)  9    |
    | (3467)  5    (346) | (367)  8     9   | (167)  2       1(3) |
    | 367     9    8     | 1      3567  2   | 567    56(3)   4    |
    +--------------------+------------------+---------------------+
    | 2346    234  1     | 367    367   5   | 468    9       38   |
    | 5       8    346   | 9      2     36  | 46-1   (136)   7    |
    | 36      7    9     | 8      4     1   | 2      (36)    5    |
    +--------------------+------------------+---------------------+
    | 39      6    7     | 5      1     8   | 39     4       2    |
    | 8       1    35    | 2      9     4   | 35     7       6    |
    | 249     24   245   | 367    367   367 | 1589   158     18   |
    +--------------------+------------------+---------------------+

als-W-wing: (1467=3)r2c1347 - (3)r2c9 = r23c8  - (3=16)r56c8 => r4c1 <> 1 

#### ALS - W - Ring:
* same as the above except the first and last nodes are also share a RCC to each other closing the loop causing more eliminations.

*example: 

    +-------------------+----------------------+-------------------+
    | 1     (478)  26-8 | (278)   9     (2468) | 27   5     3      |
    | 9     (78)   5    | (278)   1     3      | 4    6     27     |
    | 2346  34(7)  236  | 5-2(7)  (26)  45-26  | 9    1     8      |
    +-------------------+----------------------+-------------------+
    | 7     1      2389 | 6       238   289    | 358  4     59     |
    | 23    39-8   4    | 12389   5     1289   | 6    3789  79     |
    | 5     6      389  | 389     4     7      | 38   2     1      |
    +-------------------+----------------------+-------------------+
    | 8     349    1    | 2359    236   2569   | 27   379   245679 |
    | 36    5      7    | 4       2368  2689   | 1    389   269    |
    | 346   2      369  | 13589   7     15689  | 358  389   4569   |
    +-------------------+----------------------+-------------------+

 als W-ring: (48=7)r12c2 - (7)r3c2 =r3c4 -(7=2468)r1c46,r2c4,r3c5 - (4=87)r12c2 =>
r1c3,r5c2 <>8, r3c46 <>2,r3c6 <>6 
 

### [ALS - S - wing:](http://forum.enjoysudoku.com/als-s-wing-t36880.html) 
* the next easiest to expand concept is the S - wing, less known but equally common as the w-wing.  
* the middle bivalve of the S wing is an als size 1, changing it to be any size removes the restrictions 

- Typical S wing:  (a = a) - (a=b) - (b=b)   a<>b, b<>a
- Expanded S wing  (a = a) -(a=bc) - (b = b)   a<>b, b <>a

* example to be added:


### [ALS - M - Wing:](http://forum.enjoysudoku.com/als-m-wings-rings-t36866.html) 
* the hardest of  named als - chain wings
* has 1 bivalve, but invokes more aic rules for digit transference's in overlaps of sub nodes

- Typical  (a=b) - (b=b) - (a=a)   peers of a <> a
- Expansion (ac=b) - (b=b) -(a=a) peers of a <> a

*example to be added: 

#### ALS - M - Ring:
* same as the above except the first and last nodes are also peers of each other closing the loop causing more eliminations.

*example to be added: 

# Closing notes: 
I will leave it in your good graces to find your own creation of these as there is countless ways to combine als nodes with standard aic nodes, and if you venture enough you'll also find out you can use AHS nodes as well.

