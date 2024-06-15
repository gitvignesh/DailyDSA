A linked list is another data structure that is like an array in the sense that it stores elements in an ordered sequence, but there are also differences.

The first difference is that linked lists are made up of objects called `ListNode`'s. This object contains two attributes:
1. `value` - This stores the value of the node, the value can be anything - a character, an integer, etc.
2. `next` - This stores the reference to the next node in the linked list. The picture below visualizes the `ListNode` object. This will make more sense a little later on.

_Traversal_
```kotlin
while(curr.next != null){
	curr = curr.next
}
```

| Operation | Big-O Time Complexity | Note                                                                |
| --------- | --------------------- | ------------------------------------------------------------------- |
| Access    | 𝑂(𝑛)                |                                                                     |
| Search    | 𝑂(𝑛)                |                                                                     |
| Insertion | 𝑂(1)*                | Assuming you have the reference to the node at the desired position |
| Deletion  | 𝑂(1)*                | Assuming you have the reference to the node at the desired position |
