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

**Problem**:  Implement a circular queue with the following operations:
- `enqueue(x)`: Add an element to the rear of the queue.
- `dequeue()`: Remove an element from the front of the queue.
- `isFull()`: Check if the queue is full.
- `isEmpty()`: Check if the queue is empty.
```Java
public class CircularQueue {
    private int[] queue;
    private int front;
    private int rear;
    private int size;

    public CircularQueue(int capacity) {
        queue = new int[capacity];
        front = -1;
        rear = -1;
        size = capacity;
    }

    public boolean isFull() {
        return (rear + 1) % size == front;
    }

    public boolean isEmpty() {
        return front == -1;
    }

    public void enqueue(int element) {
        if (isFull()) {
            System.out.println("Queue is full. Cannot enqueue.");
            return;
        }

        if (isEmpty()) {
            front = 0;
        }

        rear = (rear + 1) % size;
        queue[rear] = element;
    }

    public int dequeue() {
        if (isEmpty()) {
            System.out.println("Queue is empty. Cannot dequeue.");
            return -1;
        }

        int element = queue[front];
        if (front == rear) {
            // Queue becomes empty
            front = -1;
            rear = -1;
        } else {
            front = (front + 1) % size;
        }

        return element;
    }

    public void display() {
        if (isEmpty()) {
            System.out.println("Queue is empty.");
            return;
        }

        System.out.print("Queue elements: ");
        int i = front;
        while (true) {
            System.out.print(queue[i] + " ");
            if (i == rear) {
                break;
            }
            i = (i + 1) % size;
        }
        System.out.println();
    }

    public static void main(String[] args) {
        CircularQueue cq = new CircularQueue(5);

        cq.enqueue(10);
        cq.enqueue(20);
        cq.enqueue(30);
        cq.enqueue(40);
        cq.display();

        System.out.println("Dequeued element: " + cq.dequeue());
        cq.display();

        cq.enqueue(50);
        cq.enqueue(60);
        cq.display();
    }
}
```

