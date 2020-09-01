
# Workshop: Custom Data Structure

[slide]

## Overview

In this workshop we will create our own custom data structures – a custom list (**SmartArray**) and a custom stack.

The **SmartArray** will have similar functionality to **Java ArrayList** that you've used before. 

Our **SmartArray** will work only with integers for now, but after the **Generics** lecture from this course, you can try to change that and make the structure generic, which means it will be able to work with any type. 

It will have the following functionality:

- `void add(int element)` - adds the given element to the end of the list
- `int get(int index)` - returns the element at the specified position in this list
- `int remove(int index)` - removes the element at the given index
- `boolean contains(int element)` - checks if the list contains the given element returns (True or False)
- `void add(int firstIndex, int secondIndex)` - adds element at the specific index, the element at this index gets shift to the right alongside with any following elements, increasing size
- `void forEach(Consumer<Integer> consumer)` - goes through each one of the elements in the list

Feel free to implement your own functionality or to write the methods by yourself.

The custom stack will also have similar functionality to the **Java ArrayDeque** and again, we will make it work only with integers.

Later on, we will learn how to implement it in a way that will allow us to work with any types.

It will have the following functionality:

- `void push(int element)` – adds the given element to the stack
- `int pop()` – removes the last added element
- `int peek()` – returns the last element in the stack without removing it
- `void forEach(Consumer<Integer> consumer)` – goes through each of the elements in the stack

Feel free to implement your own functionality or to write the methods by yourself.

[/slide]

[slide]

## Implement the SmartArray Class

### Details about the Structure

First of all, we must make it clear how our structure should work under the provided public functionality.

- It should hold a **sequence of items in an array**.
- The structure should have **capacity** that **grows twice** when it is filled, **always starting with capacity 4**.

The **SmartArray** class should have the fields listed below:

- `int[] data` - an array which will hold all of our elements
- `int size` – holds the size with real data of the array
- `int capacity` – holds the size of the array

The structure will have internal methods to make managing of the internal collection easier.

- `resize` – this method will be used to increase the internal collection's length twice
- `shrink` – this method will help us to decrease the internal collection's length twice
- `shiftLeft` – this method will help us to rearrange the internal collection's elements after removing one.
- `shiftRight` – this method we will use when we inset element at specific index

[/slide]

[slide]

## Implementation

Create class **SmartArray** and add private static constant field name **INITIAL_CAPACITY** and set the value to **4**.

This field is used to declare the **initial capacity** of the **internal array**.

It's always **good practice** to use **constants** instead of **magic numbers** in your classes.

This approach makes the code better for **managing and reading**.

```java
public class SmartArray {
    private static final int INITIAL_CAPACITY = 4;
}
```

Keep in mind that if the **internal array** has length of **4** this doesn’t mean that our collection holds 4 elements.
So, we need a field which will keep the information of the actual size of the elements in the structure.

This field should be updated **every** single time when we **make changes** related to the **count** of the elements like **adding** or **removing**.

```java
private int size;
private int capacity;
```

Now let's create the initial **collection**, which is a **private array of type int**.

To initialize the array, we will use the constructor of the class.

```java
private int[] data;
private int size;
private int capacity;

public SmartArray() {
    this.data = new int[INITIAL_CAPACITY];
    this.capacity = INITIAL_CAPACITY;
}
```

The whole class with the fields and the constructor should look like that:

```java
public class SmartArray {

    private static final int INITIAL_CAPACITY = 4;
    private int[] data;
    private int size;
    private int capacity;

    public SmartArray() {
        this.data = new int[INITIAL_CAPACITY];
        this.capacity = INITIAL_CAPACITY;
    }
}
```


[/slide]