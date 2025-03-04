- Sorting algorithm bins/buckets are created to put elements into them
- Time complexity O(n + K) // K is the number of bins/buckets
```Java
import java.util.*;

public class BucketSort {

    public static void bucketSort(float[] array, int n) {
        if (n <= 0)
            return;

        // Create n empty buckets
        @SuppressWarnings("unchecked")
        List<Float>[] buckets = new ArrayList[n];

        for (int i = 0; i < n; i++) {
            buckets[i] = new ArrayList<>();
        }

        // Put array elements in different buckets based on their values
        for (int i = 0; i < n; i++) {
            int bucketIndex = (int) array[i] * n; // Multiply by n to determine the bucket
            buckets[bucketIndex].add(array[i]);
        }

        // Sort individual buckets using a sorting algorithm (like insertion sort)
        for (int i = 0; i < n; i++) {
            Collections.sort(buckets[i]);
        }

        // Concatenate all buckets into the original array
        int index = 0;
        for (int i = 0; i < n; i++) {
            for (float value : buckets[i]) {
                array[index++] = value;
            }
        }
    }

    public static void main(String[] args) {
        float[] array = {0.78f, 0.17f, 0.39f, 0.26f, 0.72f, 0.94f, 0.21f, 0.12f, 0.23f, 0.68f};
        System.out.println("Original Array: " + Arrays.toString(array));

        bucketSort(array, array.length);

        System.out.println("Sorted Array: " + Arrays.toString(array));
    }
}

```