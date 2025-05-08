Shadowing is when a variable is declared outside of a class and changed its value inside a variable.

Means when a variable is defined in a block for example, and later if its value is changes inside another sub-block that is in the same block, the value overlaps/changes.

```java
import java.util.*;

public class Main {
	int a = 10;
	public static void main(String[] Args) {
		System.out.println(a); // 10
		a = 20;
		System.out.println(a); // 20
	}
}
```