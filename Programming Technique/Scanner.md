# Scanner -Lecture 2

To use scanner, you need import a library for it

`import java.util.Scanner`

```java
Scanner input = new Scanner(System.in);
int i = input.nextInt(); // to receive int value
int c = input.nextLine(); // to receive string value
```

**Example**

```java
System.out.print("Enter new user name:");
Scanner input = new Scanner(System.in);
String username = new String(input.nextLine());
System.out.print("Your user name is: "+username);
```

## Scan numbers

To get the `int` from input. Use `nextInt()`

```java
System.out.print("Enter 2 numbers: ");
Scanner input = new Scanner(System.in);
int n1,n2;
n1 = input.nextInt();
n2 = input.nextInt();
System.out.println("Number entered: n1 = " + n1 + "; n2 = " + n2);
```



> Enter 2 numbers: 1 2
>
> Number entered: n1 = 1; n2 = 2;

Likewise, we have `nextFloat()` `nextDouble()`



## Scan Strings

Two main method: `next()` and `nextLine()`

`next()` seperate `strings` by space. Doesn't count extra space

`nextLine` seperate `strings` by newline

```java
System.out.print("Enter s1 and s2: ");
String s1,s2;
Scanner input = new Scanner(System.in);
s1 = input.nextLine();
s2 = input.nextLine();
System.out.println("String Entered: s1 = " + s1 + "; s2 = " + s2);
```

> Enter s1 and s2: thang pham
>
> ngoc
>
> String entered: s1 = thang pham; s2 = ngoc



```java
System.out.print("Enter s1 and s2: ");
String s1,s2;
Scanner input = new Scanner(System.in);
s1 = input.next();
s2 = input.next();
System.out.println("String Entered: s1 = " + s1 + "; s2 = " + s2);
```

> Enter s1 and s2:              thang                       pham
>
> String entered: s1 = thang; s2 = ngoc

So whenever there is a space, s1 will take the word value before the space



## Note

`nextLine()` will take everything including space. It's suitable when you want to capture names, since names have space.

Every `next()`, `nextLine()`,`nextInt()`,`nextDouble()`,`nextFloat()`,...

will capture the `\n`. So there is no need to do `println`

thus:

```java
Scanner input = new Scanner(System.in);
System.out.print("Enter name: ");
String name = input.nextLine();
System.out.print("Enter age: ");
int age = input.nextInt();
System.out.print("Enter weight: ");
double weight = input.nextDouble();

System.out.printf("\nName: %s\nAge: %d\nWeight: %f",name,age,weight);
```

This will do the job.

> Enter name: thang pham
>
> Enter age: 20
>
> Enter weight: 67.4

Name: thang pham

Age: 20

Weight: 67.4