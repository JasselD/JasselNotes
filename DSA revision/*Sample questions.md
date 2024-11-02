- If a liner collection is often used by adding or removing a node from its head or tail. What is the best option for this liner collection?
	- Doubly Linkedlist because it offers effiecient node management and it can traverse both directions

- In a stack to ensure O(1) push, pop and peek methods where should the top of the stack be if using an array?
	- To maintain O(1) time complexity for stack when using an array, the top of the stack should be at the end of the array

- In a stack to ensure O(1) push, pop and peek methods where should the top of the stack be if using an singly linked list?
	- To maintain O(1) time complexity for stack when using singly linked list, the top of the stack should be at the head of the singly linked list

- What data structure can be best utilized to reverse the order of a liner collection?
	- Stack because of its FILO/LIFO behavior

- What is the difference between add() method in set and add() method in list?
	- Set add(): Adds an element only if it's not already present; returns true or false
	- List add(): Always adds the element at the end of the List; generally returns true

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

- Explanation: Linkedlist requires linear time for each access, making it inefficient for scenarios where you need to read elements sequentially multiple time, while Arraylist requires constant time access which provides much better performance for toString method
---

- What is the typical asymptotic complexity (Big O) of binary search?
	- O(n²)

- Why binary search requires the elements must be sorted?
	- 

- What is the best way of guessing a number from range of 0 to 1000 by using binary search? What is the maximum number of guesses needed to guess the number?
	- 

- Which are the O(n^2) sorting algorithms we have learnt?
	- Selection Sort
	- Bubble Sort
	- Insertion Sort

- Which are the O(〖nlog〗_2⁡n) sorting algorithms we have learnt?
	- 

- The asymptotic complexity (Big O) of radix sort is O(kn). What does k mean and what does n mean?

- Does O(kn) always better than O(〖nlog〗_2⁡n) sorting? If there are 8 3 digits numbers needs to be sort, would you use radix sort? How about 8 4 digits numbers? How about 8 2 digits numbers?

- What is the asymptotic complexity (Big O) of bin sort?