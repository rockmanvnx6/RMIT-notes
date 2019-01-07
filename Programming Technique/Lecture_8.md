# Exception handling



## Can handle the exception using try/catch block.

```java
try {
    // some code
} catch (Exception e) {
    e.printStackTrace(); // print out the error.
}
```

When don't specify `Exception`, it will catch anything possible.

Also can do like `ArrayIndexOutOfBoundsException` and many other stuff.

So when there is an exception in try, it will launch the code in catch instead. In this way, the program won't crash but also print out the error.

**Example:**

Let say if you have:

```java
class Test4 {
    public static void main(String args[]) {
        int a[] = {1,2,3,4,5}
        System.out.print(a[6]);
        System.out.println("Program completed");
    }
}
```

> Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 6
> ​	at Test4.main(exception4.java:6)

With try/catch block:

```java
class Test4 {
    public static void main(String args[]) {
        try{
            int a[] = {1,2,3,4,5}
        	System.out.print(a[6]);
        } catch (Exception e) {
            e.printStackTrace();
        }
        System.out.println("Program completed");
    }
}
```

> java.lang.ArrayIndexOutOfBoundsException: 6
> ​	at Test4.main(exception4.java:6)
> Program completed

As you can see in here, `Program completed` is still printed in  the end although there is an exception error.

So whenever a line of code occurs an exception, the program will stop the `try` and run the `catch` method. Thus, you can always customize your catch to something like:

```java
catch (Exception e) {
    System.out.print("Out of array duh");
}
```

**So if i add a line after `System.out.print(a[6])` will it work?**

The answer is **no**. at **`System.out.print(a[6])`** it will run catch instead of running the actual `System.out.print(a[6])`

Example:

```java
class Test4 {
    public static void main(String args[]) {
        try{
            int a[] = {1,2,3,4,5}
        	System.out.print(a[6]);
            System.out.println("this won't run")
        } catch (Exception e) {
            e.printStackTrace();
        }
        System.out.println("Program completed");
    }
}
```

> java.lang.ArrayIndexOutOfBoundsException: 6
> ​	at Test4.main(exception4.java:6)
> Program completed

## Multiple catch

Let say if you have something like this:

```java
int a[] = {0,2,3,4,5};
int result = a[5] / a[0];
System.out.print(result);
```

There are 2 errors with this code.

- Index Out of bound
- Divide by zero.

The question is how do we display a specific message for a specific error?

**Solution**

```java
try {
    int a[] = {0,2,3,4,5};
    int result = a[4] / a[0];
    System.out.print(result);
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Out of bound");
} catch (ArithmeticException e) {
    System.out.println("Divide by zero");
}
```

So now everything it's covered for any error.

# Throws exception

Throws exception allows you to customize your exception error.

In the previous example, the system itself detects the exception for you. 

Using throw, you can determine which error goes to which exception.

```java
try {
    int a[] = {0,2,3,4,5};
    int result = a[4] / a[3];
    if(result < 2) {
        throw new Exception("Result can't be less than 2");
    }
    System.out.print(result);
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Out of bound");
} catch (ArithmeticException e) {
    System.out.println("Divide by zero");
} catch (Exception e) {
    System.out.println(e.getMessage());
}
```

> Result can't be less than 2.

# Create a custom Exception.

You can create a custom Exception as well

```java
class myCustomException extends Exception() {
    public myCustomException() {
        // default constructor, must have.
    }
    public myCustomException(String message) {
        super(message);
    }
    public getMessage(){
        super.getMessage();
    }
}
```

Example:

```java
class SmallerThanTwoException extends Exception {
    public SmallerThanTwoException() {
        
    }
    public SmallerThanTwoException(String message)
    {
    	super(message);    
    }
}

class Test {
    public static void main(String args[]) {
        try {
            int a[] = {0,2,3,4,5};
            int result = a[4]/a[3];
            if(result < 2) {
                throw new SmallerThanTwoException("The result can't be smaller than 2");
            }
            System.out.print(result);
        } 
        catch (ArrayIndexOutOfBoundsException e) 					{
           	System.out.println("Hi, out of bound.");
        }
        catch (ArithmeticException e)
       	{
        	System.out.println("Divide by 0");    
        }
        catch (SmallerThanTwoException e)
        {
            System.out.println(e.getMessage()); // inheritant from super class.
        }
    }
}
```

> The result can't be smaller than 2

### If you want to throw but throw is not in try or catch:

You need to use `throws` method.

```java
class Test {
    public void test() throws SmallerThanTwoException {
        if(something_is_wrong) {
            throw new SmallerThanTwoException("hi");
        }
    }
}
```

And then in main class, you need to catch.

```java
class Driver{
    public static void main(String args[]) {
        Test a = new Test();
        try{
            a.test();
        } catch (SmallerThanTwoExcecption e) {
            System.out.println(e.getMessage());
        }
    }
}
```

## Throw in abstract class, abstract method

```java
public abstract class A {
    public abstract void test() throws Exception;
}
```

remember to use `throws` in here.