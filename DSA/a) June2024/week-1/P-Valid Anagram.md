Solution: https://leetcode.com/problems/valid-anagram/submissions/1272873636


```kotlin
   fun isAnagram(s: String, t: String): Boolean {
        if (s.length != t.length) {
            return false
        }
        val sCountMap = hashMapOf<Char, Int>()
        val tCountMap = hashMapOf<Char, Int>()

        for (i in 0..s.length-1) {
            sCountMap[s[i]] = sCountMap.getOrElse(s[i], {0}) + 1
            tCountMap[t[i]] = tCountMap.getOrElse(t[i], {0}) + 1

        }

        for (key in sCountMap.keys) {
            if(sCountMap[key] != tCountMap[key]){
                return false
            }
        }
        return true
    }
```


Supplementary topics covered:
1. HashMap Creation methods
2. Looping techniques