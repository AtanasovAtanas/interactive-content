[slide hideTitle]
# Problem: Generic Count Method String
[code-task title="Generic Count Method String" taskId="51f3851c-949d-4923-acaa-88e3224e30c9" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create a **method** that receives as argument a **list of any type that can be compared** and an **element of the given type**.

The method should **return the count of elements that are greater than the value of the given element**.

**Modify your Box class** to support **comparing by value** of the data stored.

On the first line you will receive **n** - the number of elements to add to the list. 

On the next **n** lines, you will receive the actual elements. 

On the **last line** you will get the value of the element to which you need to compare every element in the list.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | 2 |
| aa |  |
| aaa |  |
| bb |  |
| aa |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
aa
aaa
bb
aa
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
3
1
2
3
1
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
5
12
13
14
15
16
3
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
1
aaa
aa
[/input]
[output]
1
[/output]
[/test]
[test]
[input]
10
a
b
c
d
e
f
g
h
i
j
k
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
5
p
pp
ppp
pppp
ppppp
pp
[/input]
[output]
3
[/output]
[/test]
[/tests]
[/code-task]
[/slide]