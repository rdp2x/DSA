A simple calculator program that runs in the terminal.
```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
        while (true) {  
            System.out.print("Enter the Operation: ");  
            char operator = sc.next().trim().charAt(0);  
  
            if (operator == 'A' || operator == 'S' || operator == 'M' || operator == 'D' || operator == 'a' || operator == 's' || operator == 'm' || operator == 'd') {  
  
                System.out.print("Enter Numbers: ");  
                int num1 = sc.nextInt();  
                int num2 = sc.nextInt();  
  
                if (operator == 'A' || operator == 'a')  
                    System.out.println(num1 + num2);  
                if (operator == 'S' || operator == 's')  
                    System.out.println(num1 - num2);  
                if (operator == 'M' || operator == 'm')  
                    System.out.println(num1 * num2);  
                if (operator == 'D' || operator == 'd')  
                    if (num2 > 0)  
                        System.out.println(num1 / num2);  
                    else  
                        System.out.println("Division by zero not possible");  
  
                System.out.println();  
  
            } else if (operator == 'X' || operator == 'x') {  
                System.out.println("The Program Ends");  
                break;  
            } else {  
                System.out.println("Invalid Input");  
            }  
        }  
    }  
}
```

This program uses the concept of infinite `while` loop, multiple `if` conditions, nested `if` and `else if` conditions and [[Logical Operators]] `||` 