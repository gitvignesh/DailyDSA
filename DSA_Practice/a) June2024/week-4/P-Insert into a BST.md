Solution: 
https://leetcode.com/problems/insert-into-a-binary-search-tree/submissions/1299524726

```kotlin
 fun insertIntoBST(root: TreeNode?, `val`: Int): TreeNode? {
	if (root == null) {
		return TreeNode(`val`)
	}

	if (root.`val` > `val`){
		root.left = insertIntoBST(root.left, `val`)
	} else {
		root.right = insertIntoBST(root.right, `val`)
	}

	return root
}
```

Topic: [[Trees]]