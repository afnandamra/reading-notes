# Linked Lists

## Linked Lists: From Code Fellows [overview docs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

- Linked list: data structure that contains nodes that links/points to the next node in the list
- Most defining feature of a linked list is that each Node references the next Node in the link
- There are two types of linked lists - singly and doubly
  - singly: there is onlly one reference, and the reference points to the next node in a linked list
  - doubly: there is a reference to both next and previous node
- Node: individual items/links that live in a linked list, each node contains data for each link
- Next: each node contains property called next, property contains the reference to the next node
- Head: reference type of type Node to the first node in a linked list
- Current: reference type of type Node that is currently being looked at

## What is a Linked List (Part 1)

- Data structures: different ways that we can organize our data
- Types of data structures: variables, arrays, hashes, and objects
- Linked lists are linear data structures, which means there is a sequence and an order to how they are constructed and traversed
- Non linear data structures: hashes, trees, graphs
- Like arrays, in linked lists order matters
- Linked lists don't need to take up a single block of memory, instead, the memory that they use can be scattered (unlike arrays for example, which take up a block of memory all in one place)
- Arrays are static data structures, while linked lists are dynamic data structures
- Static data structure: needs all resources to be allocated when the structure is created, will always need a given size of memory even if it's to grow/shrink in size
- Dyamic data structure: can shrink and grow in memory
- Linked list is made up of series of nodes, starting point is the first node which is refered to as the head
- Head is effectively the only entry point to the list and all of its elements
- End of the list isn't a node, but rather a node that point to null or an empty value
- Single node has two parts: data (information the node contains) and a reference to the next node
- A node only knows about what data it contains and who its neighbor is
- This is why a linked list doesn't need a continuous block of memory, a single node has the "address" or a reference to the next node
- Singly linked lists are the simplest type of list, based sonly on fact they go only in one direction
- Doubly linked list: when node can have reference to the subsequent neighbor node and the preceeding node too
- Circular linkeded list: has a node that acts as the tail of the list, and the node after the tail node is the beginning of the list

## What is a Linked List (Part 2)

- Big O notation: way of evaluating the performance of an algorithm
- There are two major points to consider when thinking about how an algorithm performs: how much time it requires at runtime given how much time and memory it needs
- Linked lists Big O equations O(1) and O(n)
- An O(1) function takes constant time
- An O(n) function is linear
- A linked list is usuallly efficient when it comes to adding and removing most elements, but it can be very slow to search and find a single element