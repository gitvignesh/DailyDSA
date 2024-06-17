Solution: https://leetcode.com/problems/invert-binary-tree/submissions/1290669252

```kotlin
fun invertTree(root: TreeNode?): TreeNode? {
        if (root == null){
            return null
        }
        
        val temp = root.left
        root.left = root.right
        root.right = temp

        invertTree(root.left)
        invertTree(root.right)
        
        return root
    }
```

Topic: [[Trees]]