Binary search is an efficient way of searching for elements within a sorted array. Typically we are given an array, and an element called the `target` to search for.

At its core, binary search divides the array in the middle, called `mid` and compares the value at `mid` to the `target` value. If the `mid` value is lower than the `target`, it eliminates the left half of the array and searches on the right of `mid`. If `mid` is higher than the `target`, we search to the left. We either find the `target` or determine that the `target` doesn't exist in the array.

**Variation-1 (Search Array):**
Solution: https://leetcode.com/problems/binary-search/submissions/1285454781

```kotlin
fun search(nums: IntArray, target: Int): Int { 
	var L = 0
	var R = nums.size-1 
	var mid:Int = L + (R-L)/2 
	while (L<=R) { 
		mid = L + (R-L)/2
		if (target == nums[mid]){ 
			return mid 
		}else if(target > nums[mid]) { 
			L = mid + 1 
		} else {
			R = mid - 1 
		} 
	} 
	return -1 
}
```

**Variation-2 (Search Range):**
Imagine your friend gave you a range from 1 - 100 and asked you to guess the number they were thinking of. There are three outcomes. Either your guess is correct, too small or too big.

If your guess is too small, you will have to guess higher and if your guess it too big, you will have to guess lower. The difference here is that you do not know what number your friend is thinking of (aka the `target` value). All you have is feedback from them each time you guess, and you adjust your next guess accordingly.

Example Problem: Guess Number higher or lower
Solution: https://leetcode.com/problems/guess-number-higher-or-lower/submissions/1285571004
```kotlin
class Solution:GuessGame() {
    override fun guessNumber(n:Int):Int {
    var L = 1
    var R = n
    while (L <= R) {
        val mid:Int = L + (R - L) / 2
        val result = guess(mid)
        when {
            result == 0 -> return mid
            result < 0 -> R = mid - 1
            else -> L = mid + 1
        }
    }
    return -1
    }
}
```