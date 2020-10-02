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

All of the functionalities described in the description are very easy to implement, so we strongly recommend you to try to do it on your own.

If you have any difficulties, you can help yourself with the code snippets below.


[/slide]


[slide]

## Implement Void Push(int Element) Method

This method adds an element to the end of the collection, just like the Java **ArrayDeque** `push()` method does.

This is a very easy task. Here is the code you can use, if you meet any difficulties:

```java
public void push(int element) {
    // resize if the size is equal to the capacity
    if (this.size == this.capacity) {
        this.resize();
    }
    this.items[this.size++] = element;
}
```

- `resize()` method:

```java
private void resize() {
    this.capacity *= 2;
    int[] copy = new int[this.capacity];

    for (int i = 0; i < this.items.length; i++) {
        copy[i] = this.items[i];
    }
}
```

[/slide]

[slide]

## Implement Void Pop() Method

The `pop()` method returns the last element from the collection and removes it.

The implementation is easier than the implementation of the `remove(int index)` method of the **SmartArray**.

Try to implement it on your own.

Afterwards, you can look at this implementation:

```java
public int pop() {
    // throw NoSuchElementException if the size is zero
    int element = this.items[this.size - 1];
    this.size--;
    return element;
}
```

- `checkEmpty()` method checks if the stack size is equal to 0.

```java
private void checkEmpty() {
    if (this.size == 0) {
        throw new NoSuchElementException("CustomStack is empty");
    }
}
```


[/slide]

[slide]

## Implement Void Peek() Method


The `peek()` method has the same functionality as the **Java ArrayDeque** - it returns the last element from the collection, but it **doesn't remove it**.

The only thing we need to consider is that you can't get an element from an empty collection, so you must make sure you have the proper **validation**.

For sure, you will be able to implement it on your own.

[/slide]

[slide]

## Implement Void ForEach Method

This method goes through every element from the collection and executes the given action.

The implementation is very easy, but it requires some additional knowledge, so here is what you can do:

```java
public void forEach(Consumer<Integer> consumer) {
    for (int i = 0; i < this.size; i++) {
        consumer.accept(this.items[i]);
    }
}
```

You can add any kind of functionalities to your **CustomStack** and afterwards, you can test how it works in your `main()` method.

[/slide]
