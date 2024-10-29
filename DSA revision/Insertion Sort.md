- Insertion Sort is a simple sorting algorithm that works similar to the way you sort playing cards in your hands. The array is virtually split into a sorted and an unsorted part
- Values from the unsorted part are picked and placed at the correct position in the sorted part
- O(n²) complexity

```Java
public static void main(String[] arguments) {
	int arr[] = {64, 25, 12, 22, 11, 57, 37, 21};
	int length = arr.length;
        
        System.out.print("Unsorted array\n");
        for(int i = 0; i < length; i++) {
            System.out.print(arr[i] + " ");
        }
        
        for(int i = 1; i < length; i++){ //i is pointed at 
             int key = arr[i];
             int j = i - 1;
             
             while(j >= 0 && arr[j] > key) {
                 arr[j+1] = arr[j];
                 j = j - 1;
             }
             arr[j+1] = key;
        }
        
        System.out.print("\nSorted array\n");
        for(int i = 0; i < length; i++) {
            System.out.print(arr[i] + " ");
        }
        
    }
```