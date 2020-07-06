[slide hideTitle]
# Problem: Generic Swap Method Integer
[code-task title="Generic Swap Method Integer" taskId="6d827176-4208-48ad-aa4f-f2e1181e4a11" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

As in the previous problems, read **n** number of boxes of type **Integer** and add them to the list. 

On the next line you will receive a swap command consisting of **two indexes**. 

Use the method you've created to swap the elements that correspond to the given indexes and **print each** element in the list.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | java.lang.Integer: 42 |
| 7 | java.lang.Integer: 123 |
| 123 | java.lang.Integer: 7 |
| 42 |  |
| 0 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
7
123
42
0 2
[/input]
[output]
java.lang.Integer: 42
java.lang.Integer: 123
java.lang.Integer: 7
[/output]
[/test]
[test]
[input]
3
1
2
3
0 1
[/input]
[output]
java.lang.Integer: 2
java.lang.Integer: 1
java.lang.Integer: 3
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
3 4
[/input]
[output]
java.lang.Integer: 12
java.lang.Integer: 13
java.lang.Integer: 14
java.lang.Integer: 16
java.lang.Integer: 15
[/output]
[/test]
[test]
[input]
1
-2147483648
0 0
[/input]
[output]
java.lang.Integer: -2147483648
[/output]
[/test]
[test]
[input]
1
0
0 0
[/input]
[output]
java.lang.Integer: 0
[/output]
[/test]
[test]
[input]
1
2147483647
0 0
[/input]
[output]
java.lang.Integer: 2147483647
[/output]
[/test]
[/tests]
[/code-task]
[/slide]