Solution: https://leetcode.com/problems/single-number/submissions/1308504331

Question: Given a **non-empty** array of integers `nums`, every element appears _twice_ except for one. Find that single one. You must implement a solution with a linear runtime complexity and use only constant extra space.

```kotlin
fun singleNumber(nums: IntArray): Int {
	var res = 0
	for (num in nums) {
		res = res xor num
	}
	
	return res
}
```

Topic: [[Bit Manipulation]]
