- BST
- Time complexity O(log n)
- Time complexity of building a binary tree is O (n log n)
-  leftChild < parent < rightChild 
- Implementing
```Java
public class Node<T extends Comparable<T>> {
	private T data;
	private Node<T> leftChild;
	private Node<T> rightChild;
}
```