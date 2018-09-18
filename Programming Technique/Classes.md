# Classes

You can create a classes by following:

Remember the class file has to be in the same folder.

- Create a new Class java file

- ```java
  package com.example.java;
  
  public class Hero {
      String name;
      int damage;
      public void Display(){
          System.out.println("Character name: "+this.name);
          System.out.println("Character damage: "+this.damage);
      }
  }
  
  ```

- For main.java

  ```java
  package com.example.java;
  public class Main {
      public static void main(String[] args) {
          Hero Genji = new Hero();
          Genji.name = "Genji";
          Genji.damage = 313;
          Genji.Display();
      }
  }
  ```

  

For a more concise way, you can

For class java

```java
public class Hero {
    String name;
    int damage;
    public Hero(String name, int damage) {
        this.name = name;
        this.damage = damage
    }
    void Display () {
        System.out.println("Character name: "+ name);
        System.out.println("Character damage: "+ damage);
    }
}
```

And Main.java

```java
public class Main {
    public static void main(String[] args) {
        Hero Genji = new Genji("Genji",2929);
        Genji.Display();
    }
}
```

> Use **public Hero** will create an constructor **Hero** in the class so you can pass data in.



## Private element

> Use private element in the class when you don't want other class be able to modify it

```java
public class Cat{
    private int age;
}
```

Now you can't get `Cat.age` in main.

So how to get?

```java
public class Cat{
    private int age;
    public void getAge() {
        return age;
    }
}

```

> Now you can access by Cat.getAge();

## Extend cat

What if you want to extend your current Cat class.

- Create a new file class, for example: `Lynx.class`

- Now if you want `Lynx` to contain `cat`

- ```java
  public class Lynx extends cat {
      // now it contains all cat member.
      public Lynx {
          System.out.print("Lynx is created.");
      }
      public void growl() {
          System.out.println("grrr");
      }
  }
  ```

Now you can do Lynx.getAge() also but can't do Cat.growl();