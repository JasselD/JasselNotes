[[COMP603/Array|Array]]
- Collection of (box) data elements of specified type
- All data holding partitions have contiguous memory locations
- Each partition has two neighbours except first and second
- Size of array is fixed (cannot be modified)
- Being adjacent each partition is indexed and can be determined by its position
- Index start at 0 
- One dimensional array ends at (length - 1)

**Declaration of an Array
```Java
	dataType arrayName[];
	dataType[] arrayName;

	//Example
	int myArray[];
	int[] myArray; //most preferred
```

**Initialisation of Array
- Gives memory to array elements
- One dimensional array can be initialised via
```Java
	arrayName = new dataType[size];

	//Example
	myArray = new int[5];s
```

**Adding or Updating the array
```Java
public void arrayDemo() {
	int[] myArray = new int[5];
	myArray[0] = 5;
	myArray[1] = 1;
	myArray[2] = 8;
	myArray[3] = 2;
	myArray[4] = 10;
	myArray[2] = 9; //This will replace the previous myArray[2]
	myArray[5] = 7; //Exception will appear because this array does not exist
}
```

**How to print elements in an Array
```Java
public void printArray(int[] arr) {
	int n = arr.length;
	for(int i = 0; i < n; i++) {
		System.out.println(arr[i] + " ");
	}
	System.out.println();
}
```

 **Remove Even Integers from an Array

Example -
	Input: arr = {3, 2, 4, 7, 10, 6, 5}
	 Output: arr = {3, 7, 5}

 ```Java
 int[] removeEven(int[] arr) {
	int oddCount = 0;
	for(int i = 0; i < arr.length; i++) {
		if(arr[i] % 2 != 0) {
			oddCount++;
		}
	}
	int[] result = new int[oddCount]; // result array will have 3 arrays
	int idx = 0;
	for(int i = 0; i < arr.length; i++) {
		if(arr[i] % 2 != 0) {
			result[idx] = arr[i];
			idx++;
		}
	}
	return result;
 }
```

skibidi
