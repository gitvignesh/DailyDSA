Solution: https://leetcode.com/problems/diameter-of-binary-tree/submissions/1296929395

```kotlin
fun diameterOfBinaryTree(root: TreeNode?): Int {
	var maxDia = 0
	fun dfs(node: TreeNode?): Int {
		if(node == null) {
			return -1
		}
		val left = dfs(node.left)
		val right = dfs(node.right)
		maxDia = max(maxDia, 2+left+right)
		return 1 + max(left, right)
	}

	dfs(root)
	return maxDia
}
```

Topic: [[Trees]]