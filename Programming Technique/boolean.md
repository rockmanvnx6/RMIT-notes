# Boolean

## Initialize

**Inside main**

```java
boolean b1 = true;
```

`lower case true`

**outside main, inside class**

```java
static boolean bD;
```

> Default value of `static boolean` == `false`



## ParseBoolean

You can create boolean value based on a string value;

Let say:

```java
String bi = "tRuE";
Boolean custom = Boolean.parseBoolean(bi);
System.out.print(custom)
```

> True