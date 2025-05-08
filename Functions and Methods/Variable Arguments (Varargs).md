%%  %%Variable arguments is when we don't know how many arguments the user is going to give.
For this situation we use `...variableName` in the arguments.

```java
import java.util.Arrays;  
  
public class Main {  
    public static void main(String[] Args) {  
        System.out.println("This is an example of VarArgs: ");  
        sample(1, 2, 3, 4, 5);  
        sample(1, 2);  
    }  
  
    static void sample(int ...nums) {  
        System.out.println(Arrays.toString(nums));  
    }  
}
```

> [!NOTE]
> - The Variable Argument converts all the given values in an  array.
> - To print it, we need to convert the array to String format using `.toString()` method.

