- A tree is said to be "balanced" if all leaf nodes are within at least one level of each other, "unbalanced" if there are any two leaf nodes that are more than one level apart, or "degenerate" if every node has only at most one child

**AVL Trees
- A type of self-balancing BST
- Ensures that the heights of subtress of any node differ by at most 1, making it a height-balanced binary tree
- balance factor = height of left subtree - height of right subtree
	- bf = hl - hr = {-1, 0, 1}
- **Rotations
	- !!!Rotation is only done 3 nodes at a time
	- **Single right rotation (LL rotation)
		- Used when a left-heavy tree needs to rebalance
		- ![[Pasted image 20241103165143.png]]
	- **Left-right rotation (LR rotation)
		- Combination of a left rotation followed by a right rotation, used when the left subtree of a node is right-heavy
		- ![[Pasted image 20241103165555.png]]
	- **Single left rotation (RR rotation)
		- Used when a right-heavy tree needs rebalancing
		- ![[Pasted image 20241103171033.png]]
	- **Right-left rotation (RL rotation) 
		- combination of a right rotation followed by a left rotation, used when the right subtree of a node is left-heavy
		- ![[Pasted image 20241103171252.png]]
- Example:
	- ![[Pasted image 20241103171534.png]]
	- ![[Pasted image 20241103173510.png]]
	