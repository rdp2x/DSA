**[LeetCode Problem](https://leetcode.com/problems/richest-customer-wealth/description/) -** You are given an `m x n` integer grid `accounts` where `accounts[i][j]` is the amount of money the `i​​​​​​​​​​​th​​​​` customer has in the `j​​​​​​​​​​​th`​​​​ bank. Return the **wealth** that the richest customer has.

A customer's **wealth** is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum **wealth**.

```Java
public class Main {
    public static void main(String[] Args) {
        int[][] nums = {
            {1, 2, 6},
            {1, 4, 5},
            {1, 8, 5}
        };
        
        wealth(nums);
    }
	
    static void wealth(int[][] arr) {
        int max = 0;
        
        for (int i = 0; i < arr.length; i++) {
            int sum = 0;
            for (int j = 0; j < arr[i].length; j++) {
                sum = sum + arr[i][j];
            }
            
            if (sum > max)
                max = sum;
            
        }
        
        System.out.println(max);    
    }
}
```