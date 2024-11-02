- A tree is called as Binary Tree, if each node has zero, one or two children
- TreeNode
	- left pointer
	- data
	- right pointer
- Time complexity of building a binary tree is O (n log n)
```Java
public class TreeNode{
	private int data;
	private TreeNode left;
	private TreeNode right;

	public TreeNode(int data){
		this.data = data;
	}
}
```

