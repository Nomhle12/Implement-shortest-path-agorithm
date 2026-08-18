# Implement-shortest-path-agorithm
A Python implementation of Dijkstra's shortest-path algorithm using an adjacency matrix.  This project finds the shortest distance and corresponding path between nodes in a weighted graph. 

# Dijkstra Shortest Path in Python

A Python implementation of Dijkstra's shortest-path algorithm using an adjacency matrix.

This project finds the shortest distance and corresponding path between nodes in a weighted graph.

## Project Overview

Dijkstra's algorithm is a graph traversal algorithm used to find the shortest path between a starting node and other nodes in a weighted graph.

This implementation:

* Uses an adjacency matrix to represent the graph
* Calculates the shortest distance from a starting node
* Tracks the path taken to reach each node
* Allows a specific target node to be selected
* Can also calculate paths to all reachable nodes
* Uses `float('inf')` to represent the absence of a direct edge

## Graph Representation

The graph is represented using the following adjacency matrix:

INF = float('inf')

adj_matrix = [
    [0, 5, 3, INF, 11, INF],
    [5, 0, 1, INF, INF, 2],
    [3, 1, 0, 1, 5, INF],
    [INF, INF, 1, 0, 9, 3],
    [11, INF, 5, 9, 0, INF],
    [INF, 2, INF, 3, INF, 0],
]

Each row and column represents a node.

A numerical value represents the weight of an edge between two nodes, while INF indicates that there is no direct connection.

## Algorithm

The implementation follows the main steps of Dijkstra's algorithm:

1. Set the starting node's distance to `0`.
2. Set all other node distances to infinity.
3. Keep track of visited nodes.
4. Select the unvisited node with the smallest known distance.
5. Examine its neighboring nodes.
6. Calculate whether travelling through the current node produces a shorter path.
7. Update the distance and path when a shorter route is found.
8. Repeat until all reachable nodes have been processed.

## Example

The function can be called with:
shortest_path(adj_matrix, 0, 5)

This searches for the shortest path from node 0 to node 5.

### Output

0-5 distance: 6
Path: 0 -> 2 -> 1 -> 5

The shortest distance from node 0 to node 5 is 6.

The algorithm finds the route:

0 → 2 → 1 → 5

with a total weight of:

0 → 2 = 3
2 → 1 = 1
1 → 5 = 2

Total = 6


Function
shortest_path(matrix, start_node, target_node=None)

Return Value

distances, paths
distances contains the shortest known distance from the starting node to every node.
paths contains the corresponding paths.

## Concepts Demonstrated

* Graphs
* Weighted graphs
* Adjacency matrices
* Dijkstra's algorithm
* Shortest-path algorithms
* Lists and nested lists
* Loops
* Conditional statements
* Generators
* Function parameters and default values
* Path reconstruction
* Python's `float('inf')`

## Possible improvements include:

* Accepting graphs from user input
* Adding a visual representation of the graph
* Supporting larger graphs
* Adding automated tests
* Validating the adjacency matrix
* Creating a command-line interface
* Comparing Dijkstra's algorithm with other shortest-path algorithms


This project was created as part of my continued study of Python, algorithms, and graph data structures.
