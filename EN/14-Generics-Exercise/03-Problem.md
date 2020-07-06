[slide hideTitle]
# Problem: Generic Swap Method String
[code-task title="Generic Swap Method String" taskId="115c52f8-04df-47de-941f-a836b608aec7" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create a generic method that receives a list containing **any type of data** and swaps the elements at two given indexes.

As in the previous problems, read **n** number of boxes of type **String** and add them to the list. 

On the next line you will receive a swap command consisting of **two indexes**. 

Use the method you've created to swap the elements that correspond to the given indexes and **print each** element in the list.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | java.lang.String: Swap me with John |
| John | java.lang.String: George |
| George | java.lang.String: John |
| Swap me with John |  |
| 0 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
John
George
Swap me with John
0 2
[/input]
[output]
java.lang.String: Swap me with John
java.lang.String: George
java.lang.String: John
[/output]
[/test]
[test]
[input]
3
1
2
3
0 0
[/input]
[output]
java.lang.String: 1
java.lang.String: 2
java.lang.String: 3
[/output]
[/test]
[test]
[input]
5
12
13
14
15
16
0 3
[/input]
[output]
java.lang.String: 15
java.lang.String: 13
java.lang.String: 14
java.lang.String: 12
java.lang.String: 16
[/output]
[/test]
[test]
[input]
1
-2147483648
0 0
[/input]
[output]
java.lang.String: -2147483648
[/output]
[/test]
[test]
[input]
2
pulien
haos
0 1
[/input]
[output]
java.lang.String: haos
java.lang.String: pulien
[/output]
[/test]
[test]
[input]
5
abc
d
e
f
ghi
0 1
[/input]
[output]
java.lang.String: d
java.lang.String: abc
java.lang.String: e
java.lang.String: f
java.lang.String: ghi
[/output]
[/test]
[/tests]
[/code-task]
[/slide]