- Loop is when something is being repeated again & again.
- It is generally used when something is to be used repeatedly.
- There 2 types of loops:
	- [[#Entry Control Loops]]
	- [[#Exit Control Loops]]
## Entry Control Loops
- This loop always tests the condition before entering into the loop.
- You can think of it like a watchman asking a guy before entering the room.
#### For Loop
- It contains a loop called `for` loop.
- The syntax of for loop is:
```
for (initialization; conditions; increment/decrement) {
	// body
}
```
- We use `for` loop when we know how many times the loops is going to run.
###### Example Snippets
1. Program to print number from 1 to 10.
```java
for (int i = 1; i <= 10; i++) {
	System.out.println(i);
}
```

2. Program to print a name specific number of times.
```java
String name = sc.next();

for (int i = 1; i <= 10; i++) {
	System.out.println(name);
}
```

## Exit Control Loops
- Loops that executes atleast once and then check the condition at the end of the loop body.
- These loops contain `while` and `do while` loops.
#### While Loop
- While loop is usually used to maintain the cleanliness of the code.
- The initialization part is done in the beginning and the increment/decrement part is done inside the loop body and the end of the loop.
- The Syntax is:
```
// initialization
while (condition) {
	// body with increment/decrement	
}
```
#### Do while loop
- `do while` loop is much similar to while loop instead it check the condition later after the completion of the first execution of the loop.
- The Syntax is:
```
// initialization
do {
	// body with increment/decrement
} while (condition T/F)
```
#### Example Snippets (Print Numbers 1 - 10)
###### while loop
```java
int i = 1;
while (i <= 10) {
	System.out.println(i);
	i++;
}
```
###### do while loop
```java
int i = 1;
do {
	System.out.println(i);
	i++;
} while (i <= 10)
```