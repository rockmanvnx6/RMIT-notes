# Organize java classes

Let say we have folder hiarchy :

```java
folder
	folder1
		folder2
			main.java
```

in the beginning, we have to include package

```java
package folder.folder1.folder2;
public class Main{
    public static void main(String[] args) {
        System.out.println("Hello");
    }
}
```

## To compile

```console
javac folder/folder1/folder2/main.java
```

## To run

```console
java folder.folder1.folder2.main
```

> Hello

*Notice that `folder.folder1.folder2` has to declare in `package` inorder to run successfully*

> You don't have to do packages to organize the classes but all developers do it this way. So it's the good practice to use.