- FIFO/LILO data structure, a collection designed for holding elements prior to processing Linear data structure
- enqueue (adding)
- dequeue (removing)
- offer(), adding a queue to the tail
- poll(), removing a queue from the head   
- peek(), peek at the head of the queue

```Java
public static void main(String[] args) {
	Queue<String> queue = new Linkedlist<String>();

	queue.offer("Karen");
	queue.offer("Chad");
	queue.offer("Steve");
	queue.offer("Harold");

	queue.poll(); // Will remove the current head

	queue.isEmpty(); // Will check if the queue is empty or not

	
}
```