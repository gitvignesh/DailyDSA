Solution: https://leetcode.com/problems/maximum-depth-of-binary-tree/submissions/1292314023

Recursive Solution (DFS)
```kotlin
fun maxDepth(root: TreeNode?): Int {
	if (root == null){
		return 0;
	}
	var currDepth = 1

	val leftDepth = currDepth + maxDepth(root.left)
	val rightDepth = currDepth + maxDepth(root.right)

	return maxOf(leftDepth, rightDepth)
}
```

BFS Solution
```kotlin
fun maxDepth(root: TreeNode?): Int {
	if (root == null) {
		return 0;
	}
	val queue = LinkedList<TreeNode>()
	var maxDepth = 0
	queue.add(root) 

	while (queue.isNotEmpty()) {
		val levelSize = queue.size
		for (i in 0..levelSize-1) {
			val node = queue.removeFirst()
			if (node.left != null) {
				queue.add(node.left)
			}
			if (node.right != null) {
				queue.add(node.right)
			}
		}
		maxDepth+=1
	}
	return maxDepth
}
```

Iterative DFS Solution
```kotlin
fun maxDepth(root: TreeNode?): Int {
	val stack = LinkedList<Pair<TreeNode?, Int>>()
    stack.push(Pair(root,1))

    var depth = 0

	while (!stack.isEmpty()) {
		val (currNode, currDepth) = stack.pop()
		if(currNode != null){
			depth = maxOf(depth, currDepth)
			stack.push(Pair (currNode.right, currDepth + 1))
			stack.push(Pair (currNode.left, currDepth + 1))
		}
	}

	return depth
}
```

Topic: [[Trees]]
Supplementary Topics: 
1. Creating a array list and using it as Queue and Stack
2. Difference between push() & add() and pop() & remove()