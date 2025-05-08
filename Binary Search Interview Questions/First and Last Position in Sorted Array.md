> [! NOTE] Question
> Given an array of integers `nums` sorted in **ascending order**, find the starting and ending position of a given `target` value.
> If `target` is not found in the array, return `[-1, -1]`.

```Java
public class Main {  
    public static void main(String[] Args) {  
        int[] arr = {5, 7, 7, 8, 8, 10};  
        int target = 7;  
        System.out.println(position(arr, target));  
    }
      
    public static int[] position(int[] arr, int target) {  
        int[] ans = {-1, -1};  
        
        arr[0] = search(arr, target, true);
        
        if (arr[0] != -1)
	        arr[1] = search(arr, target, false);
        
        return ans;  
    }  
    
    public static int search(int[] arr, int target, boolean firstOccurrence) {  
        int ans = -1;  
        
        int start = 0;  
        int end = arr.length - 1;  
        
        while(start <= end) {  
            int mid = start + (end - start) / 2;  
            
            if (target < arr[mid])  
                end = mid - 1;  
            else if (target > arr[mid])  
                start = mid + 1;  
            else {  
                ans = mid;  
                if (firstOccurrence)  
                    end = mid - 1;  
                else  
                    start = mid + 1;  
            }  
        }  
        return ans;  
    }  
}
```

