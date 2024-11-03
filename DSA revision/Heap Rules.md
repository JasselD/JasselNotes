- Non-linear collection and is a binary tree where each node has only at most k=2 children
- Balanced tree and Complete/Full tree
- **Structure must be complete
	- If the nodes on the structure is in an array, there should not be any gaps in between nodes
	- There should not be any missing nodes in the level before
	- ![[Pasted image 20241103225824.png]]
	- Big O for complete binary tree is log n

**Max Heap
- A max/descending heap
	- leftChild < parent > rightChild
	- parent is greater than children
- Insertion
	- FIrst add node to the correct leaf
	- Then adjust the node
	- Big O is O (log n) (O(1) if no need to adjust)
- Deletion
	- Only can delete root node
	- Last node will replace the root node

**Min Heap
- A min/ascending heap
	- leftChild > parent < rightChild
	- parent is less than children