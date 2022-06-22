# Stacks and Queues

Stack is a container of objects that are inserted and removed according to the last-in first-out (LIFO) principle.

Queue is a container of objects (a linear collection) that are inserted and removed according to the first-in first-out (FIFO) principle.



## Stacks 

A stack is a linear data structure in which elements can be inserted and deleted only from one side of the list, called the top. 
A stack follows the LIFO (Last In First Out) principle,the element inserted at the last is the first element to come out.
The insertion of an element into stack is called push operation, and deletion of an element from the stack is called pop operation.
In stack we always keep track of the last element present in the list with a pointer called top

![Stack_image](https://media.geeksforgeeks.org/wp-content/uploads/geek-stack-1.png)


### push(): 
When we insert an element in a stack then the operation is known as a push. If the stack is full then the overflow condition occurs.
### pop(): 
When we delete an element from the stack, the operation is known as a pop. If the stack is empty means that no element exists in the stack, this state is known as an underflow state.
### isEmpty(): 
It determines whether the stack is empty or not.
peek(): It returns the element at the given position.


## Queues

Queue is the data structure that is similar to the queue in the real world. A queue is a data structure in which whatever comes first will go out first, and it follows the FIFO (First-In-First-Out) policy. Queue can also be defined as the list or collection in which the insertion is done from one end known as the rear end or the tail of the queue, whereas the deletion is done from another end known as the front end or the head of the queue.

The real-world example of a queue is the ticket queue outside a cinema hall, where the person who enters first in the queue gets the ticket first, and the last person enters in the queue gets the ticket at last. Similar approach is followed in the queue in data structure.

![Queue_image](https://static.javatpoint.com/ds/images/ds-types-of-queue.png)


### Enqueue: 
The Enqueue operation is used to insert the element at the rear end of the queue. It returns void.
### Dequeue: 
It performs the deletion from the front-end of the queue. It also returns the element which has been removed from the front-end. It returns an integer value.
### Peek: 
This is the third operation that returns the element, which is pointed by the front pointer in the queue but does not delete it.
### isempty: 
It shows the underflow condition when the Queue is empty, i.e., no elements are in the Queue.



