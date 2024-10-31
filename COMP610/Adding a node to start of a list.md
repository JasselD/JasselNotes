- Create a new node which hold the element to add
- Set it's next link to equal the firstNode
- Set the new node to be the firstNode

```Java
public void add(E element) {
	Node<E> newNode = new Node<E>(element); // newNode.next = null;
	newNode.next = firstNode;
	firstNode = newNode;
	numElements++;
}
```