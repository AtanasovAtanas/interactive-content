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

[slide]
# How to iterate over a Map

Iterating through objects of type **Map.Entry <K, V>**. **Cannot modify** the collection(read-only).

There are several ways to iterate the Keys stored in a Map.

- Iterating through the items of a map using a **for-each** loop

  - `keySet()` - obtain only the keys

```java live
Map<String, Double> cars = new LinkedHashMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 3);
cars.put("Opel", 4);
cars.put("Dacia", 10);

for (String fruit : fruitsPrice.keySet()) {
    System.out.println(fruit);
}
```

  - `values()` - obtain only the values

```java live
Map<String, Double> cars = new LinkedHashMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 3);
cars.put("Opel", 4);
cars.put("Dacia", 10);

for (Double price : fruitsPrice.values()) {
    System.out.println(price);
}
```

- Iterating through the items of a map using the build-in method `entrySet()`
  - `entry.getKey()` - obtain the Keys
  - `entry.getValue()` - obtain the Values

```java live
Map<String, Double> cars = new LinkedHashMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 3);
cars.put("Opel", 4);
cars.put("Dacia", 10);

for (Map.Entry<String, Double> entry : fruitsPrice.entrySet()) {
    System.out.printf("%s -> %.2f%n", entry.getKey(), entry.getValue());
}
```
- Iterating through the Map using build-in method `forEach()`

```java live
Map<String, Integer> cars = new TreeMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 3);
cars.put("Opel", 4);
cars.put("Dacia", 10);

treeMap.forEach((key, value) -> System.out.println(key + " - " + value));
```

[/slide]

[slide]

# Sorting a Map

- Sorting according to Keys in ascending order

```java live
Map<String, Integer> cars = new HashMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 3);
cars.put("Opel", 4);
cars.put("Dacia", 1);

Map<String, Integer> sortedMap = cars
        .entrySet()
        .stream()

        // comparing the elements by its keys in ascending order
        // in case you want in descending order just swap 'a' and 'b'
        .sorted((a,b)->a.getKey().compareTo(b.getKey()))

        // saving the sorted items into new LinkedHashMap,
        // or you can print the elements directly using 'forEach()'
        .collect(Collectors
                .toMap(Map.Entry::getKey, Map.Entry::getValue,
        (oldValue, newValue) -> oldValue, LinkedHashMap::new));

sortedMap.forEach((k, v) -> System.out.println(k + " - " + v));
```


- Sorting according to Values in ascending order

```java live
Map<String, Integer> cars = new HashMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 3);
cars.put("Opel", 4);
cars.put("Dacia", 1);
        
cars.entrySet()
    .stream()
    // comparing the elements by its values in ascending order
    // in case you want in descending order just swap 'a' and 'b'
    .sorted((a,b)->a.getValue().compareTo(b.getValue()))

    // printing the elements directly using 'forEach()'
    .forEach(entry -> System.out.println(entry.getKey() + " - " + entry.getValue()));

```

- Sorting Map according to Values in ascending order if there is equals values then sort by the keys

```java live
Map<String, Integer> cars = new HashMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 1);
cars.put("Opel", 1);
cars.put("Dacia", 1);

cars.entrySet()
    .stream()
    .sorted((a,b)->{
        // compareTo() - returns 0 if the elements are equals
        int sort = a.getValue().compareTo(b.getValue());

        // if the values are equals compare by the keys
        if (sort == 0){
            // sorting by the keys
            return a.getKey().compareTo(b.getKey());
        }
        // in case there is no equal values
        return sort;
    })
    // printing the elements directly using 'forEach()'
    .forEach(entry -> System.out.println(entry.getKey() + " - " + entry.getValue()));

```



[/slide]