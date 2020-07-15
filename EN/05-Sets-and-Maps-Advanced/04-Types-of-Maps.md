[slide]

# Types of Maps

## HashMap < Key, Value >

HashMap is implemented as a **Hash Table**, and there is **no ordering on keys or values**.

It implements all of the **Map** operations and **allows null values** and **one null key**. 

Consider to use a **HashMap** when **order does not matter and nulls are acceptable**.

- Initialization:
```java
Map<String, Integer> hashMap = new HashMap<>();
```
- Adding Elements 
```java live
Map<String, Integer> hashMap = new HashMap<>();


```
## TreeMap < Key, Value > 

**TreeMap** is **sorted** according to the **natural ordering of its keys**.

**TreeMap** in Java **does not allow null keys**.

It's better to use a **TreeMap** when you want **a Map sorts its key-value pairs by the natural order of the keys** (e.g. **alphabetic** order or **numeric** order).

- Initialization:
```java
Map<String, Integer> treeMap = new TreeMap<>();
```
- Adding Elements 
```java live
Map<String, Integer> treeMap = new TreeMap<>();


```

## LinkedHashMap < Key, Value >

**LinkedHashMap** also maps a `Key` and a `Value`.

It inherits HashMap class, but **maintains insertion order**.

**Keeps the Keys in order of addition.**

It's better to use a **LinkedHashMap** when you want **a Map with its key-value pairs are sorted by their insertion order.**

- Initialization:
```java
Map<String, Integer> linkedHashMap = new LinkedHashMap<>();
```
- Adding Elements 
```java live
Map<String, Integer> linkedHashMap = new LinkedHashMap<>();


```


[/slide]