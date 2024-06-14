# Shortest-Path-Finder-Breadth-First-Search-Algorithm-

# Maze Solver 

## Overview

🔍 This project is a simple maze solver using the Breadth-First Search (BFS) algorithm implemented in Python with the `curses` library for visual representation. The program finds the shortest path from the start position (`O`) to the end position (`X`) in a given maze.

## Features

- **🔄 Breadth-First Search (BFS) Algorithm**: Ensures the shortest path is found.
- **📺 `curses` Library**: Provides a visual representation of the maze and the path-finding process.
- **🎨 Color-Coded Visualization**: Uses different colors for the maze and the path.

## Prerequisites

- 🐍 Python 3.x
- 📦 `curses` library (usually pre-installed with Python on Unix-based systems)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/avishkaJSPshehan/Shortest-Path-Finder-Breadth-First-Search-Algorithm-.git
   cd maze-solver
   ```

## Usage

1. Run the `main.py` script:
   ```bash
   python main.py
   ```

2. The program will display the maze and visually find the shortest path from `O` to `X`.

## Code Explanation

### `main.py`

This is the main script containing the logic for the maze solver.

#### Maze Representation

The maze is represented as a 2D list where:
- `#` represents walls.
- ` ` represents open paths.
- `O` represents the starting position.
- `X` represents the ending position.

```python
maze = [
    ["#", "O", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#"],
    ["#", " ", " ", "#", " ", " ", " ", "#", " ", "#", " ", " ", "#", " ", "#", " ", " ", " ", " ", "#"],
    ["#", "#", " ", "#", " ", "#", "#", "#", " ", "#", "#", " ", "#", " ", "#", " ", "#", "#", " ", "#"],
    ["#", "#", " ", " ", " ", "#", " ", " ", " ", " ", "#", " ", " ", " ", "#", " ", " ", "#", " ", "#"],
    ["#", " ", "#", "#", " ", "#", " ", "#", "#", "#", "#", "#", "#", " ", "#", "#", " ", "#", " ", "#"],
    ["#", " ", "#", " ", " ", " ", " ", "#", " ", " ", "#", " ", "#", " ", " ", "#", " ", " ", " ", "#"],
    ["#", " ", "#", "#", "#", "#", " ", "#", " ", "#", "#", "#", "#", "#", " ", "#", "#", "#", "#", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", "#"],
    ["#", "#", "#", "#", "#", " ", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", " ", "#"],
    ["#", " ", " ", " ", " ", " ", "#", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", "#", " ", "#"],
    ["#", " ", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", " ", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", "#", " ", "#"],
    ["#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", " ", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", "#", " ", "#"],
    ["#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", " ", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", "#", " ", "#"],
    ["#", " ", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", " ", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", "#", " ", "#"],
    ["#", " ", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", " ", " ", " ", " ", " ", " ", " ", "#"],
    ["#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "#", "X", "#", "#", "#", "#", "#", "#", "#"]
]
```

#### Functions

- **`print_maze(maze, stdscr, path=[])`**: Prints the maze to the `stdscr` screen, highlighting the path.
- **`find_start(maze, start)`**: Finds the starting position `O` in the maze.
- **`find_path(maze, stdscr)`**: Uses BFS to find the shortest path from `O` to `X`, updating the `stdscr` screen to visualize the process.
- **`find_neighbors(maze, row, col)`**: Returns the valid neighbors of a cell (up, down, left, right).

#### Main Function

- **`main(stdscr)`**: Initializes color pairs, finds the path using BFS, and waits for a key press to exit.

```python
def main(stdscr):
    curses.init_pair(1, curses.COLOR_BLUE, curses.COLOR_BLACK)
    curses.init_pair(2, curses.COLOR_YELLOW, curses.COLOR_BLACK)

    find_path(maze, stdscr)
    stdscr.getch()

wrapper(main)
```

## Visualization

The program uses color pairs to differentiate between the maze structure and the path:
- **🔵 Blue**: Walls and open paths.
- **🟡 Yellow**: The path from `O` to `X`.


## Acknowledgements

- 📚 `curses` library for terminal handling.
- 🔍 BFS algorithm for pathfinding.

## Contributing

🤝 Feel free to fork the repository and submit pull requests. Contributions are welcome!

---
