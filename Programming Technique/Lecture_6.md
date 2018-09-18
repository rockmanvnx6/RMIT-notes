# PolyMorphism, static keyword

You can extend multiple class.

Example:

Animal <- Bird <- Bird's name.



## Polymorphism

> Different class has different method. Example:
>
> class Dog speaks "Woof"
>
> class Cat speaks "Meow"

The sub class needs to have the same constructor as the super class.

```java
public class Pet {
    public String name;
    
    public Pet (String name) {
        this.name = name;
    }
    public String talk() {
        return "hihihi";
    }
}
```

```java
public class Dog extends Pet{
    public Dog (String name) {
        super(name);
    }
    
    public String Bark() {
        return "Woof !!"
    }
    
    public String talk() {
        return "it will return this. And its name is: " + name;
    }
}
```

You can do

```java
Pet rex = new Dog("REx");
```

you can call `rex.talk()` but you can't call `rex.bark()`

inorder to `bark()` you need casting

```java
((Dog)rex).bark();
```



## Instanceof

To check if something is the element of a class, we use:

`something instanceof class_name`

Example:

```java
package main;

import app.Animal;
import app.Cat;
import app.Dog;


public class Main {

    public static void main(String[] args) {
        Animal Jex  = new Dog("Jex");
        Animal Smoky = new Cat("Smoky");
        Animal Jeff = new Animal("Jeff");
        Animal Bob = new Animal("Bob");
        Animal Chin = new Dog("Chin");
        Animal house[] = {Jex,Smoky,Jeff,Bob,Chin};
        for (int i = 0; i < house.length; i++) {
            if(house[i] instanceof Dog) {
                System.out.println(house[i].talk());
                System.out.println(((Dog)house[i]).bark());
            }

        }
    }
}

```

>**result:**
>
>Yo wassup my Dawg, this is Jex
>Woof, Woof !!
>Yo wassup my Dawg, this is Chin
>Woof, Woof !!

