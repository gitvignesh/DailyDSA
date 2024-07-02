Solution: https://leetcode.com/problems/last-stone-weight/submissions/1303926620

```kotlin
fun lastStoneWeight(stones: IntArray): Int {
	val size = stones.size
	val maxHeap = PriorityQueue<Int>(compareByDescending { it })

	for (stone in stones) {
		maxHeap.add(stone)
	}

	while (maxHeap.size > 1) {
		val big = maxHeap.remove()
		val small = maxHeap.remove()
		val newStone = big - small
		if(newStone > 0) {
			maxHeap.add(newStone)
		}
	}
	maxHeap.add(0)
	return maxHeap.remove()
}
```

Topic: [[Heaps]]