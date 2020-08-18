[slide hideTitle]
# Problem: Reverse Number with a Stack
[code-task title="Reverse Number with a Stack" taskId="ae951105-27c4-4679-ae94-338038b57663" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
Write a program that reads **N integers** from the console and **reverses them using a stack**.

Use the **ArrayDeque\&lt;Integer\&gt;** class.

Just put the input numbers in the stack and pop them.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 2 3 4 5 | 5 4 3 2 1 |


| **Input** | **Output** |
| --- | --- |
| 1 | 1 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 2 3 4 5
[/input]
[output]
5 4 3 2 1
[/output]
[/test]
[test]
[input]
1 1 3 5 8 13 21
[/input]
[output]
21 13 8 5 3 1 1
[/output]
[/test]
[test]
[input]
1
[/input]
[output]
1
[/output]
[/test]
[test]
[input]
10 11 12 13 14 15
[/input]
[output]
15 14 13 12 11 10
[/output]
[/test]
[test]
[input]
1 -2
[/input]
[output]
-2 1
[/output]
[/test]
[test]
[input]
0 0 0 0 0
[/input]
[output]
0 0 0 0 0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
