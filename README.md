# Sudoku

This Python script defines a `Board` class to represent a Sudoku puzzle and solve it using a backtracking algorithm. It is designed to solve any standard 9x9 Sudoku puzzle, where the objective is to fill the grid so that each row, column, and 3x3 section contain all digits from 1 to 9, without repetition.

## Features

- **Sudoku Puzzle Representation**: Uses a 2D list to represent the Sudoku board.
- **Pretty Printing**: Overridden `__str__` method for visually appealing representation of the Sudoku board in the terminal.
- **Solver Algorithm**: Implements a backtracking algorithm to solve the puzzle.
- **Validity Checks**: Includes methods to check if a number can be legally placed in a specific position according to Sudoku rules.
- **Finding Empty Cells**: Identifies the next empty cell (represented by `0`) on the board to try possible numbers.

## Usage

To use this script, simply define a 9x9 Sudoku puzzle as a 2D list, where zeros represent empty cells. Then, pass this puzzle to the `solve_sudoku` class method of the `Board` class. The solver will print the initial unsolved puzzle and then the solved puzzle, or indicate if the puzzle is unsolvable.

### Example

```python
puzzle = [
    [0, 0, 2, 0, 0, 8, 0, 0, 0],
    [0, 0, 0, 0, 0, 3, 7, 6, 2],
    [4, 3, 0, 0, 0, 0, 8, 0, 0],
    [0, 5, 0, 0, 3, 0, 0, 9, 0],
    [0, 4, 0, 0, 0, 0, 0, 2, 6],
    [0, 0, 0, 4, 6, 7, 0, 0, 0],
    [0, 8, 6, 7, 0, 4, 0, 0, 0],
    [0, 0, 0, 5, 1, 9, 0, 0, 8],
    [1, 7, 0, 0, 0, 6, 0, 0, 5],
]
Board.solve_sudoku(puzzle)
```

## Implementation Details

- The `Board` class encapsulates all functionality needed to solve the puzzle.
- The `__str__` method provides a detailed string representation of the board, making use of special characters to create a grid-like appearance.
- The `solver` method implements the backtracking algorithm, recursively trying numbers in empty cells and reverting if a number leads to an unsolvable configuration.
- Validity checks (`valid_in_row`, `valid_in_col`, `valid_in_square`) ensure that the board adheres to Sudoku rules at each step of the algorithm.