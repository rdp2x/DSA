Find the largest number among all the number that are given in input (_Three Inputs_)

```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the Numbers: ");  
        int num1 = sc.nextInt();  
        int num2 = sc.nextInt();  
        int num3 = sc.nextInt();  
        int max = num1;  
  
        if (num2 > max) {
            max = num2;  
        } if (num3 > max) {
            max = num3;  
        }
		
		// Using the built-in method
		max = Math.max(num3, Math.max(num2, num1));
		
        System.out.println("The largest number is " + max);  
    }  
}
```

> [!NOTE]
> `Math.max` method is a built-in method of Java that automatically returns the largest of the 2 inputs given as arguments.