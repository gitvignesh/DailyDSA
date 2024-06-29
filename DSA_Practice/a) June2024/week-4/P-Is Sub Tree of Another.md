Solution: https://leetcode.com/problems/subtree-of-another-tree/submissions/1298312050

```kotlin
fun isSubtree(root: TreeNode?, subRoot: TreeNode?): Boolean {  
	if (subRoot == null) {
		return true
	}

	if (root == null) {
		return false
	}

	if (isSameTree(root, subRoot)){
		return true
	}

	return isSubtree(root.left, subRoot) || isSubtree(root.right, subRoot)

}

fun isSameTree(p: TreeNode?, q: TreeNode?): Boolean {
	if (p == null && q == null) {
		return true
	}
	if (p != null && q != null && p.`val` == q.`val`) {
		val isLeftSame = isSameTree(p.left, q.left)
		val isRightSame = isSameTree(p.right, q.right)
		return isLeftSame && isRightSame
	}
	return false
}
```

Topic: [[Trees]]
