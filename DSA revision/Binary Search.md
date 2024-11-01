- Search algorithm that finds the position of the target value within a sorted array 
- Efficient in large data set  
- Basic binary search using arrays
```Java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        
        int array[] = new int[100];
        int target = 42;
        
        for(int i = 0; i < array.length; i++) {
            array[i] = i;
        }
        
        int index = Arrays.binarySearch(array, target);
        
        if(index == -1) {
            System.out.println(target + " not found");
        } else{
            System.out.println("Element found at: " + index);
        }
    }
}
```
- Basic binary se
