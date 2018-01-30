
In graph theory, the [shortest path problem](https://en.wikipedia.org/wiki/Shortest_path_problem) is the problem of finding a path between two vertices (or nodes) in a graph such that the sum of the weights of its constituent edges is minimized. There are many possible solutions to the problem, the most famous are:

- **Dijkstra**'s algorithm solves the single-source shortest path problem.
- **Bellman–Ford** algorithm solves the single-source problem if edge weights may be negative.
- **A*** search algorithm solves for single pair shortest path using heuristics to try to speed up the search.
- **Viterbi** algorithm solves the shortest stochastic path problem with an additional probabilistic weight on each node.

In weighted graph the **time complexity** of Dijkstra is *O(V^2)*. In unweighted graph it can be used the breadth-fist search to solve the problem, that has *O(V+E)* time complexity.


Implementation
---------------

Methods
--------


Applications
------------


Quiz
-----


Material
--------
- **Coursera Algorithms Part 2**: week 
- **Algorithms**, Sedgewick and Wayne (2014): Chapter  ""
