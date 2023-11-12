# What is Wrong with Sudoku.com's “Evil” Category?

“Evil” is the last difficulty level of the Sudoku app/website Sudoku.com, after “Easy”, “Medium”, “Hard” and “Expert”. Many solvers try “Evil” puzzles expecting them to be considerably harder than “Expert”, and are then surprised that they often seem much easier instead. This observation is correct! **Puzzles from the “Evil” category are often very easy, comparable to “Easy” puzzles.**

## Were the Puzzles Always That Easy?

No, the until around October of 2022 (as seen in [this post](https://www.reddit.com/r/sudoku/comments/y1bv38/any_ideas_here/)) the “Evil” category contained only *very* hard puzzles that required many advanced techniques such as Alternating Inference Chains (AIC) and Sue-de-Coq to be solved. This subreddit was full of post made by intermediate-level solvers who got hopelessly stuck on these puzzles.

## So What Happened?

Around the beginning of 2022 it became more and more clear that something was strange about the “Evil” puzzles. Every solver's grid looked almost the same when they got stuck, with [three vertically aligned boxes (a “stack”) almost completely filled](https://www.reddit.com/r/sudoku/comments/tsj3d7/always_stuck_with_three_completed_columns_on_evil/).

### Finding the Flaw

In April of 2022 there [multiple](https://www.reddit.com/r/sudoku/comments/tux2if/sudokucom_evil_difficulty_key_point/) [posts](https://www.reddit.com/r/sudoku/comments/tvu2xx/sudokucom_evil_more_exploits/) by one solver who had found an “exploit” to crack the puzzles without using any complex techniques. The trick was based on spotting a certain arbitrary pattern in the grid and setting one cell based on that.

After [looking into it more closely](https://www.reddit.com/r/sudoku/comments/tvg037/comment/i3evns1/?context=3), we figured out that **all puzzles in the “Evil” category were essentially the same puzzle**, just with the rows, columns and digits shuffled a bit to make it less obvious. That explained both how all grid looked so similar and why the “exploit” worked even though it wasn't logic-based. It also meant that the whole category was kind of pointless. Since it contained only one puzzle, knowing the solve path once was enough. One poster even compiled a [full list of required techniques](https://www.reddit.com/r/sudoku/comments/u0zig9/the_solve_path_to_every_sudokucomevil_puzzle/) for all the incoming requests on the subreddit.

### Sudoku.com's Reaction

Around November of 2022 the “Evil” category was changed. **The app now inserts a random additional given digit to the previously very hard but repetitive puzzles.** This lowers the resulting puzzle's difficulty by a random amount. Sometimes it's still decently hard, but very often it becomes trivially easy. A large majority of the puzzles are easier than the “Hard” category.

## Conclusion

The “Evil” category was very hard but repetitive at first, but was then it was changed to become mostly extremely easy. It is not harder than “Expert”. **Solving these puzzles for time makes no sense because their difficulties are all over the place.**

The Sudoku.com app is mostly aimed at casual Sudoku solvers, not enthusiasts. The hint system and the difficulty levels show that. The treatment of the “Evil” category is especially disappointing however.

### The Original Puzzle

Here is one example of the original “Evil” puzzle, as you could find them before the change:

 * Puzzle string:  
   `950003800001050000007000009240070008000600300009000000580040002010000000000007040`
 * Playable link on SudokuExchange.com:  
   https://sudokuexchange.com/play/?s=950003800001050000007000009240070008000600300009000000580040002010000000000007040
