Solution: https://leetcode.com/problems/maximum-depth-of-binary-tree/submissions/1290704804

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

```

Iterative DFS Solution
```kotlin

```