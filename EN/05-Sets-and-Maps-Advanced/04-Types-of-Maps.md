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

hashMap.put("BMW", 5);
hashMap.put("Mercedes", 3);
hashMap.put("Opel", 4);
hashMap.put("Dacia", 10);

hashMap.forEach((k, v) -> System.out.println(k + " - " + v));
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

treeMap.put("BMW", 5);
treeMap.put("Mercedes", 3);
treeMap.put("Opel", 4);
treeMap.put("Dacia", 10);

treeMap.forEach((k, v) -> System.out.println(k + " - " + v));
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

linkedHashMap.put("BMW", 5);
linkedHashMap.put("Mercedes", 3);
linkedHashMap.put("Opel", 4);
linkedHashMap.put("Dacia", 10);

linkedHashMap.forEach((k, v) -> System.out.println(k + " - " + v));
```


[/slide]