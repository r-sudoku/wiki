 # /r/sudoku Wiki

Welcome to r/sudoku! Let's make this a great place, of high value to all of us, experienced and newcomers!

## What is a sudoku?

Sudoku (数独, sūdoku, digit-single) (/suːˈdoʊkuː/, /-ˈdɒk-/, /sə-/, originally called Number Place)
 
Is a logic-based, combinatorial number-placement puzzle. 

The objective is to fill a 9×9 grid with digits so that each column, each row, and each of the nine 3×3 subgrids that compose the grid (also called "boxes", "blocks", or "regions") contain all of the digits from 1 to 9. The puzzle setter provides a partially completed grid, which for a well-posed puzzle has a single solution. 


### Mathematics of sudoku: 

 *A sudoku is a constraint based satisfaction problem where the 9 digits must be allocated once in each of 27 sectors that makes up the 729 constraints.* 

  - There is preciously 6,670,903,752,021,072,936,960 different grids calculated in 2003
   
*[Ed Russell and Frazer Jarvis](http://www.afjarvis.org.uk/sudoku/sudgroup.html) were the first to compute the number of essentially different sudoku solutions: 5,472,730,538*

  - Essentially different as all valid transformations of a sudoku grid are computed: ie. applying transpose & swapping: band,stack,row,col  for 2*6^8 => {3,359,232} applications which also replicate the 9! digit changes.  

  ####[Issomorphism](https://www.reddit.com/r/sudoku/wiki/index/issomorphism)

  ####[Automorphism](https://www.reddit.com/r/sudoku/wiki/index/automorphism)  

*A paper by Gary McGuire, Bastian Tugemann, and Gilles Civario, released on 1 January 2012, explains how it was proved through an exhaustive computer search that the minimum number of clues in any proper Sudoku is 17* [paper](http://www.math.ie/checker.html)

  - Proper in regards that the starting grid has a unique solution. 

*An international group effort exhaustively searched all unavoidable sets for 17 clue formations with a unique solution [completed end of 2022](http://forum.enjoysudoku.com/post323538.html#p323538): finding 49,158 different grids*

 - [All known 17 clue grids](https://drive.google.com/file/d/1StS_Sm_Eh9ZJTapOsrRJccM6UP6PmQ3B/view) 

## Considerations when asking for or giving help

### Askers: 

**A picture is good, even better is also including the puzzle string**  

- If you post the puzzle string: list the given numbers and dots for the empty spaces  exemplar: 

.16...8.34.....61...2.61........7....5.634.9....9........41.2...37.....92.1...38. 


**Give an hint as to what you have tried already**
 
 - It's way easier to give a hint if we know what you have tried


**Include images that show full pencil markups** 

- Not only does this make it easier to help you, you might find something while you're notating


**Thank the person that helped you** 

- If you get help, please post a note thanking the ones that helped you, we are all humans and get very happy when someone says thank you :)


### Helpers:

**Be polite and understanding**  

- Not everyone has the same knowledge as you so try to understand the position of other people and don't talk down to them or be condescending, critique wisely and constructively we want everyone to keep on trying, and not to give up because someone was rude to them


**If unclear ask for what they have done so far**  

- A good hint is often to ask the helpee to fill in more candidates 


**Use spoiler tags or give vaguer hints first**  

- Often someone just need a push in the right direction, and it's more satisfying to just get a hint that pushes you in the right direction rather than just "Put X in rYcX"


 The Following Guides are best viewed in desktop Dark-mode as they have in-bedded images and pictures only show up in we-based browsers


# [Vocabulary:](https://www.reddit.com/r/sudoku/wiki/index/vocabulary)
 - quick reference  

##[Entry Level Terminology](https://www.reddit.com/r/sudoku/wiki/E-terminology/)
 * Vocabulary to be familiar with when reading about Sudoku puzzles and their solution for the first time
 
###[Beginners Level & Terminology](https://www.reddit.com/r/sudoku/wiki/B-terminology/) 
* Introductory solving methods:  Naked & Hidden subsets 
* Introductory solving method:  Box - Line Reduction

#Chaining  - Methodology
* Sequential learning guide for developing chain writing/reading skills
 
##[Intermediate Level](https://www.reddit.com/r/sudoku/wiki/I-terminology/)
* Designed as an entry level for A.I.C logic: discontinuous eliminations
* Covers and defines: Strong link, Weak Link, Weak inference
* How to build & look for the next link from a strong link 
* Covers chaining Value 
* Single Digit fish as chains: X - Wing, Skyscraper, 2-string Kite 
* How to use and build an Remote Pair {simplest xy - chain} 
* How to use and build an XY - wing {smallest bivalve chain with changing digits}

###[Competent Level ](https://www.reddit.com/r/sudoku/wiki/C-terminology/)
* Discusses Mini Sectors
* Expands Strong links into Grouped Strong Links
* Expands strong link for specialty grouped link: Empty rectangle Intersection 
* Grouped Weak-links
* Discuses how to link strong links for Location
* Intro to Named A.i.C chains: W-wing,M-wing,S-wing,L-wing,H-wing 

####[Proficient Level](https://www.reddit.com/r/sudoku/wiki/P-terminology/) [constructing]
* Designed for advanced A.I,C logic: Continuous eliminations
* Spotting the different ways A.I.C can form a loop

#####[Advanced Level](https://www.reddit.com/r/sudoku/wiki/A-terminology/) [ work in Progress] 
* Bifurcation - Breadth first searching over Depth first Searching 
* Forcing chains, using Weak links as implication starting points
* intro to Nice Loops, Turbots 

######[Graduate Level](https://www.reddit.com/r/sudoku/wiki/G-terminology/) [ work in Progress ] 
* Forcing Nets

# [Locked Sets  Entry level](https://www.reddit.com/r/sudoku/wiki/L-terminology/)
 * This topic identifies locked sets by size and name
 * This topic covers their exclusions

## [Almost Locked Sets - Begginers](https://www.reddit.com/r/sudoku/wiki/ALS-terminology/) 
*  Entry level for Sudoku solving using Sets instead of chains.
*  This topic covers what is an ALS,
*  How to use ALS - xz rule and double link rule
*  Intro to named ALs-xz types: XY - Wing, XYZ- Wing, Wxyz - Wing, XY - Ring 


    ###[ Almost Locked Sets  - Intermediate ](https://www.reddit.com/r/sudoku/wiki/I-ALS-terminology/) 
    * This topic covers the ALS-XY rule and Als-XY triple link Rule 
    * ALS as a chain adding more links past 3. 
    
    #### [Almost locked Sets - Advanced ](https://www.reddit.com/r/sudoku/wiki/A-ALS-terminology/) [Constructing] 
  * This topic covers expanding locked set structure to N cells with N+X freedom
   * Where X is a flex range of > 1 to (9 - N)   
   * Sue De Coq 
   * Death Blossom 
   * Distributed Disjointed Subset

##[Almost Hidden Sets - begginners](https://www.reddit.com/r/sudoku/wiki/b-AHS-terminology/) [ construction]  
 * Entry level for sudoku solving using hidden sets  
 * This topic covers what is an almost hidden set
 * How to use ahs-xz and ahs double linked rule.
 
#[Almost locked sets + AIC - expert lvl topic](https://www.reddit.com/r/sudoku/wiki/ALS_AIC/) [Constructing] 
 * Using RCC as weak links in AIC Chains
 * Named als+aic chains: Als W,S,M - wings & rings  

# [Fish - Basics level Methodology](https://www.reddit.com/r/sudoku/wiki/Fish-basics-terminology) 
* Templates and single digit omissions - Nisho 
* Math Constructs to explain Template omissions: Set Theory 
* Fish Terms - Base,Cover sectors : N x N 
* Entry level Types: Row & Col only for base/cover
    - Cyclopes  Fish {BLR}
    - X - Wing
    - Sword Fish
    - Jelly Fish 

 ## [Fish - Intermediate](https://www.reddit.com/r/sudoku/wiki/Fish-Intermediate-terminology) 
  * Finned & Sashimi types
  * Franken Fish  adding boxes to Base & Cover
  * Mutant Fish - mixing Row/Col/Box in base and cover
  * Examples for: N x N + Fin
     - Skyscraper
     - 2 - String Kite
     - Empty Rectangle  
     - Finned: X - wing, Sword fish, Jelly fish
     - Sashimi: X - wing,  Sword fish, Jelly fish  
       
 ### [Fish - Advanced](https://www.reddit.com/r/sudoku/wiki/Fish-Advanced-terminology)  
  * Endo Fin types
  * Example Fish size 4:  Nxn + fin + endofin
  * Beyond Size 4 Fishing  

  ####[Fish - Expert](https://www.reddit.com/r/sudoku/wiki/Fish-Expert-terminology) {construction}
  * No Fish: Broken Wings [ to be added ]
  * Kraken Fish
  * Alternative fishing methods: N x (N + K) - solving for fish and no fish. 
  
  #####[ Fish - Professional ](https://www.reddit.com/r/sudoku/wiki/fishing-professional-terminology/) 
   * Combining Fish for Siamese types
   * Muti - Fish: more then 1 digit same fish pattern 

# [Technique Master List](https://www.reddit.com/r/sudoku/wiki/techniques)
 - A list of all techniques categorized by Logic type: set theory, Graphing Theory

# Online Reading Resources:  
* [Enjoy Sudoku forum](http://forum.enjoysudoku.com/) 

* [Sudoku Coach](https://sudoku.coach/)

* [Daily Sudoku forum](http://www.dailysudoku.com/sudoku/forums/index.php)

* [Sudowiki- formally Scanraid.com](https://www.sudokuwiki.org/Getting_Started)

* [Suedocue](https://www.sudocue.net/guide.php) 

* [JSudoku](http://jcbonsai.free.fr/sudoku/JSudokuUserGuide/chainsTechniques.html)

* [Sudopedia](https://www.sudopedia.org/wiki/Main_Page)

* [Sudopeida-mirror](http://sudopedia.enjoysudoku.com/Solving_Technique.html)

* [Programmers Forum defacto restored mirror](http://programmers.enjoysudoku.com/)

* [Sudoku9981](https://www.sudoku9981.com/sudoku-solving/)

* [Sudoku Snake](http://www.sudokusnake.com/techniques.php)

* [xsudo](https://sudoku.allanbarker.com/sweb/general.htm)

* [Hodoku](https://hodoku.sourceforge.net/en/techniques.php)

* [Sudoku Assistant](https://www.stolaf.edu/people/hansonr/sudoku/explain.htm)

* [Simple Sudoku](http://www.angusj.com/sudoku/hints.php)

* [Phills Folly](https://www.philsfolly.net.au/Sudoku/index.htm)

* [Hidden logic of Sudoku - Denis Berthier](https://www.researchgate.net/publication/280301600_The_Hidden_Logic_of_Sudoku)

* [Hidden logic of Sudoku Volume 2 - Denis Berthier](https://www.researchgate.net/publication/278797333_The_Hidden_Logic_of_Sudoku_second_edition_-_Introduction)

* [Pauls Page](https://paulspages.co.uk/sudokuxp/howtosolve/)

* [txt page](https://homepages.cwi.nl/~aeb/games/sudoku/)

* [John Welch - Blog](https://sysudoku.com/)
   - Tends to not follow standardized notes,names or concepts.  
   - Makes reading difficult when familiar with common notes. 

# Puzzles Collections

* [Collected ZIP of many puzzles in SDM format] 
(https://drive.google.com/drive/folders/1e_hQNQiJVxhHP_5WBQhBNur9dnS5ml3E)

# Video Sources

* [Cracking the Cryptic] (youtube)](https://www.youtube.com/channel/UCC-UOdK8-mIjxBQm_ot1T-Q)  
- Daily classical and variant solves of sudoku puzzles

* [Sudoku Swami (youtube)](https://www.youtube.com/channel/UCdh4SoUiHPACqY1SGumgKYQ)  
  - SS has probably the most in depth sudoku tutorials on the web

* [u/dxSudoku (youtube)](https://www.youtube.com/channel/UC2N60jDPloV5_imTYKIVH2Q/videos/videos)
* [BremSter:](https://www.youtube.com/c/BremSterPuzzles)
* [Memeristor:](https://www.youtube.com/@memeristor)
* [Rangsk:](https://youtube.com/Rangsk)
* [Smart Hobbies:](https://www.youtube.com/@SmartHobbies)
* [Unshackling Sudokus & Puzzles:](https://www.youtube.com/@unshacklingsudokuspuzzles)
* [zetamath does puzzles:](https://youtube.com/zetamathdoespuzzles)

# On-line Solvers {web apps}

* [Sudoku Coach](https://sudoku.coach/)

* [Sudoku Assistant](https://www.stolaf.edu/people/hansonr/sudoku/)

* [Sudowiki- formally Scanraid.com](https://www.sudokuwiki.org)

* [sudoku Slam](https://www.sudokuslam.com/)

* [linky sudoku](https://sudoku.simonton.app/)

* [Enjoy sudoku](http://www.enjoysudoku.com/webplay/)  
- Enjoy sudoku, on the web.

* [f-puzzles:](https://www.f-puzzles.com/)

# Variants solvers: [to be added as request increase in frequency] 
## Killer sudoku: sum45, tips & tricks, combo cheat sheets
* [Puzzlegenius](https://puzzlegenius.org/killer-sudoku-from-scratch/)
* [Godoku](https://godoku.com/play/killer/combinations/)

# Downloadable GUI Programs:
## Recommended 
* [Hodoku](https://hodoku.sourceforge.net/en/)
* [YZF's solver](http://forum.enjoysudoku.com/yzf-sudoku-t36846.html)
* [xsudo](https://sudoku.allanbarker.com/)

### Others 
* [Sudoku Snake](http://www.sudokusnake.com/])
* [Sudoku susser](https://www.madoverlord.com/projects/sudoku.t)
* [Simple Sudoku](http://www.angusj.com/sudoku/)
* [Rangsk's Sudoku Solver](https://github.com/dclamage/SudokuSolver/wiki/installation-guide)
  - supports many variants and integrates with f-puzzles): 

### Program for rating difficulty
* [Sudoku Explainer](http://gsf.cococlyde.org/download/sudoku/)
  - Used as the standard for all rating puzzles among the forum players as it has a fixed disclose hierarchy

# Organizational staff:

*List of known authorized users with recent activity:*

* u/hosieryadvocate - moderator 

* u/charmingpea - moderator

* u/jblosser - moderator 

* u/strmckr -  Wiki mod

* u/okapiposter - moderator

In  our opinion and presumably the opinion of others, this wiki should represent considered community consensus, inclusively, so that responses to questions on the sub may be more efficient and complete and coherently answered with  definitions covered herein.