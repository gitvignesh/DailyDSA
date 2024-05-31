Submission Link: https://leetcode.com/problems/contains-duplicate/submissions/1272856195

```kotlin
fun containsDuplicate(nums: IntArray): Boolean {
	val vistedSet = hashSetOf<Int>();
	for (num in nums){
		if (vistedSet.contains(num)){
			return true
		} else {
			vistedSet.add(num)
		}
	}
	
	return false
}
```


Supplementary topics covered:
1. HashSet Creation methods