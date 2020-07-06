[slide hideTitle]
# Problem: Custom List
[code-task title="Custom List" taskId="42476d13-5009-4c80-bc9d-fc56eaa7228f" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create a generic data structure that can store **any type** that can be **compared**.

Implement functions:

- `void add(T element)`
- `T remove(int index)`
- `boolean contains(T element)`
- `void swap(int index, int index)`
- `int countGreaterThan(T element)`
- `T getMax()`
- `T getMin()`

Create a command interpreter that reads commands and modifies the custom list that you have created. Implement the commands:

- `Add <element>` - Adds the given element to the end of the list
- `Remove <index>` - Removes the element at the given index
- `Contains <element>` - Prints if the list contains the given element **(true or false)**
- `Swap <index> <index>` - Swaps the elements at the given indexes
- `Greater <element>` - Counts the elements that are greater than the given element and prints their count
- `Max` - Prints the maximum element in the list
- `Min` - Prints the minimum element in the list
- `Print` - Prints all elements in the list, each on a separate line
- `END` - stops the reading of commands

**Note** : For the **tests**, use **String** as **T**.

## Examples
| **Input** | **Output** |
| --- | --- |
| Add aa | cc |
| Add bb | aa |
| Add cc | 2 |
| Max | true |
| Min | cc |
| Greater aa | bb |
| Swap 0 2 | aa |
| Contains aa |  |
| Print |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Add aa
Add bb
Add cc
Max
Min
Greater aa
Swap 0 2
Contains aa
Print
END
[/input]
[output]
cc
aa
2
true
cc
bb
aa
[/output]
[/test]
[test]
[input]
Add P
Print
END
[/input]
[output]
P
[/output]
[/test]
[test]
[input]
Add P
Add G
Max
END
[/input]
[output]
P
[/output]
[/test]
[test]
[input]
Add P
Add G
Swap 0 0
Swap 1 1
Swap 0 1
Swap 1 0
Swap 0 1
Print
END
[/input]
[output]
G
P
[/output]
[/test]
[test]
[input]
Add P
Add G
Contains 123
Contains falsd
Contains @\#!@\\$
Contains .
Contains P
Contains G
Greater P
Greater G
Greater aa
Greater zz
Greater true
Greater false
Greater 123
Greater ...
Greater @\#%!@\#
END
[/input]
[output]
false
false
false
false
true
true
0
1
0
0
0
0
2
2
2
[/output]
[/test]
[test]
[input]
Add a
Add b
Add c
Add d
Add e
Add f
Print
Max
Min
Greater a
Greater b
Greater c
Greater d
Greater e
Greater f
Remove 0
Remove 0
Remove 0
Print
END
[/input]
[output]
a
b
c
d
e
f
f
a
5
4
3
2
1
0
d
e
f
[/output]
[/test]
[/tests]
[/code-task]
[/slide]