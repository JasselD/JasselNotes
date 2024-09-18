**AbstractSet**
- part of the Java Collection Framework which implements the **Collection interface** and extends **AbstractCollection** class

![[Pasted image 20240801151817.png]]

**Syntax Declaration**

```Java
public abstract class AbstractSet<E>
extends AbstractCollection<E>
implements Set<E>
//Where E is the type of elements maintained by this Set
```

**Characteristics of abstract set** :
- Implements the Set interface
	  provides a standard set of methods to manipulate sets
	  
- Implements some set methods
	 size(), isEmpty(), contain(), and remove()
	 
- Supports iterator
	 provides an iterator method that returns an Iterator over the elements in the set
	 
- Does not implement all set methods
	 methods that are implemented include add(), addAll(), and clear(). These methods must be implemented by subclasses of AbstractSet
	 
- Provides default implementations
	 provides default implementations for some methods of the Set interface
	 
- Supports null elements
	 allows null elements to be added in set
	 
- Unordered
	 order in which elements are added to the set is not preserved
	 
- Thread-unsafe
	 multiple thread access the same set simultaneously can lead to data inconsistencies. If thread safety is required, a synchronised set or a concurrent set can be used

![[Screenshot 2024-08-01 at 3.33.53 PM.png]]

**size() method**
- should simply return the number of elements in the set NOT how big the array is

**clear() method**
- reset the number of elements to 0. This could suffice as new additions to the set would simply override the old values
- another alternative is to re-instantiate the array

**expandCapacity() method**
- if numElements >= elements.length, we need to expand the capacity of the underlying array and copy all the elements before we add new elements
- 