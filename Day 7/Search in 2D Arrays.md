```Java
import java.util.Arrays;

public class Main {
	public static void main(String[] Args) {
		int[][] arr= {
				{17, 28, 98},
				{42, 73, 61, 65},
				{23, 99}
		};
		
		int target = 23;
		
		System.out.println(Arrays.toString(multiSearch(arr, target)));
	}

	static int[] multiSearch(int[][] arr, int target) {
		for (int i = 0; i < arr.length; i++) {
			for (int j = 0; j < arr[i].length; j++) {
				if (arr[i][j] == target) {
					return new int[]{i, j};
				}
			}
		}
		return new int[]{-1, -1};
	}
}
```