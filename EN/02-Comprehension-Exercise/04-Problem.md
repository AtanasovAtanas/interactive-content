[slide hideTitle]
# Problem: Flatten lists
[code-task title="Problem: Flatten lists" taskId="c3422572-26d7-4d49-bb90-0e22c321de9f" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Write a program to flatten **several lists** of numbers, received in the following format:

 - String with numbers separated by '\|'.
 - Values are separated by spaces (' ', one or several).
 - Order the output list from the **last** to the **first received**, and their values from **left** to **right** as shown below.

## Examples
| **Input** | **Output** |
| --- | --- |
| 1 2 3 \|4 5 6 \|  7  8 | 7 8 4 5 6 1 2 3 |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 7 \| 4  5\|1 0\| 2 5 \|3 | 3 2 5 1 0 4 5 7 |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 1\| 4 5 6 7  \|  8 9 \| 8 9 4 5 6 7 1 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1 2 3 \|4 5 6 \|  7  8
[/input]
[output]
7 8 4 5 6 1 2 3
[/output]
[/test]
[test open]
[input]
7 \| 4  5\|1 0\| 2 5 \|3
[/input]
[output]
3 2 5 1 0 4 5 7
[/output]
[/test]
[test open]
[input]
1\| 4 5 6 7 \| 8 9
[/input]
[output]
8 9 4 5 6 7 1
[/output]
[/test]
[test]
[input]
7 \| 4  5\|1 0\| 2 5 \|3
[/input]
[output]
3 2 5 1 0 4 5 7
[/output]
[/test]
[test]
[input]
1\| 4 5 6 7 \| 8 9
[/input]
[output]
8 9 4 5 6 7 1
[/output]
[/test]
[test]
[input]
1 \| \| \|\|\|2   3 \|4   5 6 \| 7 8\| -3 2   1\|\|1 2\|3\|4\|99 77
[/input]
[output]
99 77 4 3 1 2 -3 2 1 7 8 4 5 6 2 3 1
[/output]
[/test]
[/tests]
[/code-task]
[/slide]