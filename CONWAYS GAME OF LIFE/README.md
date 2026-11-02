# Conway's Game of Life

An interactive **Conway's Game of Life** simulation built with **Python**, **Pygame**, and **NumPy**. Create patterns on a grid and watch cells evolve according to simple rules based on their neighbors.

## Features

- Interactive **800 × 600** window with an **80 × 60** cell grid.
- Click to make cells alive.
- Press **Space** to start or pause the simulation.
- Automatically updates the grid at up to **30 ticks per second**.
- Uses different colors to display living cells and cells marked to die in the next generation.

## Requirements

- Python 3
- `pygame`
- `numpy`

Install the dependencies:

```bash
pip install pygame numpy
```

## How to Run

1. Save the provided Python code as `game_of_life.py`.
2. Open a terminal in the same folder.
3. Run:

   ```bash
   python game_of_life.py
   ```

## Controls

| Control | Action |
| --- | --- |
| Left mouse button | Set the cell under the pointer to alive |
| Spacebar | Start or pause the simulation |
| Close window | Exit the program |

Start by clicking cells to create a pattern, then press **Space** to watch it evolve.

## Rules

Each generation follows the four classic rules of Conway's Game of Life:

1. A living cell with fewer than two live neighbors dies.
2. A living cell with two or three live neighbors survives.
3. A living cell with more than three live neighbors dies.
4. A dead cell with exactly three live neighbors becomes alive.

## Implementation

- `update()` checks each cell's surrounding neighborhood, calculates the next generation, and draws the grid.
- `main()` initializes the Pygame window, creates the NumPy grid, processes mouse and keyboard input, and runs the simulation loop.
- The initial grid contains only dead cells; users create the starting pattern themselves.

## Note

This README describes the supplied implementation. The neighbor calculation uses NumPy slices, so cells at the grid edges do **not** wrap around to the opposite edge. The current program also does not include a reset button or a way to erase individual cells with the mouse.
