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

	private ListNode head;
	private ListNode tail;
	private int length;

	private class ListNode{
		private int data;
		private ListNode previous;
		private ListNode next;

		public ListNode(int data) {
			this.data = data;
		}
	}

	public DoublyLinked() {
		this.head = null;
		this.tail = null;
		this.length = 0;
	}

	public boolean isEmpty() {
		return length == 0; // head == null; head is empty
	}

	public int length() {
		return length;
	}
}
```