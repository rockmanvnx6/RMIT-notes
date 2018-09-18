# Inheritence and other OO concepts

@Override

> Every class is extended from `object` class.

if you do @Override, you override the default method.

```java
@Override
public class toString(){
    return 1; //Override the default toString();
}
```



## Super()

can be act as the constructor or to call the method from the parent calss.

```java
class Animal {
    protected String spiecies;
    protected int average_ages;
    public Animal(String spiecies, int average_ages) {
        this.spiecies = spiecies;
        this.average_ages = average_ages;
    }

    public String Display() {
        return "Species: " + spiecies + "\nAverage_ages: " + average_ages;
    }
}

class Dog extends Animal{
    private String sound = "Bark";
    public Dog(String spiecies, int average_ages) {
        super(spiecies,average_ages);
    }
    public void Bark() {
        System.out.println(sound);
    }
    @Override
    public String Display() {
        return super.Display() + " -  Dog";
    }
}

class Animal_house{
    public static void main(String[] args) {
        Animal dog = new Dog("Autistic",20);
        ((Dog) dog).Bark();
        System.out.println(dog.Display());
    }
}
```

> Bark
> Species: Autistic
> Average_ages: 20 -  Dog

## Method overloading

```java
public void draw(String s) {
    ...
}

public void draw(int i) {
    ...
}

public void draw(double f) {
    ...
}

object.draw(55) // call int
object.draw("hi") // call string
object.draw("55.55") // call double
```



## Final

> Final prevent a class from raising sub class. Prevent a method for being overwritten.

