**Data structure questions
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
**Sorting algorithms questions
- What is the typical asymptotic complexity (Big O) of binary search?
	- O(log n), because binary search works by dividing the search range in half with each iteration

- Why binary search requires the elements must be sorted?
	- Binary search works by comparing the middle element to the target value. If the array is not sorted, there is a chance that the left or right half does not contain the correct element

- What is the best way of guessing a number from range of 0 to 1000 by using binary search? What is the maximum number of guesses needed to guess the number?
	- The best way is the guess the middle of the range. Each time you guess, based on whether the target is higher or lower, you can eliminate half the remaining numbers. The maximum number of guesses is log2[1000] = 10. In the worst case, you would need 10 guesses to guess a number from 0 to 1000

- Which are the O(n^2) sorting algorithms we have learnt?
	- Selection Sort
	- Bubble Sort
	- Insertion Sort
	- These algorithms have quadratic time complexity 

- Which are the O(n log n) sorting algorithms we have learnt?
	- Quick Sort
	- Merge Sort
	- Both of these algorithms use divide and conquer approach, recursively splitting the input array into smaller subarrays and sorting them

- The asymptotic complexity (Big O) of radix sort is O(kn). What does k mean and what does n mean?
	- In radix sort, n is the number of elements to be sorted, while k is the number of digits (or maximum length of the elements)

- Does O(kn) always better than O(〖nlog〗_2⁡n) sorting? If there are 83 digits numbers needs to be sort, would you use radix sort? How about 84 digits numbers? How about 82 digits numbers?
	- Effiency of radix sort depends on the value of k (number of digits) and n (number of elements). For smaller values of k; radix sort can be more efficient than O(n log n). But as K increases, the overhead of sorting each digit may make radix sort slower than O (n log n) sorting algorithms like quick sort or merge sort. For large digit counts, O (n log n) will be more effiecient

- What is the asymptotic complexity (Big O) of bin sort?
	- O(K + n)

---
**Thread questions
- What is the biggest issue of multi-thread? What is the name of this issue?
	- Race condition, this happens when mulitple threads access and modify shared data at the same time. The result can vary depending on the order in which the threads run, leading to incorrect results

- What is a monitor object?
	- A monitor is a synchorization contrust that allows threads to have exclusive access to critical sections of code

- Correct?
•synchronize ( Object my_object) { … //critical session}
correct

•synchronize ( char my_char) { … //critical session}
incorrect, char cannot synchronize 

•synchronize ( “I am always correct!”) { … //critical session}
incorrect, if you synchronize on a string literal, it might accidentally lock other code that uses the same string

•synchronize ( new String (“I am a monitor object”)) { … //critical session}
incorrect, 

•synchronize ( “I am the best!” + Math.random()) { … //critical session}
wrong

- Can we put all the code of run() method surround by the synchronize?
	- No, this will slown down the program