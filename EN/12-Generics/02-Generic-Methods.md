# Generic Methods

[slide]

# Generic Methods

Generic methods are those methods that are written with a **single method declaration** and can be called with **arguments of different types**. 

The **compiler will ensure the correctness** of whichever type is used. 

The main features of generic methods are:

- Generic methods have a **type parameter** (the diamond operator enclosing the type) before the return type of the method declaration
- Type parameters can be **bounded** (bounds are explained later in the article)
- Generic methods can have **different** type parameters separated by commas in the method signature
- Method body for a generic method is just like a normal method


```java live no-template
public class Main {

    static <T> void genericPrinter(T element) {
        System.out.println(element);
    }

    public static void main(String[] args) {

        genericPrinter(5); // Integer
        genericPrinter("SoftUni"); // String
        genericPrinter(1.5);  // Double
    }
}
```

[/slide]

