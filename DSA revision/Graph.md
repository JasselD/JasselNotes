- Non-linear collection comprised of a set of vertices(nodes) and a set of edges(links which connect two nodes together)

**Directed graph
- Contains edges that will link nodes to each other
- Adjacency Matrix:
	- ![[Pasted image 20241104163650.png]]
- Adjacency List:
	- ![[Pasted image 20241104163849.png]]
	- 
- Big O: O(1)

**Weighted graph
- A graph where each of the edges also hold a data value
- ![[Pasted image 20241104164253.png]]

**Connected vs Disconnected graphs
- Fully connected graph is a graph where there is a path between every pair of vertices. From one vertex it is possible to travel to another vertex in the graph
- A graph is disconnected if there is no path from a vertex in to travel to one or more other vertices in the graph
- ![[Pasted image 20241104164903.png]]

[[Path]]

![[Pasted image 20241104165642.png]]
**Adjacency list
- An array/arraylist of linkedlist
- Each linkedlist has a unique node at the end 
- All adjacent neighbours to that node are added to that node's linkedlist
- Big O: O(v)
```Java
public class Main { public static void main(String[] args) { // Adjacency List = An array/arraylist of linkedlists. // Each LinkedList has a unique node at the head. // All adjacent neighbors to that node are added to that node's linkedlist // runtime complexity to check an Edge: O(v) // space complexity: O(v + e) Graph graph = new Graph(); graph.addNode(new Node('A')); graph.addNode(new Node('B')); graph.addNode(new Node('C')); graph.addNode(new Node('D')); graph.addNode(new Node('E')); graph.addEdge(0, 1); graph.addEdge(1, 2); graph.addEdge(1, 4); graph.addEdge(2, 3); graph.addEdge(2, 4); graph.addEdge(4, 0); graph.addEdge(4, 2); graph.print(); //System.out.println(graph.checkEdge(0, 1)); } } import java.util.*; public class Graph { ArrayList<LinkedList<Node>> alist; Graph(){ alist = new ArrayList<>(); } public void addNode(Node node) { LinkedList<Node> currentList = new LinkedList<>(); currentList.add(node); alist.add(currentList); } public void addEdge(int src, int dst) { LinkedList<Node> currentList = alist.get(src); Node dstNode = alist.get(dst).get(0); currentList.add(dstNode); } public boolean checkEdge(int src, int dst) { LinkedList<Node> currentList = alist.get(src); Node dstNode = alist.get(dst).get(0); for(Node node : currentList) { if(node == dstNode) { return true; } } return false; } public void print() { for(LinkedList<Node> currentList : alist) { for(Node node : currentList) { System.out.print([node.data](https://www.youtube.com/redirect?event=comments&redir_token=QUFFLUhqbl92emZ1RW9XR1N2LUFjUW9NNFo3Z2JHVUV2QXxBQ3Jtc0trUWlWNGVEdVB6UF9sbERSR1NWekNxLW1fVGRCMFdYU0ZwWGJKemszLUxhNF9PbTB2dy1oNldZR05GRkhhel9MLVBSSzJuYzU4UEQzbkNrTjh6VVdWSEQzX2U2QW1GZHNuZkcxb3VzSkpQZk5GZTVqaw&q=http%3A%2F%2Fnode.data%2F) + " -> "); } System.out.println(); } } } public class Node { char data; Node(char data){ [this.data](https://www.youtube.com/redirect?event=comments&redir_token=QUFFLUhqbThVTEN6aTlXc205Y3RuZE1vY1JpY28ydHMwQXxBQ3Jtc0tsNmFHWTdGVXNKM3hpa0lscVJCckZFbVhlRE52eGxLSkFuR2FMdTNnWHZUSHE4cDZzdjV2dms2akw4NTA1cGc2c3oybWFQc2VBUzM1U3dhTThWRWFjTzVJSUFMUkdQeHFaQTZ2YU1nbmFhbUVSM19iSQ&q=http%3A%2F%2Fthis.data%2F) = data; } }

Show less
```