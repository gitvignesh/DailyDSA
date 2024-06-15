
Question: Given an array of values, design a data structure that can query the sum of a subarray of the values.

A prefix sum is a super useful technique that can be used with arrays. Suppose we have an array `nums = [2,-1,3,-3,4]`. The basic idea here is that we create an array, say, `prefix`, and fill it up such that the value at its `i`th index denotes the running sum of a `nums` subarray that starts from `0` and goes up to and including the `i`th index. This is extremely useful when we want to retrieve the sum of a subarray ending at an arbitrary index, say `i`.

So, given an array `[2,-1,3,-3,4]`, the prefix would be `[2,1,4,1,5]`.


```kotlin
fun savePrefixSum(nums: List) {
val prefixSum = arrayListOf()
var sum = 0

for ( n in nums) {
	sum += n
	prefixSum.add(sum)
}
```