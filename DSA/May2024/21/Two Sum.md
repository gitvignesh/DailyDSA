Submission link : https://leetcode.com/problems/two-sum/submissions/1263593862

```kotlin
fun twoSum(nums: IntArray, target: Int): IntArray {
	val seenMap = hashMapOf<Int, Int>();

	for ((index, num) in nums.withIndex()){
		val diff = target - num

		if (seenMap.contains(diff)){
			return intArrayOf(seenMap[diff]!!, index)
		} else {
			seenMap[num] = index
		}
	}

	throw Exception("Invalid Target")
}
```


Supplementary topics covered:
1. HashMap Creation methods
2. Looping techniques
3. Array Creation methods