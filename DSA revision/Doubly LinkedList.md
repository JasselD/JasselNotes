- Two way linked list, can traverse forwards and backwards
- ListNode in Doubly linked list
	- previous
	- data
	- next
```Java
public class ListNode {
	int data;
	ListNode previous;
	ListNode next;

	public ListNode(int data) {
		this.data = data;
	}
}
```

**Implementation
```Java
public class DoublyLinkedlist {

	private class ListNode{
		private int data;
		private ListNode previous;
		private ListNode next;

		public ListNode() {
			this.data = data;
		}
	}
}
```