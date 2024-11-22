# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

When solving Sudoku puzzles, DFS and BFS are different in performance and efficiency. DFS explores one path deepl and backtracks when it hits a dead-end. This is good for using less memory but potentially wastes time on dead-ends. BFS, on the other hand, explores all possibilities level by level, guaranteeing the shortest solution but requiring much more memory to store all possible states. It's often more efficient to use DFS for Sudoku becaise of its lower memory usage and backtracking features. BFS might be more useful in simpler puzzles where memory isn't as important and exploring all possibilities is needed.

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

The choice of data structures—Stack for DFS and Queue for BFS— impacts the functionality of the algorithms immensely. "Stack" enables DFS to explore the most recent state first which allows for fast backtracking. Queue ensures BFS explores all possibilities level by level, providing the shortest solution. Other data structures like priority queues or deques, are used to prioritize certain paths or allow more flexible exploration. However they add more complexity without significant benefit which doesn't benefit the sudoku process.

3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

To adapt to larger puzzles or different grid-based games, adjustments would be needed to handle different grid sizes and unique constraints. For example, extending to larger grids (like 16x16 or 25x25) would require changes to the board size and constraint calculations, and ensuring DFS and BFS remain efficient. The key features like constraint propagation, backtracking, and heuristic-based search (finding the most-constrained cell) can be applied across games like nonagrams. This is valuable in real-world problem-solving, especially in fields like operations research and AI, where searching through spaces and balancing search strategies is essential for tasks such as scheduling and resource allocation.