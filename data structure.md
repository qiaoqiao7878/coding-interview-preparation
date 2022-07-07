# Data structure

Some notes about common data structure.

## Binary tree

1. Pre-order traversal

root -> traverse left -> traverse right

2. In-order Traversal

traverse left -> root -> traverse right

3. Post-order Traversal

traverse left -> traverse right -> root

## Graph

### Graph representation

<pre>
0 --- 1
    / |
  /   |
3 --- 2
</pre>

1. Edge list 
  [[0,1], [1,2] \
  [1,3], [2,3]]
3. Adjacency list
  [[1], [0,2,3], [1,3], [1,2]]
5. Adjacency Matrix
  [[0,1,0,0] \
  [1,0,1,1] \
  [0,1,0,1] \
  [0,1,1,0]]
  
  
Hamiltonian Path
  
Eulerian Path:
  
Eulerian Cycle:
Travel every edge only once and return to the same starting point
  
  
### Shortest Path Problem

In an unweighted undirected graph, this is just a breath first search problem.

### Dijkstra's Algorithm
weighted graph
greedy algorithm: always take the best at the moment
min priority queue

## Knapsack problem
a knapsack has a weight constraint, a few items with weight and value, how to get the highest value?

0-1 knapsack problem: you only have one of each objects

brute force solution is O(2^n)

A faster algorithm:

use a table to store the precomputed maximum values
O(nW): n is number of elements, W is the weight limit

Dynamic Programming:

Can I break this problem into subproblems?


## Traveling Salesman problem - NP hard problem
A graph, nodes are cities, edges are distances between cities. What is the faster way for a salesman to travel every city exactly one and go home.

NP hard: not able to solve in polynomial time

exact algorithms\
Approximation algorithms



