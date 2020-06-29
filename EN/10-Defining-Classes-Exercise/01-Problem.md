[slide]
# Problem: Opinion Poll
[code-task title="Problem: Opinion Poll" taskId="ff6d1ff1-daef-4e93-b24d-14c878e40e96" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create Person class with two fields **String name** and **int age**, write a program that reads from the console **N** lines of personal information, and then prints all people whose **age** is **more than 30** years, **sorted in alphabetical order**.

**Note:** you can use `stream()` to filter the people.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | John - 48 |
| Peter 12 | Steven – 31 |
| Steven 31 |  |
| John 48 |  |

| **Input** | **Output** |
| --- | --- |
| 5 | Robert - 44 |
| Sofia 33 | Sofia - 33 |
| Thomas 88 | Thomas – 88 |
| Camilla 22 |  |
| Robert 44 |  |
| Owen 11 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
Peter 12
Steven 31
John 48
[/input]
[output]
John - 48
Steven - 31
[/output]
[/test]
[test open]
[input]
5
Sofia 33
Thomas 88
Camilla 22
Robert 44
Owen 11
[/input]
[output]
Robert - 44
Sofia - 33
Thomas – 88
[/output]
[/test]
[test]
[input]
11
A 40
B 43
C 54
D 31
E 99
M 32
N 123
O 100
P 321534
S 3213
Z 32131
[/input]
[output]
A - 40
B - 43
C - 54
D - 31
E - 99
M - 32
N - 123
O - 100
P - 321534
S - 3213
Z - 32131
[/output]
[/test]
[test]
[input]
11
Z 32
S 12
P 0
O 100
N 123
M 32
E 99
D 1
C 54
B 43
A 40
[/input]
[output]
A - 40
B - 43
C - 54
E - 99
M - 32
N - 123
O - 100
Z - 32
[/output]
[/test]
[test]
[input]
4
A 10
B 11
C 12
D 13
[/input]
[output]

[/output]
[/test]
[test]
[input]
10
A 31
B 76
E 645
Z 55
K 53
I 43
J 543
P 67
H 76
F 88
[/input]
[output]
A - 31
B - 76
E - 645
F - 88
H - 76
I - 43
J - 543
K - 53
P - 67
Z - 55
[/output]
[/test]
[test]
[input]
10
Andrew 31
Ben 76
Edward 645
Felix 11
Harley 76
Ivy 12
Joanna 0
Kylie 30
Poppy 67
Zoie 55
[/input]
[output]
Andrew - 31
Ben - 76
Edward - 645
Harley - 76
Poppy - 67
Zoie - 55
[/output]
[/test]
[test]
[input]
4
Ann 31
Anntoanette 39
An 33
Annie 31
[/input]
[output]
An - 33
Ann - 31
Annie - 31
Anntoanette - 39
[/output]
[/test]
[/tests]
[/code-task]
[/slide]