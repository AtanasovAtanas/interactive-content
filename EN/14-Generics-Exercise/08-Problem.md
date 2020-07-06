[slide hideTitle]
# Problem: Custom List Sorted
[code-task title="Custom List Sorted" taskId="b8e8dbc0-86c7-418f-917a-25f4f532c571" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Extend the previous problem by creating an additional **Sorter class**. 

It should have a single static method `sort()` which can sort objects of type **CustomList** containing any type that can be compared.

**Extend the command list** to support one additional command:

- `Sort` - Sort the elements in the list in ascending order.


## Examples
| **Input** | **Output** |
| --- | --- |
| Add cc | aa |
| Add bb | bb |
| Add aa | cc |
| Sort |  |
| Print |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Add cc
Add bb
Add aa
Sort
Print
END
[/input]
[output]
aa
bb
cc
[/output]
[/test]
[test]
[input]
Add P
Sort
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
Sort
Print
END
[/input]
[output]
P
G
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
Sort
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
Sort
Swap 0 1
Print
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
P
G
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
Sort
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