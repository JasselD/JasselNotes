- Iterate through a collection one element at a time
- Time complexity: O(n)
- Disadvantages:
	- Slow for large data sets
- Advantage:
	- Fast for searches of small to medium data sets
	- Does not need to be sorted
	- Useful for data structure that does not have random access (Linkedlist)

```Java
private static int linearSearch(int[] array, int value) {
	for(int i = 0; i < array.length; i++) {
		if(array[i] == value) {
			return i;
		}
	}

	return -1;
}
```