

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

[slide]
# Problem: SoftUni Party
[code-task title="Problem: SoftUni Party" taskId="9731adb3-e6c2-449b-9e28-79d29de7caa4" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
There is a party in SoftUni. Many guests are invited, and they are two types: **VIP** and **regular**. 
When guest comes, you have to check if he/she exist in any of two reservation lists.
All reservation numbers will be with 8 chars.
All VIP numbers start with digit.
There will be 2 command lines:
 - First is "PARTY" - party is on and guests start coming.
 - Second is "END" - then party is over, and no more guest will come.
Output shows all guests, who didn't come to the party (**VIP must be first**).



## Examples
| **Input** | **Output** |
| --- | --- |
| 7IK9Yo0h | 2 |
| 9NoBUajQ | 7IK9Yo0h |
| Ce8vwPmE | tSzE5t0p |
| SVQXQCbc |  |
| tSzE5t0p |  |
| PARTY |  |
| 9NoBUajQ |  |
| Ce8vwPmE |  |
| SVQXQCbc |  |
| END |  |

| **Input** | **Output** |
| --- | --- |
| m8rfQBvl | 2 |
| fc1oZCE0 | MDzcM9ZK |
| UgffRkOn | xys2FYzn |
| 7ugX7bm0 |  |
| 9CQBGUeJ |  |
| 2FQZT3uC |  |
| dziNz78I |  |
| mdSGyQCJ |  |
| LjcVpmDL |  |
| fPXNHpm1 |  |
| HTTbwRmM |  |
| B5yTkMQi |  |
| 8N0FThqG |  |
| xys2FYzn |  |
| MDzcM9ZK |  |
| PARTY |  |
| 2FQZT3uC |  |
| dziNz78I |  |
| mdSGyQCJ |  |
| LjcVpmDL |  |
| fPXNHpm1 |  |
| HTTbwRmM |  |
| B5yTkMQi |  |
| 8N0FThqG |  |
| m8rfQBvl |  |
| fc1oZCE0 |  |
| UgffRkOn |  |
| 7ugX7bm0 |  |
| 9CQBGUeJ |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
7IK9Yo0h
9NoBUajQ
Ce8vwPmE
SVQXQCbc
tSzE5t0p
PARTY
9NoBUajQ
Ce8vwPmE
SVQXQCbc
END
[/input]
[output]
2
7IK9Yo0h
tSzE5t0p
[/output]
[/test]
[test open]
[input]
m8rfQBvl
fc1oZCE0
UgffRkOn
7ugX7bm0
9CQBGUeJ
2FQZT3uC
dziNz78I
mdSGyQCJ
LjcVpmDL
fPXNHpm1
HTTbwRmM
B5yTkMQi
8N0FThqG
xys2FYzn
MDzcM9ZK
PARTY
2FQZT3uC
dziNz78I
mdSGyQCJ
LjcVpmDL
fPXNHpm1
HTTbwRmM
B5yTkMQi
8N0FThqG
m8rfQBvl
fc1oZCE0
UgffRkOn
7ugX7bm0
9CQBGUeJ
END
[/input]
[output]
2
MDzcM9ZK
xys2FYzn
[/output]
[/test]
[test]
[input]
m8rfQBvl
fc1oZCE0
UgffRkOn
7ugX7bm0
9CQBGUeJ
2FQZT3uC
dziNz78I
mdSGyQCJ
LjcVpmDL
fPXNHpm1
HTTbwRmM
B5yTkMQi
8N0FThqG
xys2FYzn
MDzcM9ZK
PARTY
m8rfQBvl
fc1oZCE0
UgffRkOn
7ugX7bm0
9CQBGUeJ
2FQZT3uC
dziNz78I
mdSGyQCJ
LjcVpmDL
fPXNHpm1
HTTbwRmM
B5yTkMQi
8N0FThqG
xys2FYzn
MDzcM9ZK
END
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
PARTY
END
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
m8rfQBvl
fc1oZCE0
UgffRkOn
7ugX7bm0
9CQBGUeJ
2FQZT3uC
dziNz78I
mdSGyQCJ
LjcVpmDL
fPXNHpm1
HTTbwRmM
B5yTkMQi
8N0FThqG
xys2FYzn
MDzcM9ZK
PARTY
END
[/input]
[output]
15
2FQZT3uC
7ugX7bm0
8N0FThqG
9CQBGUeJ
B5yTkMQi
HTTbwRmM
LjcVpmDL
MDzcM9ZK
UgffRkOn
dziNz78I
fPXNHpm1
fc1oZCE0
m8rfQBvl
mdSGyQCJ
xys2FYzn
[/output]
[/test]
[test]
[input]
7IK9Yo0h
9NoBUajQ
Ce8vwPmE
SVQXQCbc
tSzE5t0p
PARTY
9NoBUajQ
Ce8vwPmE
SVQXQCbc
END
[/input]
[output]
2
7IK9Yo0h
tSzE5t0p
[/output]
[/test]
[test]
[input]
m8rfQBvl
fc1oZCE0
UgffRkOn
7ugX7bm0
9CQBGUeJ
2FQZT3uC
dziNz78I
mdSGyQCJ
LjcVpmDL
fPXNHpm1
HTTbwRmM
B5yTkMQi
8N0FThqG
xys2FYzn
MDzcM9ZK
PARTY
2FQZT3uC
dziNz78I
mdSGyQCJ
LjcVpmDL
fPXNHpm1
HTTbwRmM
B5yTkMQi
8N0FThqG
m8rfQBvl
fc1oZCE0
UgffRkOn
7ugX7bm0
9CQBGUeJ
END
[/input]
[output]
2
MDzcM9ZK
xys2FYzn
[/output]
[/test]
[/tests]
[/code-task]
[/slide]