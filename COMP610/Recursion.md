- A method that calls itself

```Java
public class Recursion {
	public static void main(String[] args) {
		sayHi();
	}
}

private static void sayHi() {
	System.out.println("Hi!");

	sayHi();
}
```

**Stack overflow
- A type of buffer overflow error that occurs when a computer program tries to use more memory space in the call stack than