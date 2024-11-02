- A tree is called as Binary Tree, if each node has zero, one or two children
- TreeNode
	- left pointer
	- data
	- right pointer
- Time complexity of building a binary tree is O (n log n)
- How to represent a treenode
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
- Implementing treenode
```Java
public class BinaryTree {
    private TreeNode root;

	// Create Tree
    private class TreeNode{
        private TreeNode left;
        private TreeNode right;
        private int data;
        
        public TreeNode(int data) {
            this.data = data;
        }
    }
	// Create Node and assign location
    public void createBinaryTree() {
        TreeNode first = new TreeNode(1);
        TreeNode second = new TreeNode(2);
        TreeNode third = new TreeNode(3);
        TreeNode fourth = new TreeNode(4);
        TreeNode fifth = new TreeNode(5);
        
        root = first; // root points first
        first.left = second;
        first.right = third; 
        
        second.left = fourth;
        second.right = fifth;
    }
}
```
