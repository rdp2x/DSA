Fibonacci series is a series that creates its next element from the sum of the previous two elements. The first two elements of the series are $0$ and $1$

_The Series goes like 0, 1, 1, 2, 3, 5, 8, 13.........._

```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
  
        int first = 0;  
        int second = 1;  
        int counterVariable = 2;  
  
        System.out.print("Enter the number of values required: ");  
        int input = sc.nextInt();  
  
        System.out.print("0, 1, ");  
        while (counterVariable != input) {  
            int temp = first;  
            first = second;  
            second = second + temp;  
            counterVariable++;  
            System.out.print(second + ", ");  
        }  
    }  
}
```

A concept of swapping is used here, as well as `while` loop as we don't know how many times the loop is going to run.