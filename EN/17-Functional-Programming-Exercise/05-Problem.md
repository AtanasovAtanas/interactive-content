[slide hideTitle]
# Problem: Reverse And Exclude
[code-task title="Reverse And Exclude" taskId="d727c084-1d8e-4dda-b653-498280a6764f" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that **reverses** a collection and **removes** elements that are **divisible** by a given integer **n**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 2 3 4 5 6 | 5 3 1 |
| 2 |  |

| **Input** | **Output** |
| --- | --- |
| 20 10 40 30 60 50 | 50 40 10 20 |
| 3 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 2 3 4 5 6
2
[/input]
[output]
5 3 1
[/output]
[/test]
[test open]
[input]
20 10 40 30 60 50
3
[/input]
[output]
50 40 10 20
[/output]
[/test]
[test]
[input]
10 9 8 7 6 5 4 3 2 1
2
[/input]
[output]
1 3 5 7 9
[/output]
[/test]
[test]
[input]
2 2 2 2 5 5 5 5
2
[/input]
[output]
5 5 5 5
[/output]
[/test]
[test]
[input]
10 9 8 7 6 5 4 3 2 1
3
[/input]
[output]
1 2 4 5 7 8 10
[/output]
[/test]
[test]
[input]
-1 -3 -5 5 3 1
3
[/input]
[output]
1 5 -5 -1
[/output]
[/test]
[test]
[input]
0 0 0
2
[/input]
[output]

[/output]
[/test]
[/tests]
[/code-task]
[/slide]