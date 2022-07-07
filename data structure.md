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
