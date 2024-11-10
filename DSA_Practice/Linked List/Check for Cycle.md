Question: Check if there is a cycle in the linked list.

Basic solution is keep a note  of the visited note in a "Hash-set" as its access in O(1)
time and space complexity would be O(n)
Solution: https://leetcode.com/problems/linked-list-cycle/submissions/1448526650
```kotlin
fun hasCycle(head: ListNode?): Boolean {
	val visted = hashSetOf<ListNode>()
	var curr =  head

	while(curr != null) {
		if (curr in visted) {
			return true
		} else {
			visted.add(curr)
		}
		curr = curr.next
	}
	return false
}
```


Space complexity can be reduced by using fast and slow pointers.
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

Topic: [[Linked List]], [[Fast and Slow Pointers]]
