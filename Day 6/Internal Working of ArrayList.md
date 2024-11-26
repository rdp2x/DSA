Originally, in ArrayList the size is fixed, but when the ArrayList fills to a particular size, a new ArrayList is created of double the size, and the elements from the old list are copied to the new ArrayList and the old one is deleted.

This follows a concept of Amortized Time Complexity

Multi-Dimensional ArrayList:
```Java
ArrayList<ArrayList<Integers>> demo = new ArrayList<>();

int num = 7;

// Initializtion of the ArrayList
for (int i = 0; i < 3; i++) {
	demo.add(new ArrayList());
}

// Add Elements
for (int i = 0; i < 3; i++) {
	for (int j = 0; j < 3;ge j++) {
		demo.get(i).add(num);
	}
}

System.out.println(demo);

// O/P: [[7,7,7], [7,7,7], [7,7,7]]
```
