Check if the given number is an Armstrong number

Solution:
```kotlin
object ArmstrongNumber { 
	fun check(input: Int): Boolean { 
		val size = input.toString().length.toDouble() 
		var num = input 
		var sum = 0 
		while(num != 0) { 
			sum += (num % 10).toDouble().pow(size).toInt() num = num/10 
		}
		return input == sum 
	}
}
```

Topics: [[Operators]] 