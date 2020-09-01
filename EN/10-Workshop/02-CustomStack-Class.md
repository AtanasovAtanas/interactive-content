# CustomStack Class

[slide]

## Implement CustomStack Class

### Details about the Structure

The implementation of a **custom stack** is much easier, mostly because you can only execute actions over the last index of the **collection**, plus you can iterate through the collection.

You should be able to create it entirely on your own.

The first thing you can do is to have a clear vision of how you want your structure to work under the provided public functionality.

For example:
- It should hold a **sequence of items in an array**
- The structure should have a **capacity** that **grows twice** when it is filled, **always starting at 4**. 

The **CustomStack** class should have the fields listed below:

- `int[] items` - an array, which will hold all of our elements
- `int size` – holds the **size with real data** of the array
- `final int initialCapacity` – this constant's value will be the initial capacity of the internal array
- `int capacity` – holds the size of the array

[/slide]


[slide]

## Implementation

Create a new public class **CustomStack** and add a private constant field named **initialCapacity** and set the value to 4.

This field is used to declare the **initial capacity** of the **internal** array.

We already know that it's not a good practice to have **magic numbers** in your code.

Afterwards, we are going to declare our internal array and a field for the **capacity** of elements in our collection:

```java
public class CustomStack {
    private static final int INITIAL_CAPACITY = 4;
    private int capacity;
    private int size;
    private int[] items;
}
```

Of course, you have to initialize the collection.

Also, set the **capacity** variable to **initial capacity**.

As we already know, this can be done inside the constructor of the class:

```java
public CustomStack() {
    this.capacity = INITIAL_CAPACITY;
    this.items = new int[this.capacity];
}
```
Next, you have to add a public method **size** that holds the value of the **size** fields.

This way, you will be able to get the size of items in the collection from other classes:

```java
public int getSize() {
    return this.size;
}
```

Now you can proceed to the implementation of the methods, which your **CustomStack** is going to have.

All of the functionalites described in the description are very easy to implement, so we strongly recommend for you to try to do it on your own.

If you have any difficulties, you can help yourself with the code snippets below.


[/slide]