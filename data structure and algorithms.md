# Data structure and algorithms

Some notes about common data structures and algorithms.


## Hash table

Collision:
- Linear probing: assigned the next availabe spot on the table -> Problem: clustering
- Separate chaining: hash table is various pointer to a linked list

Good hash function:
- Makes use of all info provided by key
- Uniformaly distributes output across table
- Map similar keys to very different hash values
- Uses only very fast operations

## Tree

- Height is the length of the longest path to a leaf
- Depth is the length of the path to its root

## Binary tree

1. Pre-order traversal

root -> traverse left -> traverse right

2. In-order Traversal

traverse left -> root -> traverse right

3. Post-order Traversal

traverse left -> traverse right -> root

## Binary search tree

## AVL tree
self-balanced tree, the heights of the two child subtrees of any node differ by at most one
lookup, insertion and deletion takes O(log n) time

## Red-black tree
Self-balanced tree, searching operation takes only O(log n) time

## Trie
designed for search and retrieval operations, specifically searching for things that match a prefix string.

## Heap
Min heap, the root has smaller value than its children.
Add element: add element to the end, compare it with parent
Remove element: remove root, Move the last element to the root, compare it with children, swap with the smaller child.

We can use an array to represent a heap
if the parent index is i, its left child is 2i+1, its right child is 2i+2
if the node index is n, its parent index is floor((n-1)/2)

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


## Sorting

Simple sorts

- Insertion sort: relatively efficient for small lists and mostly sorted lists. Taking elements one by one and inserting them in their correction position in a new sorted list. Insertion is expensive.
- Selection sort: Finds the minimum value, swaps it with the value in the first position. and repeat for the rest.

Efficient sorts

- merge sort: it has additional O(n) space complexity
- Timsort: uses in Python
- Heapsort: makes use of heap
- Quicksort: divide and conquer, select a pivot, All elements smaller than the pivot are moved before it and all greater elements are moved after it. And then sort the lesser and greater sublists.

- Bubble sort: Bubble sort can also be used efficiently on a list of any length that is nearly sorted. Bubble the largest element to the end.

## greatest common divisor
Euclidean algorithm

the greatest common divisor of two numbers does not change if the larger number is replaced by its difference with the smaller number.
