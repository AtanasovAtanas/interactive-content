# Generic Methods

[slide]

# Generic Methods

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

