> [!NOTE] Question
> Assuming the Matrix is already sorted both row-wise and column-wise
> $$ \begin{bmatrix} 10, &20, &30, &40, \\ 15, &25, &35, &45, \\ 28, &29, &37, &49, \\ 33, &34, &38, &50 \end{bmatrix} $$
> 

```Java
public class Main {
	public static void main (String args[]) {
		int[][] arr = {
			{10, 20, 30, 40},
			{15, 25, 35, 45},
			{28, 29, 37, 49},
			{33, 34, 38, 50}
		};
		
		int target = 37;
		int ans = Arrays.toString(bs2d(arr, target));
	}
	
	public static int[] bs2d(int[][] arr, int target) {
		int row = 0;
		int column = arr.length- 1;
		
		while (row < arr.length && column >= target) {
			if (arr[row][column] == target)
				return new int[][]{row, column};
			
			if (arr[row][column] < target)
				row++;
			else
				column++;
		}
		
		return new int[]{-1, -1};
	}
}
```