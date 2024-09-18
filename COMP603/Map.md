Map
- Represents a mapping between a key and value
- Is an interface

Uses
- Perform lookups by keys or when someone wants to retrieve and update elements by keys
	  - A map of error codes and their descriptions
	  - A map of zip codes and cities
	  - A map of managers and employees. Each manager (key) is associated with a list of employees (values)
	  - A map of classes and students. Each class (key) is associated with a list of students (value)

Characteristics
- Cannot contain duplicate keys and each key can map to at most one value. Some implementations allow null keys and null values like [[HashMap]] and [[LinkedHashMap]], but not [[TreeMap]]
- Order of a map depends on the specific implementation. [[TreeMap]] and [[LinkedHashMap]] have predictable order, but not [[HashMap]]
- 
