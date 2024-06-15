Solution: https://leetcode.com/problems/reverse-linked-list/submissions/1176592101

__*Iterative Solution*__
```kotlin
fun reverseList(head: ListNode?): ListNode? {
	var prev: ListNode? = null
	var curr = head

	while (curr != null) {
		val temp = curr.next
		curr.next = prev
		prev = curr
		curr = temp
	}

	return prev
}
```

__*Recursive Solution*__
```kotlin
fun reverseList(head: ListNode?): ListNode? {
	
}
```
Note: Basic idea is keeping not of the connection that needs to removed before making the actual change