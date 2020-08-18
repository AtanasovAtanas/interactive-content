[slide hideTitle]
# Problem: Find The Smallest Element
[code-task title="Find The Smallest Element" taskId="7c7690a0-fb0d-441c-b6f7-ea852cc8ad84" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that is using a custom **function** (written by you) to find the **smallest** integer in a **sequence** of **integers**.

The input could have more than one space.

Your task is to **collect** the integers from the console, find the **smallest one**, and print its **index**. 

If **more** than one such element exists, print the index of the **rightmost** one.

## Hints
- Use a `Function<List<Integer>, Integer>` or something similar.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 2 3 0 4 5 6 | 3 |

| **Input** | **Output** |
| --- | --- |
| 123 10 11 3 | 3 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 2 3 0 4 5 6
[/input]
[output]
3
[/output]
[/test]
[test open]
[input]
123 10 11 3
[/input]
[output]
3
[/output]
[/test]
[test]
[input]
1 1 1 1 1
[/input]
[output]
4
[/output]
[/test]
[test]
[input]
78
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
-20
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
1 2 3 4 5 11
[/input]
[output]
0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]