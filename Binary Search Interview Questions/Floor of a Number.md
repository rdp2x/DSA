> [!NOTE] Question
> Find the floor number of the given target
> 
> (Floor Number is the number that is either **equals to the target** or the **greatest number smaller than the target**.)

```Java
public class Main {
	public static void main(String[] Args) {
		int[] arr;
		int target;
		System.out.println(floorNumber(arr, target));
	}
	
	public static int floorNumber(int[] arr, int target) {
		int start = 0;
		int end = arr.length - 1;
		
		if (target > end)
			return -1;
		
		while(start <= end) {
			int mid = (start + (end - start)) / 2;
			
			if (target > arr[mid]) {
				start = mid + 1;
			} else if (target < arr[mid]) {
				end = mid - 1;
			} else {
				return 0;
			}
		}
		return end;
	}
}
```