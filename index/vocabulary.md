# Cell 
* the smallest indivisible square, of which there are 81 in the grid. Every cell represents the junction of three units as it lies in one row, one column, and one block.

# Row 
* a horizontal unit of 9 cells which must contain all 9 digits. There are 9 in the grid. R1 is the top row, and R9 is the bottom row.

# Column 
* a vertical unit of 9 cells which must contain all 9 digits. Again there are 9 in the grid. C1 is the leftmost column, and C9 is the rightmost column.

# Block or Box 
* a set of 3 x 3 cells that also must contain all 9 digits. There are 9 in the grid. B1 is the top leftmost and B9 is the bottom rightmost, going horizontally left to right.

# Givens
* the clues provided at the start of the puzzle.

# Digit 
* all big numbers that are either given or solved as known solutions.

# Candidate
* a potential digit solution to a cell notated by a small number.

# Elimination 
* the removal of a candidate which has been determined cannot be true.

# House or Unit 
* an unspecified area of 9 cells that must contain all 9 digits. There are 27 in the grid. This may refer to a row, column, or block. Commonly used when communicating a technique that can apply to any type of unit without having to say all three.

# See aka Peer
* candidates or cells which share at least one common house are said to 'see' each other and are therefore related.

# Band 
* a horizontal grouping of three rows including a three full blocks (rows 1-3, 4-6 7-9). May also be referred to as a horizontal Chute, Tiers or Floors.

# Stack 
* a vertical grouping of three columns including a three full blocks (columns 1-3, 4-6 7-9). May also be referred to as a vertical Chute or Tower.

# Set 
* 1. the state of a single number and all of its solutions and candidates. 
* 2. The state of numbers 1-9 in a house.

# Locked Set 
* an arrangement of candidates in a house that has a number of possible solutions equal to the number of candidates. Common examples are Naked and Hidden Pairs and Triples.

# Almost Locked Set or ALS 
* a group of cells in a house containing one candidate more than the number of cells such that if one candidate is removed from all cells it would become a locked set.

# Multiple Locked Sets or Almost Locked Sets 
* can interact to identify eliminations, such as in the Sue de Coq (a technique named for the alias of it's inventor).

# Mini-line 
* a 1 x 3 line of any row or column within a single block. There are 27 mini-lines of rows and 27 of columns in the grid, three of each within each block.

# Bi-Value  or Bivalve
* any cell that contains only two possible candidates, used to communicate chains and uniqueness techniques. Often abbreviated BVC. This may also be applied to a House or Unit where there are only two possible candidates for a particular digit.

# TRUE 
* a proposition that assumes a specific candidate to be the correct digit for a specific cell.

# FALSE 
* a proposition that assumes a specific candidate cannot be the correct digit for a specific cell.

# Strong link 
* a logical statement “if this candidate is FALSE, then that candidate must be TRUE.” Both candidates cannot be FALSE at the same time. This logical proposition can be applied to two candidates in the same house, or two candidates if they are connected by a chain.

# Weak link 
* a logical statement “if this candidate is TRUE, then that candidate must be FALSE.” Both candidates cannot be TRUE at the same time (but they may both be FALSE. This logical proposition can be applied to two candidates in the same house, or two candidates connected by a chain.

* It is possible for two candidates to be both strongly linked and weakly linked at the same time. in other words, these two statements are not necessarily mutually exclusive.

# Chain
* a testable hypothesis using a sequence of strong and/or weak links to find a relationship between two candidates in the grid. This may take the form of a contradiction, or to determine a strong link between candidates at end points of the chain which appear to be otherwise unrelated. Chains form the basis of most advanced techniques in Sudoku.

# Alternating Inference Chain or AIC 
* A chain composed of alternating Strong and Weak links, which allows TRUE or FALSE propositions to be applied to candidates to determine potential eliminations.

# Loop 
* a continuous closed chain whereby candidates affect each other in sequence. As a consequence, all weak links become strong.

# Grouping 
* linking more than one candidate in a single node of a chain. Grouping is used to mean “one of these” or “all of these”.

# Wing 
* a simple chain or ALS that has been given a name. Wings are a method of drawing a conclusion by universally recognized pattern recognition rather than manual chaining.

# Fish 
* a number of rows or columns with a number of candidates each which share an alignment with each other. The magnitude of the fish determines the name it will have.

#Fin 
* a single candidate that prevents a fish or locked subset from being obviously true. A fin is strongly linked to its desired fish or subset, and is commonly used as an advanced chain starting point.

# Verity 
* a common conclusion reached by all possible angles of logic. A positively true statement that has passed all possible tests given.

# Uniqueness 
* a set of techniques which rely on the assumption that the puzzle has only one valid solution. Many people consider a puzzle with multiple solutions to be invalid as it cannot be solved logically. Solver programs are able to determine the number of solutions a puzzle has, and may be used as a quality control. Requiring a single solution is not defined in the original Sudoku rules but is a fundamental assumption behind some techniques.
