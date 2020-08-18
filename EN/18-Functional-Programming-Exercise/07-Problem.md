[slide hideTitle]
# Problem: Custom Comparator
[code-task title="Custom Comparator" taskId="76eba80c-8397-4782-819c-652aa05fca1e" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a custom **comparator** that **sorts** all even numbers before all **odd** ones in **ascending order**.

Pass it to an `Arrays.sort()` function and print the result.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 2 3 4 5 6 | 2 4 6 1 3 5 |

| **Input** | **Output** |
| --- | --- |
| -3 2 | 2 -3 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 2 3 4 5 6
[/input]
[output]
2 4 6 1 3 5
[/output]
[/test]
[test open]
[input]
-3 2
[/input]
[output]
2 -3
[/output]
[/test]
[test]
[input]
1 2 3
[/input]
[output]
2 1 3
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
[test]
[input]
-1 -1 -1 1 1 1
[/input]
[output]
-1 -1 -1 1 1 1
[/output]
[/test]
[test]
[input]
2222222 2222223 2222224 -2222222 -2222223 -2222224
[/input]
[output]
-2222224 -2222222 2222222 2222224 -2222223 2222223
[/output]
[/test]
[test]
[input]
1 2 -1 2 5 -6 7 9 10 90 -2124412 2 3 5 19 288
[/input]
[output]
-2124412 -6 2 2 2 10 90 288 -1 1 3 5 5 7 9 19
[/output]
[/test]
[/tests]
[/code-task]
[/slide]