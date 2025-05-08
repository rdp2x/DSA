A switch case that describes the fruit.
```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
  
        System.out.print("Enter a Fruit: ");  
        String fruit = sc.next();  
  
        switch (fruit) {  
            case ("Mango"):  
                System.out.println("King of Fruits");  
                break;  
            case ("Grape"):  
                System.out.println("Small Fruit");  
                break;  
            case ("Banana"):  
                System.out.println("Sus Fruit");  
                break;  
            case ("Watermelon"):  
                System.out.println("Large Seedy Fruit");  
                break;  
            default:  
                System.out.println("That's not a Fruit!!");  
        } 
    }  
}
```