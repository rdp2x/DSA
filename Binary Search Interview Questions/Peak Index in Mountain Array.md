> [!NOTE] Question
> A mountain array is something like when it contains element in ascending and then descending order. Eg. `arr = [0, 2, 5, 6, 4, 1]`.
> Find the **peak/highest** element of the array.

```Java
public class Main {  
    public static void main(String[] Args) {  
        int[] arr = {0, 2, 5, 6, 4, 1};  
        int ans = peakElement(arr);  
        System.out.println(ans);  
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
}
```