An object that can be used to loop through collections, like [[Y2S1/COMP603/Array]] and HashSet

**Getting an Iterator**
iterator() method can be used to get Iterator for any collection

```Java
package Main;

  

import java.util.ArrayList;
import java.util.Iterator;

class Demo {

public static void main(String[] args) {

//Make a collection
ArrayList<String> cars = new ArrayList<String>();
cars.add("Volve");
cars.add("BMW");
cars.add("Ford");
cars.add("Mazda");

//Get the iterator
Iterator<String> it = cars.iterator();

while(it.hasNext()) {

System.out.println(it.next());

}

}

}
```

3 popular methods in iterator
- next()
- hasNext()
- remove()

