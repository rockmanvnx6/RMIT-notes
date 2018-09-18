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
>



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

IF you extends from an abstract class, you need to include its ==abstract method== if any.

And `Cat` also have ==name and age== as inheritance.



## Interface

Interface is like a set of signature that say the `class` ==will follow these interface==

There are bunch of codes signature but without the body.

Usually, the interface is ==public==. The class will have to implement all of the method which are in that interface.



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





