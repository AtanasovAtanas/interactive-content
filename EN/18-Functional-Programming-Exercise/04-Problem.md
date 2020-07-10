[slide hideTitle]
# Problem: Applied Arithmetics
[code-task title="Applied Arithmetics" taskId="03caacb4-6d7d-40f1-b7b8-21d24988440a" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
On the first line, you receive a **list of numbers**.

On the next lines you are passed different **commands** that you need to apply to all numbers in the list: `add` -> adds 1; `multiply` -> multiplies by 2; `subtract` -> subtracts 1; `print` -> prints all numbers on **a new line**.

The input will end with a command `end`, after which you need to print the result.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 2 3 4 5 | 3 4 5 6 7 |
| add |  |
| add |  |
| print |  |
| end |  |

| **Input** | **Output** |
| --- | --- |
| 5 10 | 9 19 |
| multiply |  |
| subtract |  |
| print |  |
| end |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 2 3 4 5
add
add
print
end
[/input]
[output]
3 4 5 6 7
[/output]
[/test]
[test open]
[input]
5 10
multiply
subtract
print
end
[/input]
[output]
9 19
[/output]
[/test]
[test]
[input]
0 0
multiply
print
end
[/input]
[output]
0 0
[/output]
[/test]
[test]
[input]
0 0
multiply
subtract
print
end
[/input]
[output]
-1 -1
[/output]
[/test]
[test]
[input]
-1 -1
add
subtract
add
print
end
[/input]
[output]
0 0
[/output]
[/test]
[test]
[input]
2222222 2222224
add
print
add
print
end
[/input]
[output]
2222223 2222225
2222224 2222226
[/output]
[/test]
[test]
[input]
-2222224 -2222222
add
add
add
add
print
end
[/input]
[output]
-2222220 -2222218
[/output]
[/test]
[/tests]
[/code-task]
[/slide]