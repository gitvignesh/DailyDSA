Solution Link: https://leetcode.com/problems/valid-palindrome/submissions/1279027134

```kotlin
fun isPalindrome(s: String): Boolean {
        if (s.isEmpty()) {
             return true
        }
        var L = 0
        var R = s.length - 1

        while(L<R){
            while (isOther(s[L]) && L<R) {
                L++;
            }

            while (isOther(s[R]) && L<R) {
                R--;
            }

            if (s[L].lowercase() != s[R].lowercase()) {
                return false
            }

            L++;
            R--;
        }
        return true
}
fun isOther(ch:Char): Boolean {
	return !(ch in 'a'..'z') && !(ch in 'A'..'Z') && !(ch in '0'..'9')
}
```

supplementary topics:
case conversion: lowercase(), lowercaseChar()
letter check: isLetterOrDigit()