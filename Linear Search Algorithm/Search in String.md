We can assume a [[String]] an array of characters.

```Java
public class Main {
	public static void main(String[] Args) {
		String sample = "Demo String";
		int target = 'o';
		
		System.out.println(stringSearch(sample, target));
		System.out.println(stringSearch2(sample, target));		
	}

	static boolean stringSearch(String str, int target) {
		if (str.length() == 0)
			return false;
			
		for (int i = 0; i < str.length(); i++) {
			if (target == str.charAt(i))
				return true;
		}
		return false;
	}

	static boolean stringSearch2(sample, target) {
		if (str.length() == 0)
			return false;
			
		for (char c = str.toCharArray()) {
			if (c == target)
				return true;
		}
		return false;
	}
}
```

>[!Note]
>The `toCharArary()` method converts a string into a character array. (We need an array in for-each loop).




