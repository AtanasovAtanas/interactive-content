[slide]

# Fields

A Java field is a variable inside a class. For instance, in a class representing a car, the Car class might contain the following fields:

- brand
- model
- horsePower

The corresponding Java class could be defined like this:

```java
public class Car{

    String brand;
    String model;
    int horsePower;

}
```

## Access Modifiers

Access modifiers determine whether other classes can use a particular field.

There are four types of access modifiers in Java:

- private
- package-private
- protected
- public 

The **private** access modifier means that only code inside the class itself can access this Java field.

If you don't use any modifier, it is treated as **default** by **package-private**.

The **package-private** access modifier means that only code inside the class itself, or other classes in the same package, can access the field.

It provides more accessibility than private. But, it is **more restrictive than protected, and public**.

The **protected** access modifier is accessible within **package** and outside the package but through **\*inheritance** only.




\*Inheritance in Java is a mechanism in which one object acquires all the properties and behaviors of a parent object. You can find out more about **Inheritance** [here](https://docs.oracle.com/javase/tutorial/java/concepts/inheritance.html).



[/slide]