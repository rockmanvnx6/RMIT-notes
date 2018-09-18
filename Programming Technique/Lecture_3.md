# Lecture 3

## Switch

```java
int month = 8;
String monthString;
switch (month) {
    case 1: monthString = "January";
        break;
    case 2: monthString = "February";
        break;
    case 3: monthString = "March";
        break;
    case 4: monthString = "April";
        break;
    case 5: monthString = "May";
        break;
    case 6: monthString = "June";
        break;
    case 7: monthString = "July";
        break;
    case 8: monthString = "August";
        break;
    case 9: monthString = "September";
        break;
    case 10: monthString = "October";
        break;
    case 11: monthString = "November";
        break;
    case 12: monthString = "December";
        break;
    default: monthString = "Invalid month";
        break;
}
```

- remember to `break` at any case. 
- `default`case is like `else`.
- Switch works with String, char and int, double, long...

## String comparisons - check String.md

![image-20180808112241224](image-20180808112241224.png)

## Exit method

`System.exit(0)` - kill the program

```java
if (numberOfWinners == 0) {
    System.out.println ("Error: Dividing by zero.");
    System.exit(0); //kill the program }
else {
    oneShare = prizePool / numberOfWinners; System.out.println ("Each winner will receive $" +
    oneShare);
}
```

## Array

### int[] array

```java
int[] anArray;
anArray = new int[10];
```

or

```java
int anArray[] = new int[10];
```

Assign values

```java
anArray[0] = 1;
anArray[5] = 3;
```

or

```java
int[] anArray = {1,2,3,4,5,6}
```

no need for size; however have to do this at the declaration stage.

**Can't do like this:**

```java
##### THIS WONT WORK #####
int anArray[];
anArray = {1,2,3,3,45,4};
```

Why ?

- Because the previous method, when creating the array java will automatically count and assign a suitable length to the array. In the next method since the array is declared already, you can't assign anymore. unless you do `new int[size]`

### double[] array

```java
double[] array = new double[7]
```

### String[] array

```java
String[] array = {"hi","this"}
```

