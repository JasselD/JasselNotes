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
        
        for(int i = 1; i < length; i++){ //i is pointed at element 25
             int key = arr[i]; // key = element 25
             int j = i - 1; // j is arr[0]
             
             while(j >= 0 && arr[j] > key) { // if j (arr[0]) > 0)
                 arr[j+1] = arr[j]; // arr[1] will become element 64
                 j = j - 1; // arr[0] will -1 so arr[-1], will end the loop
             }
             arr[j+1] = key; // arr[0] will become element 25
        }
        
        System.out.print("\nSorted array\n");
        for(int i = 0; i < length; i++) {
            System.out.print(arr[i] + " ");
        }
        
    }
```