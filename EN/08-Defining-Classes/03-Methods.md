[slide]

# Methods

A method is a collection of statements that perform some specific task and return the result to the caller. 

A method can perform some specific task without returning anything.

Methods allow us to reuse the code without retyping the code. 

In Java, every method must be part of some class.

Methods are time savers and help us to reuse the code without retyping the code.

The following example defines a method called **increaseHP** inside a class named Car.

When called, this method increase the internal **horsePower** variable with a given value.

```java
class Car {
    private int horsePower;

    public void increaseHP(int value){
        horsePower += value;
    }
}
```

## Getters and Setters

In Java **getter** and **setter** are two conventional methods that are used for retrieving and updating the value of a variable.

For each instance variable, a getter method returns its value while a setter method sets or updates its value.

Getters and Setters are also known as **accessor** and **mutator**.

Why do we need Getters and Setters?

Let's have a look at the following example:

```java
class Car {

    private int horsePower;

    public int getHorsePower() {
        return this.horsePower;
    }

    public void setHorsePower(int horsePower) {
         this.horsePower = horsePower;
    }
}
```

First we have a class Car with private field "**horsePower**", because the field has private access we cannot get or modify it.

To overcome this problem we have to use "**get**" and "**set**" methods.

The `getHorsePower()` method **returns** the value of the "**horsePower**" field.

The `setHorsePower()` method **sets** the value of the "**horsePower**" field.

## Keyword "this"

The keyword this, in Java, is a reference to the current object - the object whose method or constructor is called. 

It is like a pointer (reference), given to us by the creators of Java, with which to access the elements (fields, methods, constructors) of our own class:

```java
class Car {

    private int horsePower;
    
    // not working properly
    public void setHorsePower(int horsePower) {
         horsePower = horsePower;
    }

}

```

In the example above the `setHorsePowerNotWorking()`, is not work because the method parameter "horsePower" shadows the "horsePower" field. 

To overcome this problem, we have to use `this` keyword:

```java
 public void setHorsePower(int horsePower) {
         this.horsePower = horsePower;
    }
```

The most common use of the `this` keyword is to eliminate the confusion between class attributes and parameters with the same name.

## ToString() Method

By using `toString()` method, you can represent any object as a String.

In general, the toString method returns a string that "textually represents" this object. 

The result should be a concise but informative representation that is easy for a person to read. 

It is recommended that all subclasses override this method.

If you define `toString()` method in your class then your implemented/Overridden `toString()` method will be called:

```java live no-template
public class Car {

    private String brand;
    private String model;

    public String toString()  {
        return this.brand + " - " + this.model;
    }

    public static void main(String[] args) {
        Car car = new Car();

        car.brand = "TESLA";
        car.model = "MODEL S";

        // TESLA - MODEL S
        System.out.println(car);
    }
}
```

## Equals() Method

In java `equals()` method is used to compare equality of two Objects. 

```java
Car firstCar = new Car("TESLA", "MODEL S");
Car secondCar = new Car("BMW", "5 Series");

boolean isCarsEquals = firstCar.equals(secondCar);
// false
System.out.println(isCarsEquals);
```

## HashCode() Method

The `hashCode()` method returns the **integer** hash code value of the object. 

The hash code is always the same if the object doesn’t change.

```java
Car car = new Car();

int hash = car.hashCode(); 

System.out.println(hash); 
```



[/slide]