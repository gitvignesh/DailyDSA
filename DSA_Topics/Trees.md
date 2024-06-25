# Binary Tree
The Binary Tree is another data structure that involves nodes and pointers. We talked about nodes in the linked list chapter. We connected these nodes in a straight line with `next` and `prev` pointers. Nodes in a binary tree also have at most two pointers, but we call them the **left child** and the **right child** pointers. The first node in a binary tree is referred to as the **root** node. We draw the pointers down instead of a straight line. Mathematically speaking, a binary tree is an undirected graph with no cycles. This means that a leaf node is always guaranteed to exist.
```kotlin
class BinaryTree(){
	var content: Any? = null
	var left: BinaryTree? = null
	var right: BinaryTree? = null
}
```
**Properties**
1. Root node is the highest node of the tree and has no parents
2. Leaf nodes are nodes with no children
3. Height is equal to number nodes from root to lowest leaf
	- Height of root is 1 (My assumption)
4. Dept is equal to distance from current node to root
	- Dept of leaf is 1 (My assumption)
## BST (Binary Search Tree)
Binary Search Trees (BST) are a variation of binary trees with a sorted property to them. The property tells us that every left child must be smaller than its parent and every right child must be greater than its parent. BSTs _do not_ allow duplicates.

**Why BST:**
The question here is why bother with BSTs if we have sorted arrays? With binary search, we can search values in 𝑂(𝑙𝑜𝑔 𝑛)O(log n) time and if BST is offering the same functionality, can't we just use an array? All of this is correct. However, BST shines when we are trying to insert or delete a value. Both of these operations run in 𝑂(𝑙𝑜𝑔 𝑛) time for a BST, but 𝑂(𝑛) time with an array. So, while BSTs don't offer benefit over sorted arrays for the search functionality, they are better for insertion and deletion. In this chapter, we will focus specifically on the search operation.

Balanced BST: Balanced binary tree means that the height of the left-subtree is equal to the height of the right-subtree, or there is a difference of 1. Then we can run search in **𝑂(𝑙𝑜𝑔 𝑛)**  else it is O(height)
## DFS
Depth First Search (DFS) is a way of traversing binary search trees that prioritizes depth rather than breadth.

The idea is to keep traversing down either the left subtree or the right subtree until there are no more nodes left. There are various methods under which depth-first search is performed. These methods visit the nodes - `root, left_child, right_child` in different orders. These three methods are:
- Inorder
- Preorder
- Postorder

Depth first search is best implemented using recursion. Again, you could use a stack and do it iteratively but it is a lot more complicated.

```kotlin
//InOrder Traversal (returns sorted array)
fun traverseInOrder(root: TreeNode?) {
	if(root ==  null) {
		return
	}

	traverseInOrder(root.left)
	print("$root.`val' -> ")
	traverseInOrder(root.right)
}
```
## BFS

# AVL Tree




