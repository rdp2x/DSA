Reverse the input number

```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
        int input = sc.nextInt();  
        int NewNum = 0;  
  
        while (input > 0) {  
            NewNum = NewNum * 10;  
            NewNum = (NewNum + (input % 10));  
            input = input / 10;  
        }  
        System.out.println("Reversed: " + NewNum);  
    }  
}
```

A simple logic is used here, if a number is divided by 10 it gives its last digit as *remainder* and previous all digits as *quotient*.