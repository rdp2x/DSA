Enhanced Switch is nothing but more neat and clean for of a switch case. It is generally used to make the code look more neat and formatted.

```syntax
switch (condition) {
	case -> // body
	case -> // body
	case -> // body
	case -> // body
	default -> //body
}
```

#### Display Day Name between 1 & 7

^d35971

Display what day it is according to the input
```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
  
        System.out.print("Enter the day: ");  
        int day = sc.nextInt();
  
        switch (day) {  
            case 1 -> System.out.println("Monday");  
            case 2 -> System.out.println("Tuesday");  
            case 3 -> System.out.println("Wednesday");  
            case 4 -> System.out.println("Thursday");  
            case 5 -> System.out.println("Friday");  
            case 6 -> System.out.println("Saturday");  
            case 7 -> System.out.println("Sunday");  
            default -> System.out.println("Only 7 days are there in a week");  
        }  
    }  
}
```

^8e05b0

#### Weekdays And Weekends

^0bae86

Display whether its a weekday or a weekend according to the input
```java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
  
        System.out.print("Enter the day: ");
        int day = sc.nextInt();
        switch (day) {
            case 1:
            case 2:
            case 4:
            case 3:
            case 5:
                System.out.println("Weekday");
                break;
            case 6:
            case 7:
                System.out.println("Weekend");
                break;
            default:
	            System.out.println("Only 7 days are there in a week");
        }  
    }  
}
```


