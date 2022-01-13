# Graph Theory
## 1. What is Graph?
Graph is a triplet consisiting vertex set V(G), an edge set E(G), and the relation that associates with each edge and two vertices (**not necessarily distinct**).

![](/Images/simple_graph.png)

### - Order of Graph
Number of vertices is the order of given graph.

### - Size of Graph
Number of edges is the size of given graph.

### - Loops
  Edges having same end points.

### - Multi Edges
  Two or more edges having same end points.

## 2. Types of Graphs with Respect to Loops and Multi Edges

### - Pseudo Graph(s)
  Graphs having both loops and multi edges.

### - Multi Graphs
  Graphs having multi-edges but not loops.

### - Simple Graph(s)
  Graph having neither loops nor multi-edge(s).

## 3. Various representation of Graphs
### - Linked list
![](/Images/linked_list_graph.png)
### - Adjacency matrix
![](/Images/adjacency_matrix.png)

## Degree of Vertex
- Total number of edges incident to any vertex is its degree.
- In case of adjacency matrix representation, sum of values in row gives degree of vertex.

> If degree of all the vertices in the graph is equal then graph is termed as **REGULAR GRAPH**.

## Hand-Shaking Lemma
   In any graph G(V, E) the sum of degree of vertices is twice the number of edges.
   
![](/Images/degree_sum_formula.png)

``` - Number of odd degree vertices are even.```

## Complete Graph
- Two vertices are said to be adjacent if they are connected through atleast one edge.
- Now, if in a given **Simple graph** every pair of vertices is adjacent then graph is termed as **COMPLETE GRAPH**.

> The complete graph on ***n*** vertices is denoted by K*n*.

![](/Images/complete_graph.png)


  
  


