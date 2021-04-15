# Trees

## Trees: From Code Fellows [overview docs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

## Binary Trees, Binary Search Trees, and K-ary Trees

### Terminiology
- Node: component which may contain it’s own values, and references to other nodes
- Root: node at the beginning of the tree
- K: number that specifies the maximum number of children any node may have in a k-ary tree (in a binary tree, k = 2)
- Left: reference to one child node, in a binary tree
- Right: reference to the other child node, in a binary tree
- Edge: link between a parent and child node
- Leaf: node that does not have any children
- Height: number of edges from the root to the furthest leaf

### Traversals
- Allows to search for a node, print out the contents of a tree, and more
- Two categories of traversals of trees:
  - Depth first: prioritize going through the depth (height) of the tree first
    - Three methods for depth first: pre-order (root >> left >> right), in-order (left >> root >> right), and post-order (left >> right >> root)
  - Breadth first: iterates through the tree by going through each level of the tree node-by-node

### Binary Trees versus K-ary Trees
- Trees can have any number of children per node, but Binary Trees restrict the number of children to two
- If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree
- K refers to the maximum number of children that each Node is able to have

#### Adding a Node
- Since there are no structural rules for where nodes go in binary trees, it doesn't matter where a new node gets placed
- One strategy for adding a new node to a binary tree is to fill all "child" spots from the top down
- When you want to place a node in a specific location, you need to reference both the new node to create, and the parent node upon which the child is attached to

#### Big O
- Inserting a new node: O(n) time/ O(w) space where w is the largest width of the tree
- Searching for a specific node: O(n) time
- Perfect binary tree (one where every non-leaf node has exactly two children): maximum width for a perfect binary tree is 2^(h-1), where h is the height of the tree, height can be calculated as log n, where n is the number of nodes

### Binary Search Trees
- Type of tree that does have some structure
- Nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right

#### Searching a BST
- Searching can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree
- If the value is smaller, you only traverse the left side and if the value is larger, you only traverse the right side
- Best way to approach a BST search is with a while loop, cycle through the while loop until we hit a leaf or until you reach a match with what you're searching for

#### Big O
- Insertion and search: O(height) time/ O(1) space
