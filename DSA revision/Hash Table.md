- A table of elements (array) where each element is stored at an index that is calculated based on its hash code
- Perfect hashing
	- Hash code is distinct for all objects of a class
	- If two different objects have the same hash code then there has been a collision
- Disadvantage
	- If array gets full and need to expand capacity, you will need to copy all the elements over to the new array and recalculate all the hash codes
- ![[Pasted image 20241104154724.png]]

**Chaining
- Maintain a table of singly linked lists. Elements that collide are just put into the linked list. Since order is not important, newer elements get put at the beginning of linked list

**Overflow Area
- Elements that collide are placed into an overflow area with a link from the element that alrea