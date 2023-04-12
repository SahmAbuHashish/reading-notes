# linked lists

## What’s a Linked List?

A linked list is a linear data structure used for storing collections of elements. It consists of a sequence of nodes, where each node contains both a data element and a reference to the next node in the sequence.

### Linear data structures

One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed, we have to go through all of the items in the list in order, or sequentially. Linear structures, however, are the opposite of non-linear structures. In non-linear data structures, items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.

### Memory management

The biggest differentiator between arrays and linked lists is the way that they use memory in our machines.

The fundamental difference between arrays and linked lists is that arrays are static data structures, while linked lists are dynamic data structures. A static data structure needs all of its resources to be allocated when the structure is created; this means that even if the structure was to grow or shrink in size and elements were to be added or removed, it still always needs a given size and amount of memory. If more elements needed to be added to a static data structure and it didn’t have enough memory, you’d need to copy the data of that array, for example, and recreate it with more memory, so that you could add elements to it.
On the other hand, a dynamic data structure can shrink and grow in memory. It doesn’t need a set amount of memory to be allocated in order to exist, and its size and shape can change, and the amount of memory it needs can change as well.


### Parts of a linked list

The starting point of the list is a reference to the first node, which is referred to as the head. Nearly all linked lists must have a head, because this is effectively the only entry point to the list and all of its elements, and without it, you wouldn’t know where to start! The end of the list isn’t a node, but rather a node that points to null, or an empty value.


- Singly linked lists are the simplest type of linked list, based solely on the fact that they only go in one direction. There is a single track that we can traverse the list in; we start at the head node, and traverse from the root until the last node, which will end at an empty null value.

- doubly linked list, two references contained within each node: a reference to the next node, as well as the previous node. This can be helpful if we wanted to be able to traverse our data structure not just in a single track or direction, but also backwards

- A circular linked list is a little odd in that it doesn’t end with a node pointing to a null value. Instead, it has a node that acts as the tail of the list (rather than the conventional head node), and the node after the tail node is the beginning of the list. 


### Big O: Analysis of Algorithm Efficiency

Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

- Running Time :The amount of time a function needs to complete.

- Memory Space :The amount of memory resources a function uses to store data and instructions.

- *Constant Complexity*  means that no matter what inputs are thrown at our algorithm, it always uses the same amount of time or space --> as an O(1) constant efficiency

- *Logarithmic Complexity* represents a function that sees a decrease in the rate of complexity growth, the greater our value of n. --> O(lgn) complexity growth.

- *Linear Complexity* the size of our inputs ‘n’ will directly determine the amount of Memory Space used and Running Time length --> O(n) complexity growth.

- *Linearithmic Complexity* Linearithmic functions grow faster than input size n, but not by much. This can be seen in divide and conquer algorithms such as the Merge Sort have linearithmic complexity growth rates. ---> O(lgn)

- *Quadratic Complexity* describes an algorithm with complexity growing at a rate of input size n multiplied by n. ---> O(n^2) complexity.

- *Cubic Complexity* is typically just a higher degree of what makes the quadratic complexity grow at such a high rate. We can illustrate this by nesting more loops within our algorithm. -->O(n^3) complexity

- *Exponential Complexity* represents very rapidly growing complexity, such that whatever our input size n -->  O(2^n)

- Factorial Complexity means that the our space and time requirements grow extremely fast, relative to our input size -->O(n!)

### Asymptotic Notations

 academics use the following notations in the following table to describe the differing complexities of an algorithm.

- Big O(oh): This notation describes the Worst Case for an algorithm. The Order of Growth used represents the upper bounds of Time and Space.
- Big Omega: This notation describes the Best Case for a given algorithm. The Order of Growth used represents the lower bounds of Time and Space.
- Big Theta: This notation describes the Average Case. The Order of Growth used represents the tight bound of Time and Space.

