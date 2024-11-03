- A tree is said to be "balanced" if all leaf nodes are within at least one level of each other, "unbalanced" if there are any two leaf nodes that are more than one level apart, or "degenerate" if every node has only at most one child

**AVL Trees
- A type of self-balancing BST
- Ensures that the heights of subtress of any node differ by at most 1, making it a height-balanced binary tree
- balance factor = height of left subtree - height of right subtree
	- bf = hl - hr = {-1, 0, 1}
- **Rotations
	- !!!Rotation is only done 3 nodes at a time
	- Single right rotation (LL rotation)
		- ![[Pasted image 20241103165143.png]]
	- 