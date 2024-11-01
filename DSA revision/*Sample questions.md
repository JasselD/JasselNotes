- If a liner collection is often used by adding or removing a node from its head or tail. What is the best option for this liner collection?

- In a stack to ensure O(1) push, pop and peek methods where should the top of the stack be if using an array?

- In a stack to ensure O(1) push, pop and peek methods where should the top of the stack be if using an singly linked list?

- What data structure can be best utilized to reverse the order of a liner collection?

- What is the difference between add() method in set and add() method in list?

- What is the Big O notation
```Java
    public static String toString(LinkedList<Integer> list) {
        String details = "";
        for(int i = 0; i < list.size(); i++) {
            details += list.get(i) + "";
        }
        return details;
    }
// O(n²)
```

```Java
    public static String toString(ArrayList<Integer> list) {
        String details = "";
        for(int i = 0; i < list.size(); i++) {
            details += list.get(i) + "";
        }
        return details;
    }
// O(n)
```

- Explanation: Linkedlist requires linear time for each access, making it inefficient for scenarios where you need to read elements sequentially multiple time, while Arraylist requires constant time access which provides much better performance for