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
- 

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
 - O(n) means that the runtime of the algorithm increases linearly with the input size. If the input size doubles, the time it takes for the algorithm to complete roughly doubles as well
 - n represents the size of the input array
 - The for loop runs once for every element in the array
 - The total time complexity of the algorithm is the sum of the individual parts:
	 1. O(1) for initialising the total
	 2. O(n) for the loop that iterates over each element in the array
	 3. O(1) for the addition operation inside the loop
	 4. O(1) for the returning the result
	 5. O(1) + O(n) + O(1)+O(1) = O(n)
- It is also linear, the amount of work increases at a constant rate as the input grows. If the size of array doubles, then the numb


