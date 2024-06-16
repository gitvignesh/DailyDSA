Solution: https://leetcode.com/problems/length-of-last-word/submissions/1289670253

```kotlin
fun question(s: String): int {
	val len = s.length - 1
    var count = 0

	for (n in len downTo 0){
		if (s[n] == ' ' && count>0){
			return count
		} else if (s[n] != ' '){
			count++
		}
	}
    return count
}
```

Topic: [[Arrays and Hashing]]
Supplementary Topics:
1. Range functions "x..y" don't go in reverse have to use "downTo"
2. Step option in range.