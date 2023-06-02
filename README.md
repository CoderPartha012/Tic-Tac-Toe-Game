# Tic Tac Toe Game

This is a simple command-line Tic Tac Toe game implemented in Python. The game allows two players to take turns marking spaces on a 3x3 grid with their respective symbols (X or O). The player who succeeds in placing three of their marks in a horizontal, vertical, or diagonal row wins the game.

## Table of Contents

- [Getting Started](#getting-started)
- [Code Explanation](#code-explanation)

## Getting Started

To play the game, follow these steps:

1. Run the program and enter the required information.
2. Player 1 will be prompted to choose their symbol, either "X" or "O". Player 2 will automatically be assigned the remaining symbol.
3. The game will display an empty 3x3 grid.
4. Players will take turns entering their desired row and column numbers to place their symbols on the grid.
5. The game will check for a winner after each move.
6. If a winner is found or the board is full with no winner, the game will end.

## Code Explanation

### `intro()`

This function introduces the rules of the game and provides an overview of how to play.

### `create_grid()`

This function creates a blank 3x3 playboard.

### `sym()`

This function allows Player 1 to choose their symbol ("X" or "O"). Player 2 is assigned the remaining symbol.

### `startGamming(board, symbol_1, symbol_2, count)`

This function starts the game by prompting the current player to choose a row and column to place their symbol. It checks for valid input and whether the selected square is already filled.

### `isFull(board, symbol_1, symbol_2)`

This function checks if the game board is full. It calls the `startGamming()` function and the `printPretty()` function to display the updated board after each move. It also checks for a winner by calling the `isWinner()` function.

### `outOfBoard(row, column)`

This function informs the players that their selection is out of range.

### `printPretty(board)`

This function prints the game board in a visually appealing format.

### `isWinner(board, symbol_1, symbol_2, count)`

This function checks if any player has won the game by checking the rows, columns, and diagonals of the board.

### `illegal(board, symbol_1, symbol_2, row, column)`

This function informs the players that the selected square is already filled.

### `report(count, winner, symbol_1, symbol_2)`

This function displays a summary of the game, including the winner or a tie message.

## Usage

To play the Tic Tac Toe game, execute the `main()` function.

```python
def main():
    # The main function
    introduction = intro()
    board = create_grid()
    pretty = printPretty(board)
    symbol_1, symbol_2 = sym()
    full = isFull(board, symbol_1, symbol_2)
