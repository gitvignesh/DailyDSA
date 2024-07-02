Solution: https://leetcode.com/problems/same-tree/submissions/1297883448

```kotlin
fun isSameTree(p: TreeNode?, q: TreeNode?): Boolean {
	if (p == null && q == null) {
		return true
	} else if (p != null && q != null) {
		if  (p.`val` != q.`val`) {
			return false
		}
		
		val isLeftSame = isSameTree(p.left, q.left)
		val isRightSame = isSameTree(p.right, q.right)
		return isLeftSame && isRightSame
	}  else {
		return false
	}
}
```

Topic: [[Trees]]