Using `for` loop:
```Java
public class Main {
	public static void main(String[] Args) {
		int[] sample = {56, 24, 72, 12, 83};
		int target = 12;
		
		System.out.println(linearSearch(sample, target));
	}

	static int linearSearch(int[] arr, int target) {
		if (arr.length == 0)
			return -1;
			
		for (int i = 0; i < arr.length; i++) {
			if (i == target)
				return i;
		}
		return -1;
	}
}
```

Using `for each` loop:
```Java
public class Main {
	public static void main(String[] Args) {
		int[] sample = {56, 24, 72, 12, 83};
		int target = 12;
		
		System.out.println(linearSearch(sample, target));
	}

	static boolean linearSearch(int[] arr, int target) {
		if (arr.length == 0)
			return false;
			
		for element : arr {
			if (element == target)
				return true;
		}
		return false;
	}
}
```
