# Interfaces and abstract class

Abstract can't be initialise.

Like saying if you have a `public abstract class Pet`

You can't do

```java
Pet pet = new pet();
```

> But you can do
>
> ```java
> Pet my_dog = new Dog();
> ```
>

- Use this when you want the Class cannot be initialized, so like if you have a class name `Animal`. You don't want the user to create `new Animal`. You want to specify it to either `new Dog` or `new Cat`

**HOWEVER**

you can initialise the whole array:

```java
Pet house[] = new Pet();
house[0] = new Dog();
```



## Abstract method

```java
public abstract class Pet {
    private String name;
    private int Age;
 	public abstract String talk();   
}
```



You can't put anything to the abstract method. You need to @override the method in sub class.



```java
public class Cat extends Pet {
    @Override
    public String talk() {
        System.out.print("meow");
    }
}
```

IF you (are not abstract class) and extends from an abstract class, you need to include its ==abstract method== if any.

And `Cat` also have ==name and age== as inheritance.

* Abstract class doesn't necessarily need to include its parent's abstract methods. 

## Interface

Interface is like a set of signature that say the `class` ==will follow these interface==

There are bunch of codes signature but without the body.

Usually, the interface is ==public==. The class will have to implement all of the method which are in that interface.

**You don't need to declare variable in interface and don't need to declare type <kbd>public</kbd>, <kbd>private</kbd>, <kbd>protected</kbd>**

```java
public interface MotorVehicle {
    void run();
    int getFuel()
}

class Car implements MotorVehicle{
    int fuel;
    public void run() {
        print("Wroooom");
    }
    
    public int getFuel() {
        return this.Fuel();
    }
}
```





