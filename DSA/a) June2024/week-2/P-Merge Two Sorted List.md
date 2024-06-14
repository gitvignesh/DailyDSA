Solution:
```kotlin
fun mergeTwoLists(list1: ListNode?, list2: ListNode?): ListNode? {
	val result: ListNode = ListNode(0)
	var currR = result
	var curr1 = list1
	var curr2 = list2

	while (curr1 != null && curr2 != null) {
		if(curr1.`val` < curr2.`val`) {
			currR.next = curr1
			curr1 = curr1.next
		} else {
			currR.next = curr2
			curr2 = curr2.next
		}
		currR = currR.next
	}

	if (curr1 != null) {
		currR.next = curr1
	}else if (curr2 != null) {
		currR.next = curr2
	}
	
	return result.next
}
```

Supplementary  topics covered:
Difference between "and" - "&&" in Kotlin
"and": its not shorting (both side are evaluated) used for bitwise operations
"&&": its shorting (if first check is wrong second side is not evaluated) used for logical operations
