Check if the input alphabet is in uppercase or lowercase.

```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner input = new Scanner(System.in);  
  
        System.out.print("Enter an Alphabet: ");  
        char ch = input.next().trim().charAt(0);  
  
        if (ch < 'z' && ch > 'a') {  
            System.out.println("Lowercase Letter");  
        } else {  
            System.out.println("UpperCase Letter");  
        }  
  
    }  
}
```

> [!NOTE]
> This java code uses the concept of Ternary Operator and ASCII Value. Also to get an input of only a single character, we used method chaining. The methods `input.next()`, `trim()`, and `charAt(index)` are used.
> 
> `trim()` - Removes the spaces around the input text.
> `charAt(index)` - Iterates through the String and prints the character present at given index.