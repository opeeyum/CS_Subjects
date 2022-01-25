# Graph Theory
## 1. What is Graph?
Graph is a triplet consisiting vertex set V(G), an edge set E(G), and the relation that associates with each edge and two vertices (**not necessarily distinct**).

![](/Images/simple_graph.png)

### - Order of Graph
Number of vertices is the order of given graph.

### - Size of Graph
Number of edges is the size of given graph.

### - Loops
  Edges having same starting and end points.

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

## 4. Degree of Vertex
- Total number of edges incident to any vertex is its degree.
- In case of adjacency matrix representation, sum of values in row gives degree of vertex.

> If degree of all the vertices in the graph is equal then graph is termed as **REGULAR GRAPH**.

## 5. Hand-Shaking Lemma
   In any graph G(V, E) the sum of degree of vertices is twice the number of edges.
   
![](/Images/degree_sum_formula.png)

``` - Number of odd degree vertices are even.```

## 6. Havel Hakimi theorem
1. **Degree Sequence** - The degree sequence of an undirected graph is the non-increasing sequence of its vertex degrees.
2. Havel Hakimi theorem checks whether for given degree-sequence, any **SIMPLE GRAPH** exists or not.
- Algorithm:
  - Sort the degree-sequence in non-increasing order.
  - Delete the first element(say V). Subtract 1 from the next V elements.
  - Repeat 1 and 2 until one of the stopping conditions is met.
- Stopping conditions: 
  - All the remaining degree(s) are equal to 0 **Simple graph exists**.
  - Negative number encounter after subtraction **No simple graph exists**.

## 7. Complete Graph
- Two vertices are said to be adjacent if they are connected through atleast one edge.
- Now, if in a given **Simple graph** every pair of vertices is adjacent then graph is termed as **COMPLETE GRAPH**.

> The complete graph on ***n*** vertices is denoted by K*n*.

![](/Images/complete_graph.png)

## 8. Difference between Walk, Trail, Path, Circuit and Cycle
1. Walk - Traversal of graph such that repetition of Edge and Vertex both is allowed.
  - If Walk starts and ends in same vertex then that walk is termed as **Closed Walk**.
2. Trail - Traversal of graph such that repetition of **edge(s)** is(are) not allowed.
```
Closed Trail is termed as Circuit.
```

3. Path - Traversal of graph such that repetition of **vertex(vertices)** is(are) not allowed.
```
Closed Path is termed as Cycle.
```
## 9. Types of Simple Graph
1. Null Graph(N*n*): A graph with *n* vertices and zero edges is Null Graph.
2. Cyclic Graph(C*n*, n>=3):  The cycle graph is a simple graph with 'n' vertices {V1, V2, ..., Vn} and edges {V1, V2}, {V2, V3}, ..., {Vn, V1}.
```
A Cyclic graph will always be Regular.
A Cyclic graph with Even number of Vertices will always be Bipartite.
```
3. Bipartite Graph = A Graph G = (V, E) is bipartite if the Vertex set can be partitioned into sets V1 and V2 such that every edge is between a vertex of V1 and V2.
  - Degree of Bipartite graph == **max(m, n)**, where **m** and **n** are number of vertices in V1 and V2.
  - Maximum edges possible = ![](/Images/max_edge_in_bg.png)
4. Complete Bipartite Graph(K*m*, n) = A Bipartite graph in which every vertex in V1 is adjacent to every vertex in V2 set.

  
  


