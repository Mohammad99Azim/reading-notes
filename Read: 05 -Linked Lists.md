# Linked Lists

A linked list is a sequence of data elements, which are connected together via links
Each data element contains a connection to another data element in form of a pointer
Python does not have linked lists in its standard library.

Creation of Linked list

A linked list is created by using the node class also you can add and delete node from the linked list


#### Why we Will Need the Linked List

1) Queues : For a queue, you use a First-In/First-Out (FIFO) approach That means that the first element inserted in the list is the first one to be retrieved

2) Stacks : For a stack, you use a Last-In/Fist-Out (LIFO) approach, meaning that the last element inserted in the list is the first to be retrieved

3) Graphs : Graphs can be used to show relationships between objects or to represent different types of networks.

#### Methods You will need it in the Linked list

- insert(): Add an item to the linked list at the head of the list
- find(): Find an item within the linked list
- remove(): Remove a given item with a given value
- is_empty(): Returns whether the linked list is empty or not
- get_count(): Returns the number of items in the linked list


# Big(O)

mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity.

![imageee](https://cdn-media-1.freecodecamp.org/images/1*KfZYFUT2OKfjekJlCeYvuQ.jpeg)

- constant-time function/method is “order 1” : O(1)
- linear-time function/method is “order N” : O(N)
- quadratic-time function/method is “order N squared” : O(N 2 )  etc...


##### some examples of function and there complexty

- Logarithmic algorithm – O(logn) – Binary Search. 
- Linear algorithm – O(n) – Linear Search. 
- Superlinear algorithm – O(nlogn) – Heap Sort, Merge Sort. 

Space-Time Tradeoff and Efficiency

There is usually a trade-off between optimal memory use and runtime performance. 
In general for an algorithm, space efficiency and time efficiency reach at two opposite ends and each point in between them has a certain time and space efficiency. So, the more time efficiency you have, the less space efficiency you have and vice versa






