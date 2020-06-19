# Queue - First In First Out - FIFO

[slide]
# Queue Functionality

A Queue is a "First In First Out" - **FIFO** data structure. 
It models a **queue** in **real-life**, you might have seen in front of a cinema, a shopping mall, a metro, or a bus.

Just like queues in real life, **new elements** in a Queue data structure are added **at the back** and **removed from the front**. 

# Queues provide the following functionality:

- Adding an element at the end of the queue

[image assetsSrc="queue-example(1).png" /]
    
- Removing the first element from the queue

[image assetsSrc="queue-example(2).png" /]

- Getting the first element of the queue without removing it

[image assetsSrc="queue-example(3).png" /]


[/slide]

[slide]
# Queue Implementation and Built-In Methods

- Queue Implementation using `ArrayDeque<E>`
```java
ArrayDeque<Integer> queue = new ArrayDeque<>();
```
- `offer(element)` or `add(element)` - both methods add elements at the end of the queue
    - `add()` – throws exception if queue is full
    - `offer()` – returns false if queue is full

```java live 
ArrayDeque<Integer> queue = new ArrayDeque<>();

queue.offer(2);
queue.add(5);
queue.offer(10);
        
System.out.println(queue);
```

- `poll()` or `remove()` - both methods remove the first element from the queue
    - `remove()` - throws exception if queue is empty
    - `poll()` - returns null if queue is empty, otherwise returns the removed element

```java live
ArrayDeque<Integer> queue = new ArrayDeque<>();

queue.offer(2);
queue.add(5);
queue.offer(10);

// remove
System.out.println("Removed element is: " + queue.poll());
queue.forEach(element -> System.out.print(element + " "));
```
- `peek()` - getting the value of the first element

```java live
ArrayDeque<Integer> queue = new ArrayDeque<>();

queue.offer(2);
queue.add(5);
queue.offer(10);

System.out.println("First element is: " + queue.peek());
```



[/slide]

