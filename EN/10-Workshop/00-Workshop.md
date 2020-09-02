
# Workshop: Custom Data Structures

[slide]

## Overview

In this workshop, we will create our own custom data structures – a custom list (**SmartArray**) and a custom stack.

The **SmartArray** will have similar functionality to **Java ArrayList** that you've used before. 

Our **SmartArray** will work only with integers for now, but after the **Generics** lecture from this course, you can try to change that and make the structure generic, which means it will be able to work with any type. 

It will have the following functionality:

- `void add(int element)` - adds the given element to the end of the list
- `int get(int index)` - returns the element at the specified position in this list
- `int remove(int index)` - removes the element at the given index
- `boolean contains(int element)` - checks if the list contains the given element returns (True or False)
- `void add(int firstIndex, int secondIndex)` - adds an element at the specific index, the element at this index gets shift to the right alongside with any following elements, increasing size
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




