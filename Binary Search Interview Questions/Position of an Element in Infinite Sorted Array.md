> [!NOTE] Question
> Find the position of an element in a sorted array of infinite numbers
> (This is basically simple binary search without using the `arr.length` function.)

```Java
public class Main {
	public static void main(String[] Args) {
		int[] arr = {2, 3, 4, 7, 8, 12, 13, 14, 16, 18, 21, 22, 25, 29, 32};
		int target = 13;
		System.out.println(infiniteArray(arr, target));
	}
	
	public static int range(int[] arr, int target) {
		int start = 0;
		int end = 1;
		
		while (target > end) {
			int newStart = end + 1;
			end = end + (end - start + 1) * 2;
			start = newStart;
		}
		
		return infiniteArray(arr, target, start, end);
	}
	
	public static int infiniteArray(int[] arr, int target, int start, int end) {
		while (start <= end) {
			int mid = start + (end - start) / 2;
			
			if (target < mid)
				end = mid - 1;
			else if (target > mid) 
				start = mid + 1;
			else
				return mid;
		}
		return -1;
	}
}
```
