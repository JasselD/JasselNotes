![[Pasted image 20241102235224.png]]

**In-order traversal (LNR)
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

**