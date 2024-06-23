Solution: https://leetcode.com/problems/diameter-of-binary-tree/submissions/1297855401

```kotlin
fun diameterOfBinaryTree(root: TreeNode?): Int {
	var diameter = 0
	fun findHeight(root: TreeNode?): Int {
		if(root == null){
			return 0
		}
		val leftH = findHeight(root.left)
		val rightH = findHeight(root.right)
		diameter = maxOf(diameter, leftH + rightH) 
	   return 1 + max(leftH, rightH)
	}
	findHeight(root)
	return diameter
}
```

Topic: [[Trees]]