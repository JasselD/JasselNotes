![[Pasted image 20241102235224.png]]

**In-order traversal (LNR)
Steps:
- Starting at root
- Check if current Node not empty
- Recursively move to left subtree (L)
- Process/visit current node (N)
- Recursively move to right subtree (R
- Left -> root -> right

```Java
public void traversal() {
	traversal(root);
}

private void traversal(TreeNode root) {
	if(root.left != null) {
		traversal(root.left);
	}
	System.out.println(root + ", ");
	if(root.right != null) {
		traversal(root.right);
	} 
}
```

**Post-order traversal (LRN)
Steps:
- Starting at root (root is printed at the end)
- Check if current node not empty
- Recursively move to left subtree L
- Recursively move to right subtree R
- Process/visit current node N
- Left -> right -> root

```Java
private void traverseTree(Node root) {

	traverseTree(root.left);
	traverseTree(root.right);
	System.out.println(root.data);
}
```

**Pre-oder traversal (NLR)
Steps:
- Starting at root (root is printed at the beginning)
- Check if current node not empty
- Proccess/visit current node N
- Recursively move to left subtree L
- Recursively move to right subtree R
- Root -> left -> right

```Java
private void traverseTree(Node root) {

	System.out.println(root.data);
	traverseTree(root.left);
	traverseTree(root.right);
}
```

**Level-order traversal (Queue)
- Starts from the root, and goes down level by level from left to right
- Steps
	- Enqueue root
	- Loop while queue not empty
	- Get reference to front node in queue
	- Enqueue front node's left child 
	- Enqueue front node's right child
	- Dequeue front node and repeat loop

```Java
void levelOrderTraversal(Node root) {
	if(root == null) return;
}

	Queue<Node> queue = new Linkedlist<>();
	queue.add(root);

	while(!queue.isEmpty()) {
		Node current = queue.
	}

```
