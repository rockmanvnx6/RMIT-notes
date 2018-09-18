# Lecture 1: print, declare.

```java
public class Program_name {
    public static void main(String[] args) {
        // code.
    }
}
```

**Public : ** The method available for the intire definition

**Static:** Can be call within the class.

`args` doesn't have to be `args`. You can name it anything you like

## To print

`System.out.println("something")`

To add a variable:

*Variable must start with alpha character or underscore*



```java
public class Project_name {
    public static void main(String[] args) {
        char a = 'd';
        System.out.println("goo" + a);
    }
}
```

> good



You can append numbers as well.

```
int a=4;
System.out.println("this is " + a);
```

> This is 4



*One class only has a specific job.*



## To link other .java files.

```java
public class Program_name {
    public static void main(String[] args) {
        // code.
       	new File2().sayHello();
    }
}
```

File2.java:

```java
public class Test2 {
	public void sayHello() {
		System.out.println("Pho ga");
	}
}

```

> Pho ga

or

```java
public class Program_name {
    public static void main(String[] args) {
        // code.
       	File2 a = new File2();
        a.sayHello();
    }
}
```

> Pho ga

## Data type

`byte` `short` `int` `long` `float`  `double` `char` `boolean`

**char** : ``

**string:** ""

**Casting:** 

`(int) varriable`or `(int) value`;

## Declare constants

`final int UPPER_CASE = value`

## Import

`import java.util.Scanner`

# Note

short hand ternary works for java.

```
result = condition ? ifTrue : ifFalse;
```



**Classes start with uppercase character**

```
class MyClass
```

**Method and variable start with lowercase character**

```
void doSomething(String withThis) {}
```

**Constant are all upper case**

```java
public static final String FIRSTNAME = "David"
```

**Final: can't be change**

**Static: can be called within the class.**

