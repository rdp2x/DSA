> [!NOTE] Question
> Given a characters array `letters` that is sorted in **non-decreasing** order and a character `target`, return the smallest character in the array that is larger than `target`.
> 
> Also the letters wraps around: 
> For example, if `target == z`  and `letters == [a, b]`, answer is 'a'.

```Java
public class Main {
	public static void main(String[] Args) {
		char[] arr = {'c', 'f', 'j'};
		int target = 'j';
		System.out.println(smallestLetter(arr, target));
	}
	
	public static char smallestLetter(char[] arr, int target) {
		int start = 0;
		int end = arr.length - 1;
		
		while(start <= end) {
			int mid = (start + (end - start)) / 2;
			
			if (target > arr[mid])
				start = mid + 1;
			else
				end = mid - 1;
		}
		return arr[start % arr.length];
	}
}
```