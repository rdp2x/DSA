**Question -** Search for the element $n$ in the range of an index $a, b$

```Java
public class Main {
	public static void main(String[] Args) {
		int[] sample = {56, 24, 72, 12, 83, 42, 94, 61, 30, 33};
		int target = 12;
		
		System.out.println(searchInRange(sample, target, 2, 6));
	}

	static int linearSearch(int[] arr, int target) {
		if (arr.length == 0)
			return -1;
			
		for (int i = start; i <= end; i++) {
			if (i == target)
				return i;
		}
		return -1;
	}
}
```