- Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in the wrong order
- Suitable for small data sets
- O(n²) complexity
- Image a tank with water, light (small element) will float while the heavy (big element) will sink

```Java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int array[] = {9, 1, 8, 3, 2, 4, 5, 6, 7};
        
        bubblesort(array);
        
        for(int i : array) {
            System.out.println(i);
        }
    }
    
    public static void bubblesort(int array[]) {
        
        for(int i = 0; i < array.length - 1; i++) {
            for(int j = 0; j < array.length - i - 1; j++) {
                if(array[j] > array[j+1]) {
                    int temp = array[j];
                    array[j] = array[j+1];
                    array[j+1] = temp;
                }
            }
        }
    }
}
```

