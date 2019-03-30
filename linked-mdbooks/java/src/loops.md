# Loops / Conditionals

- [if else](loops.md#if-else)
- [switch](loops.md#switch)
- [while](loops.md#while)
- [for](loops.md#)
- [for each](loops.md#for-each)
- [multiple loops: break](loops.md#break)


### **`if else`**
```java
if (condition == true) {
 	System.out.println("Do something...");
} else if (condition2 == true) {
	System.out.println("Do something else...");
} else {
	System.out.println("no condtition true!");
}
```

### **`switch`**
```java
// example input
int day = 5;

/* dont forget to BREAK after each statement! otherwise 
 * all the statements below will be executed as well!
 */ 
switch (day) {
	case 1: 
		System.out.println("monday");
		break;                                 // break after each case
	case 2: 
		System.out.println("tuesday");
		break;                                 // break after each case
	case 3:
		System.out.println("wednesday");
		break;                                 // break after each case
	case 4:
		System.out.println("thursday");
		break;                                 // break after each case
	case 5:
		System.out.println("friday");
		break;                                // break after each case
	case 6: case: 7                       // combine two cases
		System.out.println("weekend!");
		break;                                // break after each case
	// DEFAULT will be run when no case is chosen! (similar to else)
	default:
		System.out.println("illegal input!");
		// if default is last case no need to break
		// add BREAK only when default is not last!
}
```

### **`while`**
```java
boolean condition = true;
while (condition == true) {
	System.out.println("i will print this unless condition is met");
	if (Math.random()<0.1) {  // condition will be met with 10% probability
		condition = false;
	}
}
```

### **`for`**
```java
for (int i=0; i<=10; i++) {     // increment +1 each round
	System.out.println("current run: " + i);
}
```

```java
for (int i=0; i<=10; i+=2) {    // increment +2 each round
	System.out.println("current run: " + i);
}
```

```java
for (int i=100; i>=0; i-=10) {  // decrement +10 each round
	System.out.println("current run: " + i);
}
```

### **`for each`**
```java
// int[]
int[] zahlen = {1,4,7,2};
for (int zahl : zahlen) {
	System.out.println(zahl);
}
```

```java
// possible also for other more complex datatypes like HashMap, ArrayList or Objects!
ArrayList<String> arrListStr = new ArrayList<String>();
arrListStr.add("first string");
arrListStr.add("second string");
arrListStr.add("third string");
for (String s : arrListStr) {
	System.out.println(zahl);
}
```

### **`break`**
```java
// Loop1 is a label for the first loop
Loop1: 
for (;;) {  // for (;;){} is an endless loop, same as while(true)
	for (;;) {
		statement; 
		if (condition) { 
			 break Loop1;
		}
	}
}
```