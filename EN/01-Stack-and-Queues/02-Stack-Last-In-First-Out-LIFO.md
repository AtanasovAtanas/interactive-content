# Stack - Last In First Out - LIFO

[slide]
# Stack Functionality

A Stack is a data structure where you add elements to the **top** of the stack, and also remove elements from the **top** again.
This is also referred to as the "Last In First Out" - **LIFO** principle. 

- Stacks provide the following functionality:
    - Pushing an element at the top of the stack
    - Popping element from the top fo the stack
    - Getting the topmost element without removing it

[image assetsSrc="stacksAndQueues-example(1).png" /]

[/slide]

[slide]
# Java Stack Implementation

- Stack Implementation using `ArrayDeque<E>`
```java
ArrayDeque<Integer> stack = new ArrayDeque<>();
```

- `push(element)` - adding elements at the top of the stack
```java live
ArrayDeque<Integer> stack = new ArrayDeque<>();
stack.push(2);
stack.push(5);
stack.push(10);

stack.forEach(System.out::println);
```

- `pop()` - removing the topmost element
```java live
ArrayDeque<Integer> stack = new ArrayDeque<>();
stack.push(2);
stack.push(5);
stack.push(10);

// remove 
stack.pop();

stack.forEach(System.out::println);
```

- `peek()` - getting the value of the topmost element
```java live
ArrayDeque<Integer> stack = new ArrayDeque<>();
stack.push(2);
stack.push(5);
stack.push(10);

// get 
Integer element = stack.peek();

System.out.println(element);
```
[/slide]
