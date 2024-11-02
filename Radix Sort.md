- Non-comparative sorting algorithm that sorts numbers( or strings) by processing individual digits
- It sorts elements digit by digit, starting from the least significany digit(LSD) to the most significant digit (MSD)
- Time complexity O(K * n) // K is the maximum length of elements
```Java
import java.util.Arrays;

public class RadixSort {

    // A utility function to get the maximum value in an array
    private static int getMax(int[] array) {
        int max = array[0];
        for (int i = 1; i < array.length; i++) {
            if (array[i] > max) {
                max = array[i];
            }
        }
        return max;
    }

    // A function to perform counting sort on array based on a specific digit represented by exp
    private static void countingSort(int[] array, int exp) {
        int n = array.length;
        int[] output = new int[n]; // Output array to store sorted numbers temporarily
        int[] count = new int[10]; // Count array for each digit (0-9)

        // Initialize count array to 0
        Arrays.fill(count, 0);

        // Count the occurrences of each digit in the array
        for (int i = 0; i < n; i++) {
            int digit = (array[i] / exp) % 10;
            count[digit]++;
        }

        // Modify the count array such that each position contains the actual position of the digit in output[]
        for (int i = 1; i < 10; i++) {
            count[i] += count[i - 1];
        }

        // Build the output array
        for (int i = n - 1; i >= 0; i--) {
            int digit = (array[i] / exp) % 10;
            output[count[digit] - 1] = array[i];
            count[digit]--;
        }

        // Copy the sorted numbers back into the original array
        System.arraycopy(output, 0, array, 0, n);
    }

    // Main function to sort the array using radix sort
    public static void radixSort(int[] array) {
        // Get the maximum number to know the number of digits
        int max = getMax(array);

        // Perform counting sort for each digit, starting with the least significant digit (LSD)
        for (int exp = 1; max / exp > 0; exp *= 10) {
            countingSort(array, exp);
        }
    }

    public static void main(String[] args) {
        int[] array = {170, 45, 75, 90, 802, 24, 2, 66};
        System.out.println("Original Array: " + Arrays.toString(array));

        radixSort(array);

        System.out.println("Sorted Array: " + Arrays.toString(array));
    }
}

```