A graph is a data structure made up of nodes (which we have seen in form of TreeNodes and ListNodes) and possibly pointers connecting them together. In graphs, nodes are referred to as **vertices** and the pointers connecting these nodes are referred to as **edges**. There are no restrictions in graphs when it comes to where the nodes are placed, and how the edges connect those nodes together. It is also possible that the nodes are not connected by any edges and this would still be considered a graph - a null graph.
The number of edges, 𝐸, given the number of vertices 𝑉 will always be less than or equal to $V^2.$
$i.e. E <= V^2$ . This is because each node can at most point to itself, and every other node in the graph.

A graph can be represented in different ways. It is an abstract concept that is made concrete using different data structures. Most commonly, graphs are represented using the following:
1. Matrix
2. Adjacency Matrix (Least Common)
3. Adjacency List (Most Common)

**Matrix**
Let's say that all of the 0's in our grid are vertices. To traverse a graph, we are allowed to move up, down, left and right. If we are to connect the 0s together, using our edges, we would end up getting a bunch of connected zeroes, which are connected components, and that denotes a graph

**Adjacency Matrix**
This is the less common input format. Here, the index of the array represents a vertex itself. Because the indices themselves represent a vertex, 00 denotes that an edge does not exist between a given `v1, v2`, and 11 denotes the opposite. `adjMatrix[1][2] == 0` means there is no edge between vertex `1` and `2`. Also, `adjMatrix[2][1] == 0` means there is no edge between vertex `2` and `1`.
The issue with this is that if our graph has few edges it is not a good use of memory. Because it is a square matrix, the space complexity is $𝑂(𝑉^2)$, where 𝑉 is the number of vertices.

**Adjacency List**
These are typically the most common way of representing graphs. This is also a two dimensional array. The convenience here is that we can declare it using a class called `GraphNode` and it contains a list attribute called `neighbors`, using which we can access all of a given vertex's neighbor. This ends up being more space efficient because we only care about nodes that are connected.

```kotlin
Class GraphNode() {
	var `val`: Any?
	var neighbors: ArrayList<GraphNode>
}
```
