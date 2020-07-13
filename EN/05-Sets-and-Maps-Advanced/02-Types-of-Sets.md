

[slide]

# Types of Sets

**HashSet**

The **HashSet** class implements the **Set** interface, backed by a **Hash Table**.

It makes **no guarantees** about **the sequence of the elements** when you iterate them.

The **HashSet** class offers **constant** time performance for the basic operations - `add()`, `remove()`, `contains()` and `size()`.

- Initialization:
```java
Set<String> hash = new HashSet<String>();
```
- Adding Elements 
```java live
Set<Integer> hash = new HashSet<>();

List<Integer> data = Arrays.asList(40,20,30,10,50,10,10,10);

hash.addAll(data);

System.out.println(hash);
```

**TreeSet**

The elements are ordered using their **natural ordering**.

The TreeSet provides guaranteed **log(n)** time cost for the basic operations - `add()`, `remove()` and `contains()`.

**Null values** are **not accepted** by the TreeSet.

- Adding Elements 
```java live
Set<Integer> tree = new TreeSet<>();

List<Integer> data = Arrays.asList(40,20,30,10,50,10,10,10);

tree.addAll(data);

System.out.println(tree);
```

- Initialization:
```java
Set<String> tree = new TreeSet<>();
```

**LinkedHashSet**

A **LinkedHashSet** is an **ordered version of HashSet** that maintains a doubly-linked List across all elements.
A **LinkedHashSet** provides **constant** time performance for the basic operations - `add()`, `contains()` and `remove()`.

A LinkedHashSet allows maximum **one null element**.

- Adding Elements 
```java live
Set<Integer> linkedHashSet = new LinkedHashSet<>();

List<Integer> data = Arrays.asList(40,20,30,10,50,10,10,10);

linkedHashSet.addAll(data);

System.out.println(linkedHashSet);
```

- Initialization:
```java
Set<String> linkedHashSet = new LinkedHashSet<>();
```

[/slide]