# Graphs

### What is a Graphs

A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

### Undirected Graphs

An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

### Directed Graphs (Digraph)

A Directed Graph also called a Digraph is a graph where every edge is directed.

Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

### Complete vs Connected vs Disconnected

- Complete Graphs : A complete graph is when all nodes are connected to all other nodes.
- Connected: A connected graph is graph that has all of vertices/nodes have at least one edge.
- Disconnected: A disconnected graph is a graph where some vertices may not have edges

### Acyclic vs Cyclic

- Acyclic Graph: An acyclic graph is a directed graph without cycles.
A cycle is when a node can be traversed through and potentially end up back at itself.
- Cyclic Graphs: A Cyclic graph is a graph that has cycles.
A cycle is defined as a path of a positive length that starts and ends at the same vertex.

### Weighted Graphs

A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights. 

## Traversals

### Breadth First

In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. The breadth first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. Traversing a graph that has cycles will result in an infinite loop….this is bad. To prevent such behavior, we need to have some way to keep track of whether a vertex has been “visited” before. Upon each visit, we’ll add the previously-unvisited vertex to a visited set, so we know not to visit it again as traversal continues.

1. Enqueue the declared start node into the Queue.
2. Create a loop that will run while the node still has nodes present.
3. Dequeue the first node from the queue
4. if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.

### Depth First

In a depth first traversal, our approach is a bit different than the approach used for breadth first. While the breadth first traversal uses a Queue to visit all children at a given level, the depth first traversal uses a Stack to visit all children of a given subtree. (This differs from our approach to tree traversal, where we visit nodes via recursive calls. Recursive calls use a call stack internally.)

The algorithm for a depth first traversal is as follows:

1. Push the root node into the Stack and mark as visited.
2. Start a while loop that runs as long as the stack is not empty.
3. Pop the top node off of the stack and check its neighbors.
4. If a neighbor hasn’t been visited, push it onto the stack and mark as visited.
5. Repeat until the stack is empty.

### Real World Uses of Graphs

GPS and Mapping
Driving Directions
Social Networks
Airline Traffic
Netflix uses graphs for suggestions of products