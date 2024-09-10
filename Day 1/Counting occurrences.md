Given a number, count the given digit occurred in input
```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  

        System.out.print("Enter the Number: ");
        int input = sc.nextInt();
        
        System.out.print("Enter the digit to search: ");
        int find = sc.nextInt();
        
        int counter = 0;  

        while (input > 0) {  
            if (input % 10 == find) {  
                counter++;  
            }  
            input = input / 10;  
        }  
        System.out.println("Occured: " + counter);  
    }  
}
```
