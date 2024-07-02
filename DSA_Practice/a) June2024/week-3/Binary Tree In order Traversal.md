Solution: https://leetcode.com/problems/binary-tree-inorder-traversal/submissions/1294857646

```kotlin
fun inorderTraversal(root: TreeNode?): List<Int> {
	val result = arrayListOf<Int>()
	
	fun dfs(node: TreeNode?){
		if (node == null) {
			return
		}

		dfs(node.left)
		result.add(node.`val`)
		dfs(node.right)
	}
	dfs(root)
	return result
}
```

Topic [[Trees]]
Supplementary Topics:
1. [[Collections]]