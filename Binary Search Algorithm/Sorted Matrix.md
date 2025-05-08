> [!NOTE] Question
> Given a 2D array that is sorted:
> $$ \begin{bmatrix} 1, &2, &3, &4, \\ 5, &6, &7, &8, \\ 9, &10, &11, &12, \\ 13, &14, &15, &16 \end{bmatrix} $$

```Java
public class Main {
	public static void main(String[] args) {
		int[][] arr = {
			{1, 2, 3, 4},
			{5, 6, 7, 8},
			{9, 10, 11, 12},
			{13, 14, 15, 16}
		};
		
		int target = 7;
		
		String ans = Arrays.toString(sortedBS(arr, target));
		System.out.println(ans);
	}
	
	public static int[] sortedBS(int[][] arr, int target) {
		int row = arr.length;
		int column = arr[0].length;
		
		while (row < arr)
	}
}
```