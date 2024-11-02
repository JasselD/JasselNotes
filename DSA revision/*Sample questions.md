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
	- Effiency of radix sort depends on the value of k (number of digits) and n (number of elements). For smaller values of k; radix sort can be more efficient than O(n log n)

- What is the asymptotic complexity (Big O) of bin sort?
	- O(K + n)