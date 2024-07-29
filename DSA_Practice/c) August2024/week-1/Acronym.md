Question:
Help generate some jargon by writing a program that converts a long name like Portable Network Graphics to its acronym (PNG).

Punctuation is handled as follows: hyphens are word separators (like whitespace); all other punctuation can be removed from the input.

Solution:
```kotlin
object Acronym { 
	fun generate(phrase: String) : String { 
		val items = phrase.split(Regex("[- ]+")) 
		var result = ""
		for (item in items) { 
			val first = item[0]
			result += if(first.isLetterOrDigit()) { 
				first.toString().capitalize()
			} else { 
				item[1].toString().capitalize() 
			} 
		} 
		return result 
	} 
}
```

Topics: [[Regex]]