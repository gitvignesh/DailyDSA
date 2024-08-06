Solution: https://leetcode.com/problems/remove-element/submissions/1346834827

```kotlin
class Solution {
    fun removeElement(nums: IntArray, `val`: Int): Int {
        var k = 0

        for (num in nums) {
            if (num != `val`){
                nums[k] = num
                k += 1
            }
        }

        return k
    }
}
```

Topics: [[Collections]], [[Two Pointers]]
