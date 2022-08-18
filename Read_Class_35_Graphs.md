# Graphs

A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

Here is some common terminology used when working with Graphs:

Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.

Edge - An edge is a connection between two nodes.

Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.

Degree - The degree of a vertex is the number of edges connected to that vertex.


### Traversals

You will be required to traverse through a graph. The traversals itself are like those of trees. Below is a breakdown of how you would traverse a graph.

Breadth First
In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. The breadth first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. Traversing a graph that has cycles will result in an infinite loop….this is bad. To prevent such behavior, we need to have some way to keep track of whether a vertex has been “visited” before. Upon each visit, we’ll add the previously-unvisited vertex to a visited set, so we know not to visit it again as traversal continues.

As a refresher of what breadth first actually means here it is: Breadth first traversal is when you visit all the nodes that are closest to the root as possible. From there you traverse outwards, level by level, until you have visited all the vertices/nodes.

Here is what the algorithm breadth first traversal looks like:

Enqueue the declared start node into the Queue.
Create a loop that will run while the node still has nodes present.
Dequeue the first node from the queue
if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.



#### BreadthFirst

```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    DECLARE visited <-- new Set()

    breadth.Enqueue(vertex)
    visited.Add(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                visited.Add(child)
                breadth.Enqueue(child)

    return nodes;
```


Here is a breakdown of what is going on:

We have declared that our starting node (or root) is going to be Node A.

The first thing we want to do is Enqueue the root.

We also need to add the root to the visited set.

Next, we enter a while loop. We want this loop to keep running until there are no more nodes in our queue.

Once we are in the while loop, we want to Dequeue the front node and then check to see if it has any children.

if there are children of the node we are currently looking at, we want to add them to visited set. This will help us know that we have already seen that node before,

and won’t accidently push us into an infinite loop if the graph was cyclic. In addition to tracking each child node as visited, we want to place any of its children 

that have not yet been visited into the queue.

The process will complete until the queue is empty.

Once the while loop breaks, we can then return the list of nodes. This list will contain, in order, all the nodes that were traversed.

A few things to note about breadth first traversals:

If there are any disconnected nodes (such as islands) with the graph data structure, they will not be traversed.

Breadth first only outputs the nodes that are connected in some relation to the root that you pass in.




#### Depth First


The algorithm for a depth first traversal is as follows:

Push the root node into the Stack and mark as visited.

Start a while loop that runs as long as the stack is not empty.

Pop the top node off of the stack and check its neighbors.

If a neighbor hasn’t been visited, push it onto the stack and mark as visited.

Repeat until the stack is empty.




### Real World Uses of Graphs

Graphs are extremely popular when it comes to it’s uses. Here are just a few examples of graphs in use:

- GPS and Mapping

- Driving Directions

- Social Networks

- Airline Traffic

- Netflix uses graphs for suggestions of products









