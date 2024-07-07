Solution: https://leetcode.com/problems/number-of-1-bits/submissions/1312591464

```kotlin
fun hammingWeight(n: Int): Int {
	var count = 0
	var num = n
	while (num != 0) {
		if (num and 1 == 1) {
			count++
		}
		num = num shr 1
	}
	return count
}
```

Topic: [[Bit Manipulation]]


