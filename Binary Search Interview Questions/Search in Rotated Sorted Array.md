> [!NOTE] Question
> There is an integer array `nums` sorted in ascending order (with **distinct** values).
> 
> Prior to being passed to your function, `nums` is **rotated** at an unknown pivot index `k (0 <= k nums.length)` such that the resulting array is `[nums[k], nums[k+1], ..., nums[n-1], nums[0], nums[1], ...,  nums[k-1]]` (**0- indexed**). For example, `[0,1,2,4,5,6,7]` might be rotated at pivot index `3` and become `[4,5,6,7,0,1,2]`.
> 
> Given the array `nums` **after** the rotation and an integer `target`, return the *index* of `target` if it is in `nums`, or `-1` if it is not in `nums`.

```Java
public class Main {
	public static void main(String[] args) {
	
	}
	
	public static int search(int[] arr, int target) {
		int pivot = findPivot(arr);
		
		if (pivot == -1)
			binarySearch(arr, target, 0, arr.length - 1);
		
		if (arr[pivot] == target)
			return pivot;
		
		if (target >= arr[0])
			return binarySearch(arr, target, 0, pivot - 1);
		
		return binarySearch(arr, target, pivot + 1, arr.length - 1);
	}
	
	public static int binarySearch(int[] arr, int target, int start, int end) {
		while (start <= end) {
			int mid = (start + (end - start)) / 2;
			
			if (target > arr[mid])
				start = mid + 1;
			else if (target < arr[mid])
				end = mid - 1;
			else
				return mid;
		}
		return -1;
	}
	
	public static int findPivot(int[] arr) {
		int start = 0;
		int end = arr.length - 1;
		
		while (start <= end) {
			int mid = start + (end - start) / 2;
			
			if (mid < end && arr[mid] > arr[mid + 1])
				return mid;
			if (mid > start && arr[mid] < arr[mid - 1])
				return mid - 1;
			
			if (arr[mid] <= arr[start])
				mid = end - 1;
			else
				start = mid + 1;
		}
		return -1;
	}
}
```

