**Big O notation**
- describes the performance of an algorithm as the amount of data increases
- machine independent (# of steps to completion)
- ignore smaller operations O(n + 1) -> O(n)
- Express the upper bound of an algorithm's running time
- Upper bound means for any given input this notation determines longest amount of time an algorithm can take to complete
- Example : If an algorithm takes 100 secs to complete, then the upper bound is 100 secs. The algorithm can take less than 100 secs to complete but not more than 100secs

 **Rules:
- Keep the fastest growing term
- Drop constants
example :  n = amount of data
O(1)
O(n)
O(log n)
O(n²)

**O(1)
```Java
public class AccessArray {
    public static int getFirstElement(int[] arr) {
        return arr[0];  // O(1) - direct access to the first element
    }

    public static void main(String[] args) {
        int[] numbers = {10, 20, 30, 40, 50};
        System.out.println("First element: " + getFirstElement(numbers));  // Output: 10
    }
}

```
- Accessing an element at a <mark style="background: #ABF7F7A6;">specific index</mark> like arr[0] in an array is done in <mark style="background: #ABF7F7A6;">constant time</mark>, it does not matter whether the array has 5 elements or 5 million elements, the time it takes to access arr[0] is always the same
- There are <mark style="background: #ABF7F7A6;">no loops or recursive calls</mark> that depend on the size of the input

**O(n)
```Java
public class SumArray {
    public static int sum(int[] arr) {
        int total = 0;  // O(1)
        for (int i = 0; i < arr.length; i++) {  // O(n)
            total += arr[i];  // O(1) per iteration
        }
        return total;  // O(1)
    }

    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5};
        System.out.println("Sum: " + sum(numbers));  // Output: Sum: 15
    }
}
```
 - O(n) means that the <mark style="background: #ABF7F7A6;">runtime of the algorithm increases linearly with the input size</mark>. If the input size doubles, the time it takes for the algorithm to complete roughly doubles as well
 - <mark style="background: #ABF7F7A6;">n represents the size of the input array</mark>
 - The for loop runs <mark style="background: #ABF7F7A6;">once for every element in the array</mark>
 - The total time complexity of the algorithm is the sum of the individual parts:
	 1. O(1) for initialising the total
	 2. O(n) for the loop that iterates over each element in the array
	 3. O(1) for the addition operation inside the loop
	 4. O(1) for the returning the result
	 5. O(1) + O(n) + O(1)+O(1) = O(n)
- It is also <mark style="background: #ABF7F7A6;">linear</mark>, <mark style="background: #ABF7F7A6;">the amount of work increases at a constant rate as the input grows</mark>. If the size of array doubles, then the number of iterations through the loop also doubles

**O(log n)
```Java
public class BinarySearch {
    public static int binarySearch(int[] arr, int target) {
        int left = 0;
        int right = arr.length - 1;

        while (left <= right) {
            int mid = left + (right - left) / 2;  // Calculate the middle index

            if (arr[mid] == target) {
                return mid;  // Target found at index mid, O(1) for comparison
            } else if (arr[mid] < target) {
                left = mid + 1;  // Narrow search to the right half
            } else {
                right = mid - 1;  // Narrow search to the left half
            }
        }

        return -1;  // Target not found
    }

    public static void main(String[] args) {
        int[] numbers = {1, 3, 5, 7, 9, 11, 13, 15};
        int target = 7;
        int result = binarySearch(numbers, target);
        if (result != -1) {
            System.out.println("Target found at index: " + result);  // Output: 3
        } else {
            System.out.println("Target not found");
        }
    }
}

```
- 

