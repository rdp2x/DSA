In java, there's nothing like pass by reference. There is only pass by value. So when a variable is passed a method as argument, the original value is not passed, a copy of the reference variable is passed. Means another reference variable that is pointing to the same object is passed. This is the reason, why values altered in another method does not change. So when an alteration is made in the new reference variable, it points to the new object, whereas the pervious reference variable still points to the same old object.

This is the case in [[Primitive Data Types in Java |Non-Primitives]]

```java
import java.util.Arrays;  
  
public class Main {  
    public static void main(String[] Args) {  
		String name = "Meet";
		change(name);
		System.out.println(name); // Meet
    }  
  
    static void change(String name) {  
        naam = Preet; // does not change the obj, it creates a new obj
    }
}
```