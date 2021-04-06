# Stacks and Queues

## Stacks and Queues: From Code Fellows [overview docs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

## Stacks

### Terminology

- Stack: data structure that consists of nodes, each node references the next node in the stack but does not reference its previous
- Push: nodes or items that are put into the stack are pushed
- Pop: nodes or items that are removed from the stack are popped, when you attempt to pop an empty stack an exception will be raised
- Top: top of the stack
- Peek: view the value of the top node in the stack, when you attempt to peek an empty stack an exception will be raised
- isEmpty: returns true when stack is empty otherwise returns false

### Concepts

- FILO (first in last out): first item added in the stack will be the last item popped out of the stack
- LIFO (last in first out): last item added to the stack will be the first item popped out of the stack
- Push O(1): pushing a node will always be an O(1) operation because it takes the same amount of time no matter how many nodes you have in the stack
- Pop O(1): popping a node or removing it from the top, top node is reassigned to the the next node
- Peek O(1): only inspecting the top node of the stack
- IsEmpty O(1)


![Stacks and Queues](../Images/stacksqueues.jpg)

## Queues

### Terminology

- Enqueue: nodes or items added to queue
- Dequeue: nodes or items removed from the queue
- Front: front/first node of the queue
- Rear: rear/last node of the queue
- Peek: fiew the value of the first node in the queue
- IsEmpty: returns true when queue is empty otherwise returns false

### Concepts

- FIFO (first in first out): first item in the queue will be the first item out of the queue
- LILO (last in last out): last item in the queue will be the last item out of the queue
- Enqueue O(1)
- Dequeue O(1)
- Peek O(1)
- IsEmpty O(1)