# Project “Labyrinth”: Solution using Q-Learning

This project demonstrates the implementation of the Q-learning algorithm (reinforcement learning) to find the optimal path in a 7x7 grid maze.

## Project Description

In Jupyter Notebook `Q-Learning-labyrinth.ipynb`, an agent is implemented that learns to navigate the maze, avoiding “walls” (cells with a large negative penalty) and striving for the “goal” (a cell with a high reward).

### How it works

1.  **Environment:**
* The maze is a 7x7 grid (49 states).
* The environment is defined by the list `M`, where:
* `-1000`: Wall (large penalty).
        * `-1`: Normal step (small penalty to motivate the agent to find a short path).
* `1000`: Goal (high reward).
* The function `Action(n, i)` defines possible actions (up, down, left, right) and checks the boundaries of the maze.

2.  **Algorithm (Q-Learning):**
* The agent uses a Q-table (called `P` in the code) of size `49x4` to store the “value” of each action in each state.
    * It follows an **ε-greedy strategy** to balance exploration and exploitation of known paths.
* Q-values are updated using the iterative Q-learning formula.

3.  **Hyperparameters:**
    * **`alpha` (learning rate):** 0.1
    * **`gamma` (discount factor):** 0.9
    * **`eps` (epsilon):** 0.1

### Visualization

The notebook contains two visualizations built using `matplotlib`:
1.  **Maze heatmap:** Shows the initial reward structure (walls, passages, goal).
2.  **Path heatmap:** Shows the path (`W`) that the agent has traveled over 200 iterations of its training/movement, superimposed on the maze map.

---
*This project is a tutorial example of Q-learning implementation.*
