# String - Lecture 2

# COMPARE 2 STRINGS USE .EQUALS()

### To create a new String:

`String something;`

### To assign the String to be something:

`String something = new String("aciobaxoibco");`

or short hand:

`String something = "something"`

### To assign one string to another:

`String h1, h2;`

`h1 = h2`

### To get the length of a string:

`h1.length()`

### To check if the string empty:

`h1.isEmpty()`

### To check if 2 String equals:

`h1.equals(h2)` **ignore uppercase and lowercase**

why can't use `==` ?:

> Because it will compare the pointer between the two values.

### To compare 2 strings

`s1.compareTo(s2)`

| result | value    |
| ------ | -------- |
| < 0    | S1 < S2  |
| = 0    | S1 == S2 |
| > 0    | S1 > S2  |



## To get a character at specific index `substring, charAt`

`h1.charAt(index)`

`h1.substring(0,1)` 

stops at 1, take 0.

> Syntax:
>
> `substring(start,end)` or `substring(start)`

### To get the index:

`h1.indexOf("either a char or a sentence like this")`

`h1.lastIndexOf("something")`

# Mutable String

String normally is immutable, which mean you can't change the value of the string



use `StringBuffer` then `setCharAt`

`StringBuffer string = new StringBuffer("something")`

`string.setCharAt(2,'a')`

> soaething

# String conversions

## toLowerCase()

> This **only works with `String`, not `StringBuffer`**

```java
String name = "THANG";
System.out.println(name.toLowerCase());
```
> thang
> 

## toUpperCase()


> This **only works with `String`, not `StringBuffer`**

```java
String name = "thang";
System.out.println(name.toUpperCase());
```
> THANG


## replace(String s1, String s2)

> This **only works with `String`, not `StringBuffer`**

```java
String name = "thangpham";
name = name.replace('a','x')
System.out.println(name);
```
> thxngphxm



## replaceAll(String s1, String s2)

> This **only works with `String`, not `StringBuffer`**

```java
String name = "thangpham pham ngoc thang";
name = name.replaceAll("thang","kieu");
System.out.println(name);
```
> kieupham pham ngoc kieu

Likewise, we have `replaceFirst()`



> The difference between  replace and replaceAll is:
>
> `replaceAll` accepts regex for the first argument and replace do not. Thus, you can do:
>
> ```java
> String a = "thang pham phAm thAng";
> a.replaceAll("[Aa]","i")
> ```
>
> > thing phim phim thing

## trim(string)

remove space from both ends.

> This **only works with `String`, not `StringBuffer`**

```java
String name2 = "        thangpham pham ngoc thang        ";
name = name.trim();
System.out.println(name);
```
> thangpham pham ngoc thang



## Split()

`String arr[]=normalString.split("space")`

returns an array with split string:

```java
String a = "abcde efg hyz";
String arr[] = a.split(" ");
arr
```

> [abcde,efg,hyz]



* This only works like this, if you initial the array using split. won't work if you do like this:

  ```java
  ##### THIS WONT WORK #####
  String arr[] = new String[5];
  String a = "abcde efg hyz";
  arr[] = a.split(" ");
  ```
