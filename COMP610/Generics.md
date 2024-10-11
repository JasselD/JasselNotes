- Create classes that work with different data types
- An entity such as a class, interface, or method that operates on a parameterised type is a generic entity
- <mark style="background: #ABF7F7A6;">Does not work with generic types (can use wrapper type)</mark>
```Java
public class Printer<T> {
	T thingToPrint;

	public Printer(T thingToPrint) {
		this.thingToPrint = thingToPrint;
	}

	public void print() {
		System.out.println(thingToPrint);
	}
}

public class Generics{

	public static void main(String[] args) {

		Printer<Integer> printer = new Printer<>(23);
		printer.print();

		Printer<Double> doubleprinter = new Printer<>(33.5);

		doubleprinter.print();
	}
}
```
