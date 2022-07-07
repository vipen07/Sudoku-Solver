# Sudoku Solver

We’ve all played Sudoku. Maybe you enjoy it, or maybe you really don’t, but you feel offended by its incompleteness in the in-flight magazine. Either way, the puzzle must be solved! Sometimes you don’t want to bother, but just copying the solution is not very satisfying. However, it’s not really cheating if you write an app that does the heavy lifting, is it? That’s what we’re setting out to do today—write a Sudoku solver from scratch in JavaScript.

## Algorithm
The most basic way I could think of to write a Sudoku solver is to start at the first empty square, try a number, and check the row, column, and nearest 3x3 square for a match. If there is no match, the number is currently valid, so move to the next square and try a new number. If you try numbers 1-9 and find no valid numbers, go back to the previous square and increment it by one until you either exceed 9 or you find a new possible valid number. Keep following this same plan, sliding forward and backward through the empty squares until you arrive at a solution.

This is a backtracking algorithm. The basic idea being that you incrementally build a solution and discard it once you realize that it’s not viable.

Please have a look at it [here](https://the-sudoku-solver.netlify.app/)
- Get New Puzzle: This will reset the puzzle 
- Solve: This will solve the Sudoku 
