# Solve sudoku using graph coloring algorithms
This software can solve Sudoku using graph coloring techniques, heuristic and algorithm.

## What does that mean

Graph is a math structure represented as G = (V, X), where V is a set of objects called vertices which are linked to each other and stored at X as a family of sets or n-uples.

[Graph coloring](https://en.wikipedia.org/wiki/Graph_coloring) is a branch in graph theory that studies ways of coloring a graph in a way that no adjacent vertices have the same colors.

Sudoku can be represented as a graph where each square is linked to all other squares in the row, column, and 3x3 grid. Coloring it means no other adjacent will have the same number, hence the graph that represents Sudoku is a 9-coloring graph.

## How does it work

There are two algorithms in the file which are RESOLUCAO and RESOLUCAO2, both work using backtracking, which means it goes backwards if the algorithm fails for some vertex (there are no colors possible), then it goes back to the previous vertex and tries the next possible color for that previous vertex. 


The difference relies on the heuristic of each algorithm:

* RESOLUCAO2 uses iteration to go forth and back, and a static list of priority L, defined before the begining of the algorithm. The list L is a decreasing list based on the number of already colored adjacents (the more squares already numbered, the easier it is to selected a possible number).
* While on the RESOLUCAO, it uses recursion and stack to solve it, and at each iteration it chooses the vertex with the least number of possibilities.

Full algorithms can be found in the file, implemented in Python.

## It works fast!

<img alt="Preview gif" src="https://github.com/MasterTuto/sudoku_coloring/raw/main/2021-01-25-09-23-45.gif" height="500px">
