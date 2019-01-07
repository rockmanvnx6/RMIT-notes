# File_IO

First, need to import a few thing.

```java
import java.io.*;
import java.util.Scanner;
```

- ` java.io.*` for File access
- `java.util.Scanner` for file reading.

# To READ



## It's best to use File reading with try and catch

```java
public static void main(String args[]) {
    String content = new String();
   	File inputFile = new File("file.txt");
    try {
        Scanner input = new Scanner(inputFile);
        while(input.hasNextLine()) { 
        	content += input.nextLine()
        }
    } catch (Exception e) {
        System.out.println("No file");
    }
    System.out.println(content);
}
```

So basically put the file inside `Scanner()`

## Read using delimiter

```java
String content = new String();
File inputFile = new File("file.txt");
try{
    Scanner input = new Scanner(inputFile);
    input.useDelimiter(":");
    while(input.hasNext()) {
        content += input.next();
    }
} catch (Exception e) {
    System.out.println("No file");
}

System.out.println(content);
```

Remember to use `hasNext()` instead of `.hasNextLine()`

and `next()` insteaad of `nextLine()`



# To write

## Good to use try catch as well

use `PrintWriter out = new PrintWriter("file.txt")`

and then `out.println("Something")` to write in the file.

**Example**

```java
public static void main(String args[]) {
    File output = new File("output.txt");
    String test = "This is a string.";
    try {
       	PrintWriter out = new PrintWriter(output);
        int i = 0;
        while (i < 10) {
            out.println(test);
            i++;
        }
        out.close();
    } catch (Exception e) {
        System.out.println("Error: " + e.getMessage());
    }
}
```

Remeber to `close()` else it won't work



Exception for `java.io.*` are called `IOException`

# Append

Now you can't use `File output = new File("file.txt")` any more.

Have to use

```java
FileOutputStream output = new FileOutputStream("file.txt",true);
```

`true` will allow us to append to an existed file.

but FileOutputStream are required to put in a try catch block

```java
try {
	FileOutputStream output = new FileOutputStream("output.txt", true);
    int i = 0;
    PrintWriter out = new PrintWriter(output);
    while(i < 10) {
        out.println("hi");
        i++;
    }
    out.close();
} catch (Exception e) {
    System.out.println(e);":"
}
```

## Read everyfile in a folder:

```java
File path = null;
String filename = new String();
try {
    path = new File("."); // current folder;
    File list[] = path.listFiles();
    for(int i = 0; i < list.length; i++) {
        filename += list[i].getName();
    }
} catch (Exception e) {
    System.out.println(e);
}

System.out.println(filename);
```

## Check if a file exists

```java
import java.io.*;

class FileExist{
	public static void main(String args[]) {
		System.out.println(new File("file.txt").isFile());
	}
}
```

> Boolean: True or False