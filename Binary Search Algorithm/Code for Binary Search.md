```Java
public class Main {
	public static void main(String[] Args) {
		int[] arr;
		int target;
		System.out.println(binarySearch(arr, target));
	}
	
	public static int binarySearch(int[] arr, int target) {
		int start = 0;
		int end = arr.length - 1;
		
		while(start <= end) {
			int mid = start + (end - start) / 2;
			
			if (target > arr[mid]) {
				start = mid + 1;
			} else if (target < arr[mid]) {
				end = mid - 1;
			} else {
				return 0;
			}
		}
		return -1;
	}
}
```

> [!NOTE] Formula Change
> Sometime, while getting the value for middle element, the value in it can exceed the `MAX_INTEGER` size in java.
> 
> So instead of using the formula:
> $$\frac{Start + End}{2}$$ 
> 
> We use this formula:
> $$\frac{Start + (End - Start)}{2}$$ 

