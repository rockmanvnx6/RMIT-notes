# Passing argument to console

```java
public class Main {
    public static void main(String[] args) {
        System.out.println(args[0])
    }
}
```

> String[] means create a string array from the input and then print out the first one.

**When you run it:**

```java
java Main hi
```

> Output:
>
> hi

Since the first one is hi

**If you do**

```java
java main hi thang
```

> Output:
>
> hi

since you only want to print the first one.

**To do something like that**

```java
java main "hi thang"
```

> Output:
>
> hi thang