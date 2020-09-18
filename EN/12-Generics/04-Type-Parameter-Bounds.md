# Type Parameter Bounds

[slide]

# Type Parameter Bounds

In case, you want to **restrict** the types that can be used as type arguments in a parameterized type, you have to use bounded type parameters.

Let's explain the need for type parameters bоunds with the following example:
```java
public class PowerOfThree<T>  {

    public int powerOf(T number) {
        return number.intValue() * number.intValue() * number.intValue();
    }
}
```
The code above will produce compile-time-error - "The method intValue() is undefined for the type T".

The error occurs as there is no way for compiler to know type `T` will always be used for numeric classes.

So, we need bounded type to restrict the types that can be used for parameterized type.

To declare a bounded type parameter, list the type parameter's name, followed by the `extends` keyword, followed by its **upper bound**.

In our case that will be a Number class.

```java
T extends Number
```
The above code should looks like this:

```java
public class PowerOfThree<T extends Number>  {

    public int powerOf(T number) {
        return number.intValue() * number.intValue() * number.intValue();
    }
}
```
Let's explain what does the code above:

The type parameter `T` extends Number to restrict the type of objects that can be used in the parameterized type.

The `Number` is a superclass of all numeric classes, such as `Integer`, `Float` and `Double`.

So, if we try to use another class which is **not a subclass of Number**, the compiler will throw `compile-time-error`.


[/slide]