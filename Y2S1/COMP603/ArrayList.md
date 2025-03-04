ArrayList
- Used in programs where lots of manipulation in the array is needed
- Is a Java implemented using the [[LinkedLists]] 
- Does not have a fixed size (automatically changes)
- Can only hold object, cannot hold primitives (but can use it's wrapper class)

![[Pasted image 20240727200532.png]]

```Java
///Imports used
import java.util.ArrayList;
```

```Java
ArrayList<String> friendsArrayList = new ArrayList<>();

//This is a inremovable list (cannot be changed)
ArrayList<String> friendsArrayList2 = new ArrayList<>(Arrays.aslist("John", "Chris", "Eric", "Luke"));

//To retrieve data from ArrayList
//Use .get method
System.out.println(friendsArrayList2.get(1));

//To get the length
//Use .size method
System.out.println(friendsArrayList2.size());

//To add element
//Use .add method
System.out.println(friendsArrayList2.add("Mitch"));
```



