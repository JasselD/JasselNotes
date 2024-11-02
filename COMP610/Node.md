- ListNode is used to implement linked lists efficiently
- Linked list are dynamic data structures that consist of nodes
- Each node holds a value and a reference to next node in the list

**ListNode**
- represents a single node in a linked list
- contains 2 main components 
	  value/data stored in the node 
	  reference to the next node in the list

```Java
public class Node {
	public class Node {
		public static void main(String args[]) {
		Node x = new Node(1, null);
		Node y = new Node(2, x);
		System.out.println(y.getNext().getData());
	}
	
	private int data;
	private Node next;

	public Node(int d, Node nx) {
		data = d;
		next = nx;
	}

	public int getData() {
		return data;
	}

	public Node getNext() {
		return next;
	}

	public void setData(int d) {
		data = d;
	}

	public void setNext(Node n) {
		next = n;
	}
}
```

