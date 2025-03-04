- Definition: Selection Sort algorithm sorts an array by repeatedly finding the minimum element (considering ascending order) from the unsorted part and putting it at the beginning
- O(n²) complexity
- Selecting the smallest value
- In every iteration of the selection sort, the minimum element form the unsorted subarray is picked and moved to the sorted subarray

```Java
public static void main(String[] arguments) {
	int arr[] = {64, 25, 12, 22, 11}
	int length = arr.length;

	for(int i=0; i<length-1; i++) {
		int min_index = i;
		for(int j=i+1; j<length; j++) {
			if(arr[min_index] > arr[j]) {
				min_index = j;
			}
		}
		int temp = arr[min_index]
		arr[min_index] = arr[i];
		arr[i] = temp;
	}
}
```

