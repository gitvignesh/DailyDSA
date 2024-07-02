Solution: https://leetcode.com/problems/linked-list-cycle/submissions/1306702424

```kotlin
fun hasCycle(head: ListNode?): Boolean {
	var slow = head
	var fast = head

	while (fast != null && fast.next != null) {
		slow = slow!!.next
		fast = fast.next.next

		if (slow == fast) {
			return true
		}
	}
	return false
}
```