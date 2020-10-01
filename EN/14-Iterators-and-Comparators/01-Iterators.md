
# Iterators

[slide]

# Iterable

## Collections Hierarchy

The Collection interface extends Iterable and hence all child classes of Collection also implement Iterable.

[image assetsSrc="iterators-example(1).png" /]

`Iterable<T>` is the root interface of the Java collection classes.

An Iterable represents a collection which can be traversed.

A class that implements the `Iterable<T>` can be used with the new for loop.

It does that by internally calling the `iterator()` method on the object.

## Iterable\<T\> Methods

- Iterable `iterator()` method

The Iterable `iterator()` method returns an iterator over elements of type T.

In the following example, we have a List which extends `Iterable<T>`.

The iterator() method of this List returns Iterator of type String.

So we can use all the Iterator methods.

```java
List<String> list = new ArrayList<>();
list.add("one");
list.add("two");
list.add("three");

Iterator<String> iterator = list.iterator();
```

- `forEach(Consumer<? super T> action)`

```java

```

- `spliterator()`

```java

```


[/slide]

[slide]

# Iterator

[/slide]

