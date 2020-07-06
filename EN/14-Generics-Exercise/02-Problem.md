[slide hideTitle]
# Problem: Generic Box of Integer
[code-task title="Generic Box of Integer" taskId="02b21d7e-498e-4ff1-ae18-27793c1e0f19" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create a **generic class Box** that can store any type.

**Override** the `toString()` method to print the type and the value of the stored data in the format 

`{class full name}: {value}`

Use the class that you have created and test it with the class `java.lang.Integer`. 

On the first line you will get the number **n** - the number of Integers to read from the console. 

On the next **n** lines, you will get the actual Integers. 

For each of them create a box and call its `toString()` method to print its data on the console.

## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | java.lang.Integer: 7 |
| 7 | java.lang.Integer: 123 |
| 123 | java.lang.Integer: 42 |
| 42 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
7
123
42
[/input]
[output]
java.lang.Integer: 7
java.lang.Integer: 123
java.lang.Integer: 42
[/output]
[/test]
[test]
[input]
3
1
2
3
[/input]
[output]
java.lang.Integer: 1
java.lang.Integer: 2
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
[/input]
[output]
java.lang.Integer: 12
java.lang.Integer: 13
java.lang.Integer: 14
java.lang.Integer: 15
java.lang.Integer: 16
[/output]
[/test]
[test]
[input]
1
-2147483648
[/input]
[output]
java.lang.Integer: -2147483648
[/output]
[/test]
[test]
[input]
1
0
[/input]
[output]
java.lang.Integer: 0
[/output]
[/test]
[test]
[input]
1
2147483647
[/input]
[output]
java.lang.Integer: 2147483647
[/output]
[/test]
[/tests]
[/code-task]
[/slide]