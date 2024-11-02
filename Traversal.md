![[Pasted image 20241102235224.png]]

**In-order traversal (LNR)
- Starting at root
- Check if current Node not empty
- Recursively move to left subtree (L)
- Process/visit current node (N)
- Recursively move to right subtree (R)

```Java
public void traversal() {
	traversal(root);
}

private void traversal(TreeNode root)
```