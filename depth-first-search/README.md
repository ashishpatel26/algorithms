
The [depth-first search](https://en.wikipedia.org/wiki/Depth-first_search) is an algorithm for **searching** or for traversing a graph. It is possible to understand how the algorithm works using the maze example. Let's suppose that a maze can be represented with nodes (intersection points) and edges (paths between nodes), as follows:

<p align="center">
<img src="./images/dfs_maze_definition.png" width="450">
</p>

The [Trémaux's algorithm](https://en.wikipedia.org/wiki/Maze_solving_algorithm) can be used to find the exit. This algorithm is similar to the one used by Theseus in the Minotaur maze. The rules are three: first unroll a ball of string behind you, second mark each visited intersection and passage, third retrace your steps when no unvisited options are available. The main idea in depth-first search is to mimic the maze exploration. There are two main steps: first mark the current vertex `v` as visited, second *recursively* visit all unmarked vertices adjacent to `v`. The **recursion** is the engine of the algorithm.

The **time complexity** for marking all the vertices connected to `s` in time proportional to the sum of their degrees. The degree is the number of adjacent nodes of a vertex. The time to find a path from `s` to `v` is proportional to its length.


Implementation
---------------

It is good practice to implement a `Graph()` object, that is passed to the algorithm. In this way the graph is decoupled from the algorithms  used on it. After the class `Graph()` is ready (see previous module) it is possible to create a second object called `Path(Graph G, vertex s)` that is used to find paths in the graph once a given starting vertex (represented as integer) is defined. The path class has a method `hasPathTo(vertex v)` returning `True` if there is a route between the starting vertex `s` and the end vertex `v`. 

The graph can be represented with all the methods described in the previous module. Here however we hypothesise that an adjacency-list representation is used. A list of list is defined, for instance in a graph having 5 nodes: `vertex_list[[], [], [], [], []]`. Each sub-list contains the vertex connected to that particular node. For instance with the syntax `vertex_list[2][3]` we are accessing the connection 3 of the vertex 2. The information regarding the fact that a vertex has been visited can be stored in an array of boolean `marked_list[False, False, False, False, False]`. The recursive method marks the given vertex and calls itself for any unmarked vertices on its adjacency list. It is possible to use another list called `edgeto_list[]` to store the incoming connection to any vertex. This list is useful if we want to move back from a given node to the starting node.

```Python
def depth_first_search(v):
    if marked_list[v] == False:
        marked_list[v] = True #mark the node
        print(v) #print marked node
        adjacent_list = vertex_list[v] #get adjacent nodes
        for v_adj in adjacent_list:
            if marked_list[v_adj] == False:
                edgeto_list[v_adj] = v
                depth_first_search(v_adj) #iterative call

```

The following is a representation of the trace of the algorithm on a given graph:

<p align="center">
<img src="./images/dfs_trace.png" width="250">
</p>

The result of calling the algorithm from the vertex 0 of a graph divided in three groups is the following:

<p align="center">
<img src="./images/dfs_result.png" width="550">
</p>

Methods
--------

`depth_first_search(v)`: iterative function to deep search in an adjacent-list of vertices.


Applications
------------

1. financial transactions between partners
2. hyperlink classification of complex networks

Quiz
-----




Material
--------
- **Coursera Algorithms Part 1**: week 4
- **Algorithms**, Sedgewick and Wayne (2014): Chapter 4.1 "Undirected Graph"
