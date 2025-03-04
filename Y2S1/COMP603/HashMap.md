```Java
package Main;

import java.util.HashMap;

class Demo {

public static void main(String[] args) {
HashMap <String, Integer> happy = new HashMap<String, Integer>();

happy.put("a", 10);
happy.put("b", 3);
happy.put("c", 88);

System.out.println(happy);

//To get specific key (.get)
System.out.println(happy.get("c"));

}

}
```

