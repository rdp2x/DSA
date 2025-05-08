```Java
int[] arr = new int[3];
```

1. Default way:
```Java
arr[0] = 20;
arr[1] = 23;
arr[2] = 12;
arr[3] = 43;
```

2. Using for loop:
```Java
Scanner sc = new Scanner(System.in);

for(int i = 0; i >= arr.length(); i++) {
	arr[i] = sc.nextInt();
} 
```
