Solution: https://leetcode.com/problems/delete-node-in-a-bst/submissions/1299623448

```kotlin
 fun deleteNode(root: TreeNode?, key: Int): TreeNode? {
	if (root == null) {
		return null
	}
	if (root.`val` > key){
		root.left = deleteNode(root.left, key)
	} else if (root.`val` < key) {
		root.right = deleteNode(root.right, key)
	} else {
		if (root.left == null){
			return root.right
		} else if(root.right == null){
			return root.left
		} else {
			//Replace the node with its inorder successor.
			val minValue = findMinValue(root.right)
			root.`val` = minValue
			root.right = deleteNode(root.right, minValue)
		}
	}
	return root
}

fun findMinValue(root: TreeNode) : Int{
	var curr = root
	while(curr != null && curr.left != null){
		curr = curr.left
	}
	return curr.`val`
}
```

Topic: [[Trees]]