- A FIFO data structure that serves elements with the highest priority first before elements with lower priority

```Java
import java.util.*; public class Main{ public static void main(String args[]) { 

//Strings in default order 
Queue<String> queue = new PriorityQueue<>(); 

//Strings in reverse order 
Queue<String> queue = new PriorityQueue<>(Collections.reverseOrder()); 

queue.offer("B"); 
queue.offer("C");
queue.offer("A"); 
queue.offer("F");
queue.offer("D"); 

while(!queue.isEmpty()) { System.out.println(queue.poll()); } 
} }
```

HEAP
**Min Heap
- Smaller number, higher priority

**Max Heap
- Larger number, higher priority