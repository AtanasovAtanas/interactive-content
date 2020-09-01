
# SmartArray Class

[slide]

## Implement SmartArray Class

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

[slide]

## Implement Void Add(int Element) Method

It is time to create the method which **adds** a new elements to the **end** of our collection.

It looks like an easy task, but keep in mind that if our internal array is **filled**, we have to **increase it by twice** the length it currently has and **add** the **new element**.
 
To make our job easier let's create a `resize()` method first.

The method should be used only **within** the **class** so it must be **private**.

```java
private void resize() {

}
```

Here is how the method should work step by step:

- Create a new array with length **twice** the current length of the internal array:

```java
private void resize(){
    this.capacity *= 2;
    int[] copy = new int[this.capacity];
}
```

- Iterate through the items in the **internal array** and fill the **newly created array**:

```java
for (int i = 0; i < this.data.length; i++) {
    copy[i] = this.data[i];
}
```

- Set the newly created array to the field "**data**":

```java
this.data = copy;
```

- The whole method should look like this:

```java
private void resize() {
    this.capacity *= 2;
    int[] copy = new int[this.capacity];

    for (int i = 0; i < this.data.length; i++) {
        copy[i] = this.data[i];
    }

    this.data = copy; 
}
```

Now, we are ready to start implementing the logic behind the `add()` method.

This is how the method should work:

```java
public void add(int element) {

}
```

- Check if the **size** of the **actual data** in our **SmartArray** is equal to the **capacity of our collection**.

If it is, this means that the internal array is **filled** and we need to use the **resize()** method.

```java
if (this.size == this.capacity){
    this.resize();
}
```

- After we have checked that we have empty space in the internal array, we can just **add** the **new** item at the end and update the "**size**" field:

```java 
this.data[this.size++] = element;
```

The whole method should look like this:

```java
public void add(int element) {
    if (this.size == this.capacity){
        this.resize();
    }
    this.data[this.size++] = element;
}
```

Before proceeding with the next tasks, it is a good practice, since you've done so much work, to test if everything is fine.

Use the **debugger** to **test** for bugs.


[/slide]

[slide]

## Implement Int Get(int index) Method

This method has the functionality to **get item** at given **index** from our internal array.

Keep in mind that you have to check if the given index is at the range of our array.

If it's in range return the **element** at our index, if not throw the corresponding exception.

Let's start implementing our method:

```java
public int get(int index){
    // TODO: Check index

    return this.data[index];
}
```

Checks whether the **index** is **less than zero** or **greater than** the actual **size** of internal array.

If it's true throw **IndexOutOfBoundsException**.

We can create **private method checkIndex** because we can use it again later:

```java
private void checkIndex(int index) {
    if (index < 0 || index >= this.size){
        // throw IndexOutOfBoundsException
    }
}
```

When we throw any kind of exception, we can add our personal message:

```java 
private void checkIndex(int index) {
    if (index < 0 || index >= this.size) {
        String message = String.format("Index %d out of bounds for length %d",
                index, this.size);
        throw new IndexOutOfBoundsException(message);
    }
}
```

The whole method should look like this:

```java
public int get(int index) {
    checkIndex(index)

    return this.data[index];
}
```

[/slide]

[slide]

## Implement Int Remove(int Index) Method

The `remove()` method has the functionality to **remove an element** on the **given index** and **returns the same element**.

Let's think about how to solve this problem by **dividing it to smaller tasks**.

- First we must check if the index is **valid** and if not, we should throw **IndexOutOfBoundsException**
- Get the item on the given index and assign it to a variable, which will be **returned** at the end
- Set the value on the given index to the **default value of int**
- Now we have an empty element and we need to **shift** the elements
- Reduce the size and check if the size is **4 times smaller** than the **internal array** capacity
    - If it is, we have to think about a way to **shrink** the array
- In the end, return the variable to which we assigned the value of the requested index

So now you already know that we need to implement the other 2 internal methods `shift()` and `shrink()`.

## Void Shift(int Index)

The shift method uses a loop, which moves all of the elements to the left, starting from a given index.

```java
private void shift(int index) {
    for (int i = index; i < this.size - 1; i++) {
        this.data[i] = this.data[i + 1];
    }
    this.data[size - 1] = 0;
}
```

## Void Shrink()

Decrease the **size** and check if it is **4 times smaller** than the **capacity**.

Probably it is but is not necessarily.

If its smaller, a good idea is to shrink our array, so we can free some memory.

Our **SmartArray** will keep only integers, which makes it pretty easy with the memory consumption.

However, if we had to store complex objects, which would have taken a lot more memory, we would rather think about shrinking it anyway.

The `shrink()` method is exactly the same as the `resize()` method with the small difference that it will **reduce** the length twice, instead of increasing it:

```java
private void shrink() {
    this.capacity /= 2;
    int[] copy = new int[this.capacity]
    for (int i = 0; i < this.size; i++) {
        copy[i] = this.data[i];
    }

    this.data = copy;
}
```


Now we are ready to proceed with the implementation of the `remove()` method.

```java
public int  remove(int index) {

}
```

- First, we need to validate that our index is valid. We can use our **checkIndex** method:

```java
public int remove(int index) {
    checkIndex(index);
}
```

- Get the value on the given index, assign it to a variable and don’t forget to shift the elements:

```java
int element = this.data[index];
shift(index);
```

- Now we must reduce the size and check if shrinking the array is required:

```java
this.size--;

if (this.size <= this.capacity / 4) {
    shrink();
}
```

- After all, just return the element that we saved at the start.

The whole method should look like this:

```java
public int remove(int index) {
    checkIndex(index);

    int element = this.data[index];
    shift(index);
    this.size--;

    if (this.size <= this.capacity / 4) {
        shrink();
    }

    return element;
}
```

It is time to test out your **SmartArray** again.

If everything works fine, proceed with the next task.


[/slide]

[slide]

## Implement Void Add(int Index, Int Element) Method

You are already familiar with this method so let's head straight to the implementation.

First of all, we will **split** the logic on **small tasks**:
- We have an index parameter, so we must **validate the index**
- We must check if the array should be **resized**
- We have to **rearrange** the items to **free the space for the required index**
- Finally **add** the given element on the index and **increase** the **size**

You probably already noticed, that since we have a method to **rearrange** the elements to the left, used to fill up the empty space when we remove an element, we must have method to **rearrange** elements to the right, so let's create it.

Starting from the **end of the actual elements**, this method will **copy** every single element on the **next indexes**.

The loop will **end on the requested index**:

```java
private shiftRight(int index) {
    for (int i = this.size - 1; i > index; i--) {
        this.data[i] = this.data[i - 1];
    }
}
```
Now complete the **add** method:

```java
public void add(int index, int element) {
    checkIndex(index);

    if (index == this.size - 1) {
        add(this.data[this.size - 1]);
        this.data[this.size - 2] = element;
    } else {
        this.size++;
        shiftRight(index);
        this.data[index] = element;
    }
}
```

[/slide]

[slide]

## Implement Boolean Contains(int Element) Method

This method should check **if** the given element **is in the collection**.

Return **true** if it is contained and **false** if it's not.

It's a simple task, so you should do it all on your own.

**Hint**: When you are **iterating** through the elements, use the **size** field as an **end condition**, instead of the internal array **capacity**.


[/slide]

[slide]

## Implement ForEach(Consumer<Integer> Consumer) Method

Implement a method which will allow you to iterate through each element of the **SmartArray**.

You can pass `Consumer<>` to the method:

```java
public void forEach(Consumer<Integer> consumer) {
    for (int i = 0; i < this.size; i++) {
        consumer.accept(this.data[i]);
    }
}
```

Feel free to add methods whatever you may find useful or interesting.

[/slide]