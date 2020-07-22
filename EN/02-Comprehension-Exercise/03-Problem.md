# Problem: Number Classification

[slide]
# Video

[vimeo-video]
[stream language="EN" videoId="435704471" default /]
[stream language="RO" videoId="436342752"  /]
[/video-vimeo]
[/slide]

[slide hideTitle]
# Problem: Number Classification
[code-task title="Problem: Number Classification" taskId="1002ef9b-f0e9-4d80-bd53-d221a3870113" executionType="tests-execution" executionStrategy="python-code" requiresInput]
[code-editor language=python]
```
# Write your code here
```
[/code-editor]
[task-description]
## Description
Using **list comprehension** write a program that receives numbers separated by comma and space ", " and prints all the **positive**, **negative**, **even** and **odd** numbers on separate lines as shown below.

**Note: Zero (0) is counted for a positive number.**

## Examples
| **Input** | **Output** |
| --- | --- |
| 1, -2, 0, 5, 3, 4, -100, -20, 12, 19, -33 | Positive: 1, 0, 5, 3, 4, 12, 19 |
|  | Negative: -2, -100, -20, -33 |
|  | Even: -2, 0, 4, -100, -20, 12 |
|  | Odd: 1, 5, 3, 19, -33 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1, -2, 0, 5, 3, 4, -100, -20, 12, 19, -33
[/input]
[output]
Positive\: 1, 0, 5, 3, 4, 12, 19
Negative\: -2, -100, -20, -33
Even\: -2, 0, 4, -100, -20, 12
Odd\: 1, 5, 3, 19, -33
[/output]
[/test]
[test]
[input]
1, 2, 53, 2, 21
[/input]
[output]
Positive\: 1, 2, 53, 2, 21
Negative\:
Even\: 2, 2
Odd\: 1, 53, 21
[/output]
[/test]
[test]
[input]
22, 44, 66, 88
[/input]
[output]
Positive\: 22, 44, 66, 88
Negative\:
Even\: 22, 44, 66, 88
Odd\:
[/output]
[/test]
[test]
[input]
-19, -4, -24, -99, -49
[/input]
[output]
Positive\:
Negative\: -19, -4, -24, -99, -49
Even\: -4, -24
Odd\: -19, -99, -49
[/output]
[/test]
[test]
[input]
-1, -3, -5, -7, -9
[/input]
[output]
Positive\:
Negative\: -1, -3, -5, -7, -9
Even\:
Odd\: -1, -3, -5, -7, -9
[/output]
[/test]
[test]
[input]
1, 53, 321, 53, 32, 55, 12, 0, -12, -4, -53, -3, 21, -44
[/input]
[output]
Positive\: 1, 53, 321, 53, 32, 55, 12, 0, 21
Negative\: -12, -4, -53, -3, -44
Even\: 32, 12, 0, -12, -4, -44
Odd\: 1, 53, 321, 53, 55, -53, -3, 21
[/output]
[/test]
[/tests]
[/code-task]
[/slide]