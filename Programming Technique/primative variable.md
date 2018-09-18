# Primative data types

- Use to store numbers, characters, booleans
- Store in the fastest available memory
- Store in all lowercase
- Not: String!
- **default is 0**

**Example:**

```java
int myInt;
System.out.println(myInt);
```

> 0



### Declaring primative variables

Need to have their type decalare

**Example:**

`int myVar = 5`



## Numeric Primitive Data Types

| Data type | Bits | Minimum        | Maximum       |
| --------- | ---- | -------------- | ------------- |
| byte      | 8    | -128           | 127           |
| short     | 16   | -32,768        | 32,767        |
| int       | 32   | -2,147,483,648 | 2,147,483,647 |
| long      | 64   | -9.2337E+18    | 9.2337E+18    |
| float     | 32   | See docs       | See docs      |
| double    | 64   | See docs       | See docs      |



## Equivalent Helper Class

Like `Integer.parseInt("9")`

`Integer` here is the helper class.

| Data Type | Helper Class - initial upper case |
| --------- | --------------------------------- |
| byte      | Byte                              |
| short     | Short                             |
| int       | Integer                           |
| long      | Long                              |
| float     | Float                             |

**Example 1** 

- Each of the helper class is the member of the package `java.lang` example: `java.lang.Double`
- Let say: we have a double: `double doubleValue = 156.6d`
- The character `d` in here tell the system that we want it to use `double` because sometimes it use `float`
- `System.out.println(doubleValue) == 156.6`

Now if we want to assign that doubleValue to another double Value:

```java
Double doubleObj = new Double(doubleValue);
System.out.println(doubleObj);
```

> 156.6

Notice that we can also use:

```java
double anotherDouble = doubleValue;
System.out.println(anotherDouble);
```

> 156.6



But the benefit of using object is you can then dereference it.

For example, to get the `byteValue`

```java
byte byteValue = doubleObj.byteValue();
System.out.println(byteValue);
```

> -91

*You can't do that with just a normal double*



### intValue()

let say if we have a double `double doubleValue = 204.213125`

How do we get the integer value — in this case, `204` ? use `intValue()`

```java
double doubleValue = 204.213125;
Double doubleObj = new Double(doubleValue);
int return = doubleObj.intValue();
System.out.println(return);
```

> 204



### floatValue()

let say if we have a double `double doubleValue = 204.2131256789`

`floatValue()` will convert that to a float value.

```java
double doubleValue = 204.2131256789;
Double doubleObj = new Double(doubleValue);
float return = doubleObj.floatValue();
System.out.println(return);
```

> 204.21312



### toString()

convert a number into string

```javascript
double doubleValue = 204.2131256789;
Double doubleObj = new Double(doubleValue);
String return = doubleObj.toString();
System.out.println(return + 1);
```

> 204.21312567891 // this is a string



## Declare & Initializing

```java
public static void main(String[] args) {
        byte b = 1;
        short sh = 1;
        int i = 1;
        long l = 1;
        float f = 1f;
        double d = 1d;
        System.out.println("Byte: " + b);
        System.out.println("Short: " + sh);
        System.out.println("Int: " + i);
        System.out.println("Long: " + l);
        System.out.println("Float: " + f);
        System.out.println("Double: " + d);
}
```

>Byte: 1
>Short: 1
>Int: 1
>Long: 1
>Float: 1.0
>Double: 1.0



## MAX_VALUE

You can call the MAX_VALUE of one type by:

```java
Byte.MAX_VALUE
Integer.MAX_VALUE
Float.MAX_VALUE
Double.MAX_VALUE
Long.MAX_VALUE
Short.MAX_VALUE
```

>127
>3.4028235E38
>2147483647
>1.7976931348623157E308
>9223372036854775807
>32767

