Solution: https://leetcode.com/problems/pascals-triangle/submissions/1313972743

```kotlin
fun generate(numRows: Int): List<List<Int>> {
	var ans: ArrayList<ArrayList<Int>> = arrayListOf(arrayListOf(1))

	for ( i in 1..numRows-1) {
		var prevList = arrayListOf(0) + ans[i-1] + arrayListOf (0)
		var currList = arrayListOf<Int>()

		for (j in 0..prevList.size-2) {
			currList.add (prevList[j] + prevList[j+1])
		}

		ans.add(currList)
	}

	return ans
}
```

Topic: [[Arrays and Hashing]], [[Two Pointers]]