Solution: https://leetcode.com/problems/lexicographically-smallest-string-after-a-swap/submissions/1320708763

```kotlin
 fun getSmallestString(s: String): String {
	
	val len = s.length
	var t = StringBuilder(s)

	for (i in 0..len-2){
		val curr = t[i].toInt()
		val next = t[i+1].toInt() 

		if (curr and 1 == next and 1  && curr > next){
			val temp = t[i]
			t.setCharAt(i, t[i+1])
			t.setCharAt(i+1, temp)
			return t.toString()
		}
	}

	return t.toString()
}
```

Topics: [[Bit Manipulation]], [[String Manipulation]]