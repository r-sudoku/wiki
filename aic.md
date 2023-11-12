# Alternating Inference Chain (AIC)

## What is an Alternating Inference Chain

An alternating inference chain (AIC) is a sequence of links which alternates between strong and weak links, starting and ending with a strong link. Therefore, an AIC always consists of an odd number of links.

An AIC creates a strong link between its ends. Therefore, a candidate which is weakly linked to both ends of an AIC can be eliminated.

## Examples

The first example is a standard example of an AIC. In the following diagram (taken from https://www.reddit.com/r/sudoku/comments/f9x9fe/extreme_hodoku_score_3676/), the 7s in row 4 are strongly linked. Furthermore, the 2s in row 4 are strongly linked and there is a strong link between the 2 and 7 in r6c5. These three strong links can be chained together through the weak links between the 2 and 7 in r4c7 and the 2s in box 5. The complete chain then reads:

r4c2 <> 7 -> r4c7 == 7 -> r4c7 <> 2 -> r4c4 == 2 -> r6c5 <> 2 -> r6c5 == 7.

Since the 7 in r6c3 is weakly linked to both ends of the chain, it can be eliminated.

https://i.imgur.com/tISEyma.png

Many low-difficulty strategies are actually examples of AICs, the most basic one being the pointing pair. In the example below (taken from https://www.reddit.com/r/sudoku/comments/fbgel9/moderate_hodoku_score_1754/), there are only two places in box 8 where a 6 can go. As a result, there is a strong link between the 6 in r9c4 and the 6 in r9c6. Since the 6 in r9c8 can see both 'ends' of the chain, it can be eliminated.

https://i.imgur.com/tUOR3St.png

A bit later on in the same puzzle, one encounters another basic type of AIC: the naked pair. In the diagram below, there are strong links of type C in both r9c1 and r9c9. Since the 1s in those cells are weakly linked, we can chain the strong links together:

r9c1 <> 3 -> r9c1 == 1 -> r9c9 <> 1 -> r9c9 == 3.

The remaining 3s in r9 see both ends of the chain and therefore can be eliminated. Similarly, we could have chained the strong links together through the weak link between the 3s in r9c1 and r9c9, which eliminates the 1 from r9c8.

https://i.imgur.com/BfuBCaM.png

## Classifying Chains

For a simple AIC, every link (weak or strong) is either between different digits in a cell (which we call type C) or between identical digits whose cells share a house (type H). AICs are virtually unlimited in their power to chain different types of links to produce different types of chains. For example, an AIC which consists of exactly 2 strong links and 1 weak link can take vastly different forms:

 * Type ChC: two bi-value cells which share a house. If this produces an elimination, it is a naked pair.

 * Type HcH: two bi-location digits which share at least one cell. If this produces an elimination, they must share both cells, in which case it is a hidden pair.

 * Type HhH: two type H strong links on the same digit. All Turbot Fish are categorized by this type, only distinguished by which types of houses are involved:

  - If the weak link is a box, this is a Two-String Kite;

  - If one of the strong links is a box, this is a Turbot Crane.

  - If none of the links is a box, this is a Skyscraper. Note that X-Wings do not get their own type, since they are nothing more than two Skyscrapers.

For AICs with 3 strong links, this is already more complicated, where not every type has a given name yet. The types with names are:

 * Type HhHhH: this is an ordinary X-chain.
 * Type ChHhC: W-Wing.
 * Type ChChC: Y-Wing.
 * Type HhChH and type ChChH: Windmill.

## Types of Eliminations

Any candidate which is weakly linked to both ends of an AIC can be eliminated. Since these weak links can be of type C or type H, there are 3 different types of elimination:

 * Type HH: if both links are of type H, then both ends of the chain are the same digit as the elimination. This is the most common type of elimination.

 * Type CC: if both links are of type C, then both ends of the chain ended up in the same cell. This elimination is less common, but does occur as a hidden pair elimination.

 * Type CH: if there is one link of both types, the ends of the chain are on different candidates in different cells. This type of elimination is more uncommon, and is most easily missed by a human player. An example can be found in the following diagram:

https://i.imgur.com/a2MR2w3.png

## External sources

 * https://www.sudokuwiki.org/Alternating_Inference_Chains
 * https://www.sudokuwiki.org/AIC_with_Groups
 * http://hodoku.sourceforge.net/en/tech_chains.php
 * http://sudopedia.enjoysudoku.com/Alternating_Inference_Chain.html

