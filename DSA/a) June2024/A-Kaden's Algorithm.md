

Kadane's algorithm is a greedy/dynamic programming algorithm that can be used on array problems to bring the time complexity down to 𝑂(𝑛). It is used to calculate the maximum sum subarray ending at a particular position.

Find the non-empty **Sub-Array** with the largest sum.
Variation-1: (return the sum)
Submission: https://leetcode.com/problems/maximum-subarray/submissions/1273789451

```kotlin
fun maxSubArray(nums: IntArray): Int {
	var maxSum = nums[0]
	var currSum = 0
	for (num in nums) {
		if (currSum < 0) {
			currSum = 0
		}    
		currSum += num
		maxSum = maxOf(maxSum, currSum)
	}
	return maxSum;
}
```

Variation-2: (return the indices)

This is a divide and conquer solution: 


