> [!NOTE] Question
> Search for an element in a mountain array.

```Java
public class Main {  
    public static void main(String[] Args) {  
        int[] arr = {0, 2, 5, 6, 4, 1};
        int target = 4;
	}
	
	public static int search(int[] arr, int target) {
        int peak = peakElement(arr);
        int firstTry = binarySearch(arr, target, 0, peak);
        if (firstTry != -1)
	        return firstTry;
		
		return binarySearch(arr, target, peak + 1, arr.length - 1);
	}
	
    public static int peakElement(int[] arr) {  
        int start = 0;  
        int end = arr.length - 1;  
        
        while (start < end) {  
            int mid = start + (end - start) / 2;  
            
            if(arr[mid] > arr[mid + 1])  
                end  = mid;  
            else  
                start = mid + 1;  
        }  
        return arr[start];  
    }
    
	public static int binarySearch(int[] arr, int target, int start, int end) {
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