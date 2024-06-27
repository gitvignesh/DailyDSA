A heap is a specialized, tree-based data structure, which is a complete binary tree. It implements an abstract data type called the Priority Queue, but sometimes 'Heap' and 'Priority Queue' are used interchangeably.

We already learned that queues operate with a first-in-first-out basis but with a priority queue, the values are removed based on a given priority. The element with the highest priority is removed first.

## Two types of heaps

**Min heaps** have the smallest value at the root node and when deleting, the smallest value has the highest priority.

**Max heaps** have the largest value at the root node and when deleting, the largest value has the highest priority.

## Properties

For a binary tree to qualify as a heap, it must satisfy the following properties:

**1. Structure Property**  
A binary heap is a binary tree that is a **complete binary tree**, where every single level of the tree is filled completely, except the lowest level nodes, which are filled contiguously from left to right.

**2. Order Property**
The order property for a min-heap is that all of the descendants should be greater than their ancestor. In other words, if we have a tree rooted at `y`, every node in the right and the left sub-tree should be greater than or equal to `y`. This is a recursive property, similar to binary search trees.

In a max-heap, every node in the right and the left sub-tree is smaller than or equal to `y`

## Implementation

Binary heaps are drawn using a tree data structure but under the hood, they are implemented using arrays. We will take an array of size 𝑛+1 where 𝑛 is the number of nodes in our binary heap.

We will insert these into our array in a contiguous fashion starting from 1, the reason why we start filling up our array from index `1` is because it helps us figure out the index at which a node's left child, right child, or the parent resides. Because binary heaps are complete binary trees, no space is required for pointers. Instead, a node's left child, right child and parent can be calculated using the following formulas, where 𝑖i is the index of a given node.

`leftChild` = 2∗𝑖
`rightChild` = 2∗𝑖+1
`parent` = 𝑖/2