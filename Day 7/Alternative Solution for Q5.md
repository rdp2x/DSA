```Java
class HelloWorld {
    public static void main(String[] args) {
        int[] nums = {-12, 422, -8342, 91, 12, 5421};
        System.out.println(evenDigits(nums));
    }

    public static int evenDigits(int[] arr) {
        int count = 0;
        for(int i = 0; i < arr.length; i++) {
            if (digits(arr[i]) % 2 == 0)
                count++;
        }
        return count;
    }

    public static int digits(int element) {
        if (element < 0)
            element = element * -1;
        
        int count = 0;
        
        while (element > 0) {
            element = element / 10;
            count++;
        }
        return count;
    }    
}
```