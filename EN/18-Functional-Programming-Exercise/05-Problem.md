[slide hideTitle]
# Problem: Predicate For Names
[code-task title="Predicate For Names" taskId="36a2cb92-7cdb-4203-9be0-2b693ca73b04" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a **predicate**.

It has to **check** a name for its length and return **true** if the length of the names is **less or equal** the passed **integer**.

You will receive an **integer** that represents the length you have to use.

On the second line, you will receive a **string** array with some names.

Print the names, passing the **condition** in the predicate.

## Examples
| **Input** | **Output** |
| --- | --- |
| 4 | Adam |
| Kenneth Adam Kevin Yasmin |  |

| **Input** | **Output** |
| --- | --- |
| 4 | Gaby |
| Yasmine Quinn Gaby Mat Ivan | Mat |
|  | Ivan |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
4
Kenneth Adam Kevin Yasmin
[/input]
[output]
Adam
[/output]
[/test]
[test open]
[input]
4
Yasmine Quinn Gaby Mat Ivan
[/input]
[output]
Gaby
Mat
Ivan
[/output]
[/test]
[test]
[input]
4
Qqqq Kkkk Iii Kkkkkk
[/input]
[output]
Qqqq
Kkkk
Iii
[/output]
[/test]
[test]
[input]
3
Iii Aaa Bbbb
[/input]
[output]
Iii
Aaa
[/output]
[/test]
[test]
[input]
0
Aaaa Sssssssssss
[/input]
[output]

[/output]
[/test]
[test]
[input]
-1
Koko
[/input]
[output]

[/output]
[/test]
[/tests]
[/code-task]
[/slide]