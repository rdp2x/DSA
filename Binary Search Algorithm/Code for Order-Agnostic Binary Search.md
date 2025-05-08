```Java
public class Main {
	public static void main(String[] Args) {
		int[] arr1 = {-18, -12, -4, 0, 2, 3, 4, 15, 16, 18, 22, 45, 89};
		int[] arr2 = {89, 45, 22, 18, 16, 15, 4, 3, 2, 0, -4, -12, -18};
		int target = 18;
		System.out.println(binarySearch(arr1, target));
	}
	
	public static int binarySearch(int[] arr, int target) {
		int start = 0;
		int end = arr.length - 1;
		
		boolean isAscn = arr[start] < arr[end];
		
		while(start <= end) {
			int mid = start + (end - start) / 2;
			
			if (arr[mid] == target)
                return mid;
			
			if (isAscn) {
			    if (target < arr[mid])
                    end = mid - 1;
                else
                    start = mid + 1;
			} else {
			    if (target > arr[mid])
                    end = mid - 1;
                else
                    start = mid + 1;
			}
		}
		return -1;
	}
}
```