

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

- Initialization:
```java
Set<String> tree = new TreeSet<>();
```

- Adding Elements 
```java live
Set<Integer> tree = new TreeSet<>();

List<Integer> data = Arrays.asList(40,20,30,10,50,10,10,10);

tree.addAll(data);

System.out.println(tree);
```

**LinkedHashSet**

A **LinkedHashSet** is an **ordered version of HashSet** that maintains a doubly-linked List across all elements.

A **LinkedHashSet** provides **constant** time performance for the basic operations - `add()`, `contains()` and `remove()`.

A LinkedHashSet allows maximum **one null element**.

- Initialization:
```java
Set<String> linkedHashSet = new LinkedHashSet<>();
```

- Adding Elements 
```java live
Set<Integer> linkedHashSet = new LinkedHashSet<>();

List<Integer> data = Arrays.asList(40,20,30,10,50,10,10,10);

linkedHashSet.addAll(data);

System.out.println(linkedHashSet);
```
[/slide]

[slide]
# Problem: Parking Lot
[code-task title="Parking Lot" taskId="3a94dfc6-efac-41fb-a81a-1e09ddb41e79" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that:
 - Records car number for every car that enter in the parking lot
 - Removes car number when the car goes out
## Input
The input will be string in format [direction, carNumber]
The input ends with string "**END**"
## Output
Print the output with all car numbers which are in parking lot 

## Examples
| **Input** | **Output** |
| --- | --- |
| IN, CA2844AA | CA9999TT |
| IN, CA1234TA | CA2844AA |
| OUT, CA2844AA | CA9876HH |
| IN, CA9999TT | CA2822UU |
| IN, CA2866HI |  |
| OUT, CA1234TA |  |
| IN, CA2844AA |  |
| OUT, CA2866HI |  |
| IN, CA9876HH |  |
| IN, CA2822UU |  |
| END |  |

| **Input** | **Output** |
| --- | --- |
| IN, CA2844AA | Parking Lot is Empty |
| IN, CA1234TA |  |
| OUT, CA2844AA |  |
| OUT, CA1234TA |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
IN, CA2844AA
IN, CA1234TA
OUT, CA2844AA
IN, CA9999TT
IN, CA2866HI
OUT, CA1234TA
IN, CA2844AA
OUT, CA2866HI
IN, CA9876HH
IN, CA2822UU
END
[/input]
[output]
CA2822UU
CA2844AA
CA9999TT
CA9876HH
[/output]
[/test]
[test open]
[input]
IN, CA2844AA
IN, CA1234TA
OUT, CA2844AA
OUT, CA1234TA
END
[/input]
[output]
Parking Lot is Empty
[/output]
[/test]
[test]
[input]
IN, CA2844AA
IN, CA1234TA
IN, CA9999TT
IN, CA2866HI
IN, CA2844AA
IN, CA9876HH
IN, CA2822UU
END
[/input]
[output]
CA2866HI
CA1234TA
CA2822UU
CA2844AA
CA9999TT
CA9876HH
[/output]
[/test]
[test]
[input]
END
[/input]
[output]
Parking Lot is Empty
[/output]
[/test]
[test]
[input]
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
END
[/input]
[output]
Parking Lot is Empty
[/output]
[/test]
[test]
[input]
IN, CA2844AA
IN, CA1234TA
IN, CA9999TT
IN, CA2866HI
IN, CA2844AA
IN, CA9876HH
IN, CA2822UU
OUT, CA2844AA
OUT, CA1234TA
OUT, CA9999TT
OUT, CA2866HI
OUT, CA2844AA
OUT, CA9876HH
END
[/input]
[output]
CA2822UU
[/output]
[/test]
[test]
[input]
IN, CA2844AA
IN, CA1234TA
IN, CA9999TT
IN, CA2866HI
IN, CA2844AA
IN, CA9876HH
IN, CA2822UU
IN, CA2844AA
IN, CA1234TA
IN, CA9999TT
IN, CA2866HI
IN, CA2844AA
IN, CA9876HH
IN, CA2822UU
END
[/input]
[output]
CA2866HI
CA1234TA
CA2822UU
CA2844AA
CA9999TT
CA9876HH
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Parking Lot
[code-task title="Parking Lot" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        LinkedHashSet<String> parkingLot = new LinkedHashSet<>();

        String input = sc.nextLine();
        while (!input.equals("END")) {

            String[] reminder = input.split(", ");
            if (reminder[0].equals("IN")) {
                parkingLot.add(reminder[1]);
            } else {
                parkingLot.remove(reminder[1]);
            }
            input = sc.nextLine();
        }

        if (parkingLot.isEmpty()){
            System.out.println("Parking Lot is Empty");
        }else{
            parkingLot.forEach(System.out::println);
        }
    }
}
```
[/code-editor]
[task-description]
## Description
Write a program that:
 - Records car number for every car that enter in the parking lot
 - Removes car number when the car goes out
## Input
The input will be string in format [direction, carNumber]
The input ends with string "**END**"
## Output
Print the output with all car numbers which are in parking lot 

## Examples
| **Input** | **Output** |
| --- | --- |
| IN, CA2844AA | CA9999TT |
| IN, CA1234TA | CA2844AA |
| OUT, CA2844AA | CA9876HH |
| IN, CA9999TT | CA2822UU |
| IN, CA2866HI |  |
| OUT, CA1234TA |  |
| IN, CA2844AA |  |
| OUT, CA2866HI |  |
| IN, CA9876HH |  |
| IN, CA2822UU |  |
| END |  |

| **Input** | **Output** |
| --- | --- |
| IN, CA2844AA | Parking Lot is Empty |
| IN, CA1234TA |  |
| OUT, CA2844AA |  |
| OUT, CA1234TA |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
IN, CA2844AA
IN, CA1234TA
OUT, CA2844AA
IN, CA9999TT
IN, CA2866HI
OUT, CA1234TA
IN, CA2844AA
OUT, CA2866HI
IN, CA9876HH
IN, CA2822UU
END
[/input]
[output]
CA9999TT
CA2844AA
CA9876HH
CA2822UU
[/output]
[/test]
[test open]
[input]
IN, CA2844AA
IN, CA1234TA
OUT, CA2844AA
OUT, CA1234TA
END
[/input]
[output]
Parking Lot is Empty
[/output]
[/test]
[test]
[input]
IN, CA2844AA
IN, CA1234TA
IN, CA9999TT
IN, CA2866HI
IN, CA2844AA
IN, CA9876HH
IN, CA2822UU
END
[/input]
[output]
CA2844AA
CA1234TA
CA9999TT
CA2866HI
CA9876HH
CA2822UU
[/output]
[/test]
[test]
[input]
END
[/input]
[output]
Parking Lot is Empty
[/output]
[/test]
[test]
[input]
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
IN, CA2844AA
OUT, CA2844AA
END
[/input]
[output]
Parking Lot is Empty
[/output]
[/test]
[test]
[input]
IN, CA2844AA
IN, CA1234TA
IN, CA9999TT
IN, CA2866HI
IN, CA2844AA
IN, CA9876HH
IN, CA2822UU
OUT, CA2844AA
OUT, CA1234TA
OUT, CA9999TT
OUT, CA2866HI
OUT, CA2844AA
OUT, CA9876HH
END
[/input]
[output]
CA2822UU
[/output]
[/test]
[test]
[input]
IN, CA2844AA
IN, CA1234TA
IN, CA9999TT
IN, CA2866HI
IN, CA2844AA
IN, CA9876HH
IN, CA2822UU
IN, CA2844AA
IN, CA1234TA
IN, CA9999TT
IN, CA2866HI
IN, CA2844AA
IN, CA9876HH
IN, CA2822UU
END
[/input]
[output]
CA2844AA
CA1234TA
CA9999TT
CA2866HI
CA9876HH
CA2822UU
[/output]
[/test]
[/tests]
[/code-task]
[/slide]