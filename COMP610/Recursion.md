- A method that calls itself

```Java
public class Recursion {
	public static void main(String[] args) {
		sayHi();
	}
}

private static void sayHi() {
	System.out.println("Hi!");

	sayHi(); //This will cause stack overflow, need an exit strategy
}
}
```

**Stack overflow
- A type of buffer overflow error that occurs when a computer program tries to use more memory space in the call stack than has been allocated to that stack

Fixed method
```Java
public class Recursion {
	public static void main(String[] args) {
		sayHi(3);
	}
}

private static void sayHi() {
	System.out.println("Hi!");

	if(count <= 1) {
		return;
	}
	sayHi(count - 1);
}
}
```

