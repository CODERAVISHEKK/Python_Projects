# Tower of Hanoi

A command-line implementation of the **Tower of Hanoi** puzzle written in Python. The player moves disks between three stacks—Left, Middle, and Right—until all disks have been transferred to the Right stack while following the puzzle's rules.

## Features

- Text-based, interactive gameplay.
- Three towers represented using custom stack data structures.
- Stacks are implemented with linked nodes.
- Prompts the player to choose a source tower and a destination tower.
- Prevents placing a larger disk on top of a smaller disk.
- Displays the current contents of all three stacks after each turn.
- Calculates and displays the theoretical minimum number of moves.

## Requirements

- Python 3
- No external libraries are required.

## How to Run

1. Save or download `Towers of Hanoi.py`.
2. Open a terminal or command prompt in the folder containing the file.
3. Run:

   ```bash
   python "Towers of Hanoi.py"
   ```

   On some systems, you may need to use `python3` instead:

   ```bash
   python3 "Towers of Hanoi.py"
   ```

4. Enter the number of disks when prompted. The program requires **at least 3 disks**.

## How to Play

The game has three towers:

- **Left (L)** — the starting tower; all disks are placed here initially.
- **Middle (M)** — the auxiliary tower.
- **Right (R)** — the destination tower.

On each turn:

1. Choose the tower to move a disk **from** by entering `L`, `M`, or `R`.
2. Choose the tower to move the disk **to**.
3. Only the top disk of a tower can be moved.
4. A larger disk cannot be placed on top of a smaller disk.
5. Continue until every disk is on the Right tower.

The program prints the state of the towers and reports the number of moves used when the puzzle is completed.

## Minimum Number of Moves

For `n` disks, the minimum number of moves required to solve the Tower of Hanoi puzzle is:

\[
2^n - 1
\]

The program calculates this value at the beginning and displays it for comparison with the player's move count.

For example, with 3 disks:

\[
2^3 - 1 = 7
\]

## Code Structure

| Class / Function | Purpose |
|---|---|
| `Node` | Stores a disk value and a reference to the next node. |
| `Stack` | Implements a stack using linked nodes and provides operations such as `push`, `pop`, `peek`, and `is_empty`. |
| `get_input()` | Displays the tower choices and returns the selected stack. |
| Main game loop | Sets up the towers, accepts moves, checks move validity, displays the stacks, and detects completion. |

## Notes

- Tower selection uses the uppercase initials `L`, `M`, and `R`.
- The code sets a maximum capacity of 1,000 disks per stack.
- The program is an interactive manual puzzle; it does not automatically calculate or perform the solution.
