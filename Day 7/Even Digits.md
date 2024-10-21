**[LeetCode Problem](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/) -** Given an array `nums` of integers, return how many of them contains even number of digits.

```Java
public class Main {
    public static void main(String[] args) {
        int[] nums = {-12, 422, -8342, 91};
        System.out.println(sample(nums));
    }
    
    public static int sample(int[] arr) {
        int count = 0;
        for(int i = 0; i < arr.length; i++) {
            
            if (arr[i] < 0)
                arr[i] = arr[i] * -1;
            
            String temp = String.valueOf(arr[i]);
            
            if (temp.length() % 2 == 0)
                count++;
        }
        return count;
    }
    
}
```