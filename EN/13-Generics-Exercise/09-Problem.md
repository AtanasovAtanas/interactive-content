[slide hideTitle]
# Problem: Custom List Iterator
[code-task title="Custom List Iterator" taskId="4a388940-1ad6-4118-be3f-f49c133366ae" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Extend the previous problem by making your custom list class to implement **Iterable**.

For the print command you have probably used a **for** loop.

This should allow you to iterate your list in a **foreach** statement.

## Examples
| **Input** | **Output** |
| --- | --- |
| Add aa | cc |
| Add bb | aa |
| Add cc | 2 |
| Max | cc |
| Min | bb |
| Greater aa | aa |
| Swap 0 2 |  |
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