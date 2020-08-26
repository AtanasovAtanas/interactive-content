[slide]

# Static Members

In Java, static members are those which belongs to the class and you can access these members without instantiating the class.

The static keyword can be used with methods, fields, classes (inner/nested), blocks.

## Static Methods

Static methods can access only static fields, methods.

To access static methods there is no need to instantiate the class, you can do it just using the class name.

```java live no-template
public class Car {
    private static String brand;
    private static int horsePower;


    public static void setBrand(String brand) {
        Car.brand = brand;
    }

    public static void setHorsePower(int horsePower) {
        Car.horsePower = horsePower;
    }

    public static String printFields() {
        return brand + " - " + horsePower;
    }

    public static void main(String[] args) {
        Car.setBrand("TESLA");
        Car.setHorsePower(503);

        System.out.println(Car.printFields());
        }
    }
```

## Static Fields

You can create a static field by using the keyword static. 

The static fields have the same value in all the instances of the class. 

These are created and initialized when the class is loaded for the first time. 

Just like static methods you can access static fields using the class name

```java live no-template
public class Car {
    private static int horsePower = 503;

    public static void main(String[] args) {
            
        System.out.println(Car.horsePower);
    }
}
```
[/slide]