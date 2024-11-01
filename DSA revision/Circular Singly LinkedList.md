- The last element is linked to the first element
- Instead of head, we keep track of last node in circular singly list
- **Josephus Problem
	- Question relating circular linkedl list, where nodes are deleted in a cyclic manner

 **Problem**:  Given a circular linked list with `n` nodes, eliminate every `m`-th node until only one node remains. Write a function that returns the position of the last remaining node.
 ```Java
class Node {
    int data;
    Node next;

    public Node(int data) {
        this.data = data;
        this.next = null;
    }
}

public class JosephusProblem {
    public static int findJosephusPosition(int n, int m) {
        // Create the circular linked list
        Node head = new Node(1);
        Node current = head;
        for (int i = 2; i <= n; i++) {
            current.next = new Node(i);
            current = current.next;
        }
        current.next = head; // Connect the last node to the head (circular)

        // Now, eliminate every m-th node
        Node prev = current; // This is the last node (before the head)
        current = head; // Start from the head

        while (n > 1) {
            // Move to the m-th node
            for (int i = 1; i < m; i++) {
                prev = current;
                current = current.next;
            }
            // Remove the m-th node
            prev.next = current.next;
            current = prev.next; // Move current to the next node after removal
            n--; // One node has been removed, so decrease the total number of nodes
        }
        
        return current.data; // The last remaining node
    }

    public static void main(String[] args) {
        int n = 8; // Number of people
        int m = 3; // Step size

        System.out.println("The position of the last remaining person is: " + findJosephusPosition(n, m));
    }
}

```