- Create classes that work with different data types
- An entity such as a class, interface, or method that operates on a parameterised type is a generic entity
```Java
public class Printer<T> {
	T thingToPrint;

	public Printer(T thingToPrint) {
		this.thingToPrint = thingToPrint;
	}

	public void print
}
```