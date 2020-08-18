[slide hideTitle]
# Problem: Generic Count Method Double
[code-task title="Generic Count Method Double" taskId="39f0850a-cf23-47af-9bd9-554c556a4a92" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create a **method** that receives as argument a **list of Double** and an **element of the given type**.

The method should **return the count of elements that are greater than the value of the given element**.

**Modify your Box class** to support **comparing by value** of the data stored.

On the **first line**, you will receive **n** - the number of elements to add to the list. 

On the next **n** lines, you will receive the actual elements. 

On the **last line**, you will get the value of the element to which you need to compare every element in the list.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | 2 |
| 7.13 |  |
| 123.22 |  |
| 42.78 |  |
| 7.55 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
7.13
123.22
42.78
7.55
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
5
[/output]
[/test]
[test]
[input]
1
1231542.123
1
[/input]
[output]
1
[/output]
[/test]
[test]
[input]
3
-1
0
1
-1
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
5
11.11
22.22
33.33
44.44
55.55
66.66
[/input]
[output]
0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]