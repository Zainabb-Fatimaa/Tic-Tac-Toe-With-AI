# Tic-Tac-Toe with AI Players

## Overview

This project implements a Tic-Tac-Toe game with various AI opponents, including Minimax and Alpha-Beta Pruning algorithms. The game features an interactive graphical interface built with Jupyter widgets, making it playable directly in Jupyter notebooks or Google Colab.

## Features

- **Interactive GUI**: Play Tic-Tac-Toe with a visual board in Jupyter notebooks
- **Multiple Game Modes**:
  - Human vs Minimax AI
  - Human vs Alpha-Beta AI
  - Minimax AI vs Alpha-Beta AI
  - Random AI vs Minimax AI
  - Random AI vs Alpha-Beta AI
- **Advanced AI Players**:
  - **Minimax Algorithm**: Perfect play using recursive tree search
  - **Alpha-Beta Pruning**: Optimized Minimax with pruning
  - **Random Player**: Makes random valid moves
- **First Move Optimization**: AI makes smart first moves for better performance
- **Game Statistics**: Tracks and displays number of states evaluated and computation time

## How to Play

1. **Run the Game**:
   - Execute the `run_visual_game()` function to start the game interface

2. **Select Game Mode**:
   - Choose from the available game modes by clicking the corresponding button

3. **Choose Your Letter (for human vs AI modes)**:
   - Select whether you want to play as X (goes first) or O (goes second)

4. **Start the Game**:
   - Click the "Start Game" button to begin

5. **Make Moves**:
   - For human players: Click on an empty square to place your mark
   - AI players will automatically make their moves

6. **Game Controls**:
   - Use the "Reset Game" button to start a new game
   - Change game modes between matches

## Technical Details

### AI Algorithms

1. **Minimax Player**:
   - Implements the Minimax algorithm for perfect play
   - Evaluates all possible game states recursively
   - Uses depth-first search to find optimal moves

2. **Alpha-Beta Player**:
   - Optimized version of Minimax with Alpha-Beta pruning
   - Cuts off branches that cannot affect the final decision
   - Significantly reduces the number of states evaluated

3. **Random Player**:
   - Makes random valid moves
   - Serves as a baseline opponent

### Implementation Notes

- The game uses Jupyter widgets for the interactive interface
- AI moves are computed in separate threads to maintain UI responsiveness
- The board state is represented as a simple list of 9 elements
- Game logic includes win detection, move validation, and turn management

## Requirements

- Python 3.x
- Jupyter Notebook or Google Colab
- Required packages:
  - `ipywidgets`
  - `numpy`
  - `IPython`

## Performance

The AI players include several optimizations:
- First move optimization (selects from corners and center)
- Move ordering (prioritizes center and corner moves)
- Alpha-Beta pruning (reduces search space)
- State evaluation caching (memoization)

For standard Tic-Tac-Toe, both AI players will always play perfectly, either winning or forcing a draw.

## Future Enhancements

Potential improvements could include:
- Adjustable difficulty levels
- More sophisticated move ordering heuristics
- Additional game statistics and analytics
- Support for larger board sizes (e.g., 4x4, 5x5)
- Network multiplayer functionality

Enjoy playing Tic-Tac-Toe against these AI opponents!
