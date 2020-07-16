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
# Built-in methods

- `put(K key, V value)` - **add items** (insert an entry) in the map. 

Only a **single Key + Value pair** for each Key can exist in the Map **at the same time**. 

If `put()` is called more than once with the same Key, **the latest Value** passed to `put()` for that Key will **overwrite** what is already stored in the Map for that Key. 

**The latest Value replaces the existing Value** for the given Key.

```java
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Boeing 737", 130);
airplanes.put("Airbus A320", 150);
```

- `putIfAbsent(K key, V value)` - insert the specified Value with the specified Key in the Map only if it is **not already existing**

```java live
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Boeing 737", 130);
airplanes.putIfAbsent("Boeing 737", 100);
System.out.println(airplanes.get("Boeing 737"));
```

- `get(K key)` - **access a Value** in the Map using its Key and **return the Value** object
```java live
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Boeing 737", 130);
int peopleCount = airplanes.get("Boeing 737");
System.out.println(peopleCount);
```

- `remove(K key)` - **delete** an item (entry) **using its Key**
```java live
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Boeing 737", 130);
airplanes.remove("Boeing 737");
System.out.println(airplanes.get("Boeing 737"));
```

- `clear()` - remove all items (entries) in the map, reset the Map
```java live
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Boeing 737", 130);
airplanes.put("Airbus A320", 150);
airplanes.clear();
System.out.println(airplanes.get("Boeing 737"));
System.out.println(airplanes.get("Airbus A320"));
```

- `size()` - return the **number of items (entries)** in the Map
```java live
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Boeing 737", 130);
airplanes.put("Airbus A320", 150);
System.out.println(airplanes.size());
```

- `containsKey(K key)` - check **if there is such Key object** in the Map and if there is return `true`, else return `false`
```java live
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Airbus A320", 150);
if (airplanes.containsKey("Airbus A320")) {
    System.out.println("Airbus A320 key exists.");
}
```

- `containsValue(V value)` - check **if there is such Value object** in the Map and if there is return `true`, else return `false`
```java live
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Airbus A320", 150);
System.out.println(airplanes.containsValue(150));
System.out.println(airplanes.containsValue(100));
```

- `isEmpty()` - return `true` if the Map is **empty** and `false` if it contains **at least one Key**
```java live
HashMap<String, Integer> airplanes = new HashMap<>();
System.out.println(airplanes.isEmpty());
```

```java live
HashMap<String, Integer> airplanes = new HashMap<>();
airplanes.put("Boeing 737", 130);
System.out.println(airplanes.isEmpty());
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
Map<String, Integer> cars = new LinkedHashMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 3);
cars.put("Opel", 4);
cars.put("Dacia", 10);

for (Integer number : cars.values()) {
    System.out.println(number);
}
```

- Iterating through the items of a map using the built-in method `entrySet()`
  - `entry.getKey()` - obtain the Keys
  - `entry.getValue()` - obtain the Values

```java live
Map<String, Integer> cars = new LinkedHashMap<>();

cars.put("BMW", 5);
cars.put("Mercedes", 3);
cars.put("Opel", 4);
cars.put("Dacia", 10);

for (Map.Entry<String, Integer> entry : cars.entrySet()) {
    System.out.printf("%s -> %.2f%n", entry.getKey(), entry.getValue());
}
```
- Iterating through the Map using built-in method `forEach()`

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

```java live no-template
import java.util.*;
import java.util.stream.Collectors;

public class Main {
    public static void main(String[] args) {

        Map<String, Integer> cars = new HashMap<>();

        cars.put("BMW", 5);
        cars.put("Mercedes", 3);
        cars.put("Opel", 2);
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
    }
}
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

[slide]
# Problem: Count Real Numbers
[code-task title="Count Real Numbers" taskId="652e7421-f805-48bb-ac97-88e91f56fcc4" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
Write a program that counts the occurrence of real numbers.

The input is a single line with real numbers separated by spaces.

Print the numbers in the order of appearance.

All numbers must be formatted to one digit after the decimal point.

## Examples
| **Input** | **Output** |
| --- | --- |
| -2.5 4 3 -2.5 -5.5 4 3 3 -2.5 3 | -2.5 -> 3 |
|  | 4.0 -> 2 |
|  | 3.0 -> 4 |
|  | -5.5 -> 1 |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 2.3 4.5 4.5 5.5 5.5 2.3 3.0 3.0 4.5 4.5 3.0 3.0 4.0 3.0 5.5 3.0 2.3 5.5 4.5 3.0 | 2.3 -> 3 |
|  | 4.5 -> 5 |
|  | 5.5 -> 4 |
|  | 3.0 -> 7 |
|  | 1.0	-> 1 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
-2.5 4 3 -2.5 -5.5 4 3 3 -2.5 3
[/input]
[output]
-2.5 -\> 3
4.0 -\> 2
3.0 -\> 4
-5.5 -\> 1
[/output]
[/test]
[test open]
[input]
2.3 4.5 4.5 5.5 5.5 2.3 3.0 3.0 4.5 4.5 3.0 3.0 4.0 3.0 5.5 3.0 2.3 5.5 4.5 3.0
[/input]
[output]
2.3 -\> 3
4.5 -\> 5
5.5 -\> 4
3.0 -\> 7
4.0 -\> 1
[/output]
[/test]
[test]
[input]
13 23 42 69 13 23 42 69 13 23 42 69 13 23 42 69 13 23 42 69
[/input]
[output]
13.0 -\> 5
23.0 -\> 5
42.0 -\> 5
69.0 -\> 5
[/output]
[/test]
[test]
[input]
1.111
[/input]
[output]
1.1 -\> 1
[/output]
[/test]
[test]
[input]
23 23 23 23 2 3 23 23 23 23 23 232 232 2323 23 23232
[/input]
[output]
23.0 -\> 10
2.0 -\> 1
3.0 -\> 1
232.0 -\> 2
2323.0 -\> 1
23232.0 -\> 1
[/output]
[/test]
[test]
[input]
-3 -3 -3 -3 -3 -3 -3 -3 -3 -3 -3 -3 -3 -3
[/input]
[output]
-3.0 -\> 14
[/output]
[/test]
[test]
[input]
0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9
[/input]
[output]
0.0 -\> 10
1.0 -\> 10
2.0 -\> 10
3.0 -\> 10
4.0 -\> 10
5.0 -\> 10
6.0 -\> 10
7.0 -\> 10
8.0 -\> 10
9.0 -\> 10
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Count Real Numbers
[code-task title="Count Real Numbers" taskId="652e7421-f805-48bb-ac97-88e91f56fcc4" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        double[] input = Arrays
        .stream(scanner.nextLine()
        .split("\\s+"))
        .mapToDouble(Double::parseDouble)
        .toArray();

        LinkedHashMap<Double, Integer> result = new LinkedHashMap<>();

        for (Double number : input) {
            if (!result.containsKey(number)) {
                result.put(number, 1);
            } else {
                result.put(number, result.get(number) + 1);
            }
        }
        for (Double key : result.keySet()) {
            System.out.printf("%.1f -> %d", key, result.get(key));
        }
    }
}
```
[/code-editor]
[task-description]
## Description
Write a program that counts the occurrence of real numbers.

The input is a single line with real numbers separated by spaces.

Print the numbers in the order of appearance.

All numbers must be formatted to one digit after the decimal point.

## Examples
| **Input** | **Output** |
| --- | --- |
| -2.5 4 3 -2.5 -5.5 4 3 3 -2.5 3 | -2.5 -> 3 |
|  | 4.0 -> 2 |
|  | 3.0 -> 4 |
|  | -5.5 -> 1 |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 2.3 4.5 4.5 5.5 5.5 2.3 3.0 3.0 4.5 4.5 3.0 3.0 4.0 3.0 5.5 3.0 2.3 5.5 4.5 3.0 | 2.3 -> 3 |
|  | 4.5 -> 5 |
|  | 5.5 -> 4 |
|  | 3.0 -> 7 |
|  | 1.0	-> 1 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
-2.5 4 3 -2.5 -5.5 4 3 3 -2.5 3
[/input]
[output]
-2.5 -\> 3
4.0 -\> 2
3.0 -\> 4
-5.5 -\> 1
[/output]
[/test]
[test open]
[input]
2.3 4.5 4.5 5.5 5.5 2.3 3.0 3.0 4.5 4.5 3.0 3.0 4.0 3.0 5.5 3.0 2.3 5.5 4.5 3.0
[/input]
[output]
2.3 -\> 3
4.5 -\> 5
5.5 -\> 4
3.0 -\> 7
4.0 -\> 1
[/output]
[/test]
[test]
[input]
13 23 42 69 13 23 42 69 13 23 42 69 13 23 42 69 13 23 42 69
[/input]
[output]
13.0 -\> 5
23.0 -\> 5
42.0 -\> 5
69.0 -\> 5
[/output]
[/test]
[test]
[input]
1.111
[/input]
[output]
1.1 -\> 1
[/output]
[/test]
[test]
[input]
23 23 23 23 2 3 23 23 23 23 23 232 232 2323 23 23232
[/input]
[output]
23.0 -\> 10
2.0 -\> 1
3.0 -\> 1
232.0 -\> 2
2323.0 -\> 1
23232.0 -\> 1
[/output]
[/test]
[test]
[input]
-3 -3 -3 -3 -3 -3 -3 -3 -3 -3 -3 -3 -3 -3
[/input]
[output]
-3.0 -\> 14
[/output]
[/test]
[test]
[input]
0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9
[/input]
[output]
0.0 -\> 10
1.0 -\> 10
2.0 -\> 10
3.0 -\> 10
4.0 -\> 10
5.0 -\> 10
6.0 -\> 10
7.0 -\> 10
8.0 -\> 10
9.0 -\> 10
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
