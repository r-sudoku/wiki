
In chain concepts so far it has been discussed with examples of [Discontinuous](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_discontinuous.3A) A.i.C

By the end of this topic a player should be able to understand and apply [Continuous](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_continuous_aka_loop.28s.29.3A) A.I.C logic to chains found without having to iterate all the outcomes as mentioned [here](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_x_-_wing.3A)

To procedure into this stage ensure you are familiar with all previously discussed concepts as referenced below

[Entry Level Terminology](https://www.reddit.com/r/sudoku/wiki/E-terminology/)

[beginners Level Terminology](https://www.reddit.com/r/sudoku/wiki/b-terminology/)

[Intermediate Level Terminology](https://www.reddit.com/r/sudoku/wiki/I-terminology/)

[Competent Level Terminology](https://www.reddit.com/r/sudoku/wiki/C-terminology/)

All logic concepts in basics,Intermediate,Competent propagate into higher constructs without foundations concepts get increasingly difficult to follow. 

#Symbols used in Proficient solving

    => implies
    <> not equal to
    =  Strong Link 
    -  Weak Inference

# Identifying Continuous A.I.C 
- A written Chain gives the information needed to determine if its a loop or not
- Peer cell concepts are used frequently for identifying loops

- The Four types of Loop triggers: 
    - Direct Peer, Shared, Contradicting, Contradicting Peer 

## Direct Peer 
- Both Starting cell(s) and the Last Cell(s) are Peers cell(s) and use the same Value.
- The last cell as a truth inferences  the first cell is also false.
- First cell as a truth inferences the last cell is also false.
- Indicates the first and last cell can only be true for the sector.   

## Shared 
- Start and End Cell(s) are Identical with Same starting value
- Implies the starting value  Must be true. 

## Contradicting 
- Start And End Cell(s) are Identical with the end value and the starting Inferred Value the same.
- Indicates the starting Value can only be false 

## Contradicting peer
- Both starting cell(s) and the last Cell(s) are peer cell(s) and End Cell uses the inferred Value of the start. 
- Implies the starting Value must True as the inferred value cannot be true twice in a sector. 

* When constructing A.I.Cs Direct peers & Shared are the most important, if you happen to need Contradicting version you can drop 1 of the links away and have easier eliminations from a Discontinuous A.i.C" 

# Working Logic: Putting it together 
## Direct Peers - how to use it
 - Using our [example: x - wing again](https://www.reddit.com/r/sudoku/wiki/i-terminology/#wiki_x_-_wing.3A) as an example: 
    
..47.5...29....15..5891....52.49861....5.1...9.1.3..85..2856931..9...546..51498..

*we wrote a chain:*
 
*(7) (r2c3 = r2c9) - (r4c9 = r4c3) => R5C3 <> 7*

- r2c3 and r4c3 are peers {they share a Col} and also share (7) 
- Identifies it as a direct Peer type of loop. 

We can use this chain to write another one but this time we flip all the links       from strong -> weak inferences & Weak inference -> Strong 

 *(r2c3 - r2c9) = (r4c9 - r4c3)* 

Read the chain  left to right

- r2c3 is true and r2c9 is false and r4c9 is true and r4c3 is false

Read it left to right 

- r4c3 is true and r4c9 is false and r2c9 is true and r2c3 is false

Combine the truths: (R2c3 = R4C3), (R2c9 = R4c9) 

- Eliminate any peer that sees the combined truths 

- (R2c3 & R4C3) => R5C3 <> 7  { this one was given by the initial chain} 
- (R2C9) & R4C9) => r359c9 <> 7   <- the loop eliminations.

- The short cut method is to place brackets around the cells that have the "=" symbol between them as these must be true as a strong link. 
and use these new strong links as the elimination point. 

 *r2c3 - (r2c9 = r4c9) - r4c3*

### Named A.i.C's "Wings" Become "Rings"
 - Some of the Named AIC's may form as continuous A.i.C  when this occurs they become "Rings" instead indicating the loop

*Example Puzzle* 

.4...5..9..8...3.......9.7.7..2...4.3..5.6..2.6...7..1.2.9.......7...5..4..8...3. 

M-Ring: (9=8)r5c8 - (8)(r5c2 = r8c2) - (9)r8c2 = r8c8 => R8c8 <> 1,3

With this example we'll find another style of Direct Peer elimination 
 - a cell within the chain is Locked to the digits of the links.

- r5c8 and r8c8 are peers {they share a col} and also share (7) 
- Identifies it as a direct Peer type of loop. 

We can use this chain to write another one but this time we flip all the links       from strong -> weak inferences & Weak inference -> Strong 

(9-8)r5c8 = (8)(r5c2 - r8c2) = (9)r8c2 - r8c8

- next step is to add the information that gets broken up
- and compress like cells and use the digits for the exchange. 

 (9)r5C8 - (8)(R5c8 = r5c2) - (8=9)r9c2 - (9)r8c8

use the new strong links for the extra eliminations: 
 - (8)(r5c8 & r5c2) : has no eliminations
 - (8=9)r8c2: Cell is locked to these digits eliminate other candidates (1,3)
 - (9)(r5c8 & r8c8): no eliminators {normal elimination}

## Shared - how to use it

*Example Puzzle:* 
 
370401000061902400429006510002105649196248375040069821004607150057810000610500700

W - Ring {unorthodox version}: (8) r9c8 = r2c8 - (8=5)r2c1 - (5=8)r1c3 - r9c3 = r9c8 => r2c8, r9c3 <>8, r7c9 <> 8

first and last cell are identical: r9c8 & r9c8 with the same value expressed {8}

- Implies this cell can only be true
- Peer cells of r9c8 can be eliminated for the digit: r7c9, r2c8 & r9c3 
- note: the immediate linkage next to r9c8 is eliminated: r2c8 & r9c3 {as they are peers}

