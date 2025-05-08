**Question -** Search for the minimum element in the array.

```Java
public class Main {
	public static void main(String[] Args) {
		int[] sample = {56, 24, 72, 12, 83, 42, 94, 61, 30, 33};
		
		minSearch(sample);
	}
}

static int minSearch(int[] arr) {
		if (arr.length == 0)
			return -1;
			
		int min = arr[0];
			
		for (int i = 0; i < arr.length; i++) {
			if (arr[i] < min)
				min = arr[i];
		}
		return min;
	}
```
