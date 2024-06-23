Solution: https://leetcode.com/problems/balanced-binary-tree/submissions/1297867405

```kotlin
fun isBalanced(root: TreeNode?): Boolean {
	var check = true
	fun dfsHeight(node: TreeNode?): Int {
		if (node == null) {
			return 0
		}
		val leftH = dfsHeight(node.left)
		val rightH  =dfsHeight(node.right)
		check = check && abs(leftH - rightH) <= 1
		return 1 + max(leftH, rightH)
	}
	dfsHeight(root)
	return check
}
```

Topic: [[Trees]]