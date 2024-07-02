Solution: 
https://leetcode.com/problems/kth-largest-element-in-a-stream/submissions/1302926556

```kotlin
class KthLargest(k: Int, nums: IntArray) {
    private val minHeap = PriorityQueue<Int> (k)
    private val size = k


    init {
        nums.forEach {
           add(it)    
        }
    }

    fun add(`val`: Int): Int {
        if (minHeap.size != size){
            minHeap.add(`val`)
        } else {
            if (minHeap.peek() < `val`) {
                minHeap.remove()
                minHeap.add(`val`)
            }
        }
        return minHeap.peek()
    }
}
```

Topic: [[Heaps]]