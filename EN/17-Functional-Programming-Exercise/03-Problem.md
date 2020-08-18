[slide hideTitle]
# Problem: Custom Min Function
[code-task title="Custom Min Function" taskId="7f5f070e-8a9b-46a4-8155-93e23f1084a3" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a simple program that **reads** a **set of numbers** from the console and finds the **smallest** of the **numbers** using a simple `Function<Integer[], Integer>`.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 4 3 2 1 7 13 | 1 |

| **Input** | **Output** |
| --- | --- |
| 4 5 -2 3 -5 8 | -5 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 4 3 2 1 7 13
[/input]
[output]
1
[/output]
[/test]
[test open]
[input]
4 5 -2 3 -5 8
[/input]
[output]
-5
[/output]
[/test]
[test]
[input]
1 1 1 1 1 1 1 1 1
[/input]
[output]
1
[/output]
[/test]
[test]
[input]
-1
[/input]
[output]
-1
[/output]
[/test]
[test]
[input]
1 2 3 -1
[/input]
[output]
-1
[/output]
[/test]
[test]
[input]
2 3
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
-1 -2 -3
[/input]
[output]
-3
[/output]
[/test]
[/tests]
[/code-task]
[/slide]