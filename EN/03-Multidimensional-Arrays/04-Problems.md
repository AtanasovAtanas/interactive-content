# Problems

[slide]
# Compare Matrices
[code-task title="Compare Matrices" taskId="e13fd83f-0adb-47b0-b590-e27920a40259" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that reads two integer matrices - `2D arrays` from the console and compares them element by element. 
For better code reusability, you could do the comparison in a method, which returns **true** if they are equal and **false** if not.
Each matrix definition on the console will contain a line with a positive integer number **R** – the number of rows in the matrix and **C** – the number of columns – followed by **R** lines containing the **C** numbers, separated by spaces (each line will have an equal amount of numbers.
The matrices will have at most **10** rows and at most **10** columns.
Print **equal** if the matrices match, and **not equal** if they don’t match.


## Examples
| **Input** | **Output** |
| --- | --- |
| 2 3 | equal |
| 1 2 3 |  |
| 2 1 3 |  |
| 2 3 |  |
| 1 2 3 |  |
| 2 1 3 |  |

| **Input** | **Output** |
| --- | --- |
| 2 3 | not equal |
| 1 2 3 |  |
| 4 5 6 |  |
| 2 2 |  |
| 1 3 |  |
| 4 5 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2 3
1 2 3
2 1 3
2 3
1 2 3
2 1 3
[/input]
[output]
equal
[/output]
[/test]
[test open]
[input]
2 3
1 2 3
4 5 6
2 2
1 3
4 5
[/input]
[output]
not equal
[/output]
[/test]
[test]
[input]
1 3
1 2 3
1 3
1 2 3
[/input]
[output]
equal
[/output]
[/test]
[test]
[input]
4 1
1
11
21
31
4 1
1
11
21
31
[/input]
[output]
equal
[/output]
[/test]
[test]
[input]
2 3
1 2 3
4 5 6
2 2
1 2
3 4
[/input]
[output]
not equal
[/output]
[/test]
[test]
[input]
3 1
1
2
3
4 1
1
2
3
5
[/input]
[output]
not equal
[/output]
[/test]
[test]
[input]
10 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
10 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
[/input]
[output]
equal
[/output]
[/test]
[test]
[input]
10 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
10 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 4
[/input]
[output]
not equal
[/output]
[/test]
[/tests]
[/code-task]
[/slide]