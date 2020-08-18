[slide hideTitle]
# Problem: Knights of Honor
[code-task title="Knights of Honor" taskId="6e9ffed1-43e4-44b3-88d5-40bda1ac9c60" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that **reads a collection of names** as strings from the console and then **appends "Sir"** in front of every name and prints it back onto the console.

Use a `Consumer<T>`.

## Examples
| **Input** | **Output** |
| --- | --- |
| Henry Alex Anthony Stanley | Sir Henry |
|  | Sir Alex |
|  | Sir Anthony |
|  | Sir Stanley |

| **Input** | **Output** |
| --- | --- |
| Derryl Isaac David | Sir Derryl |
|  | Sir Isaac |
|  | Sir David |

| **Input** | **Output** |
| --- | --- |
| Patrick Christopher | Sir Patrick |
|  | Sir Christopher |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Henry Alex Anthony Stanley
[/input]
[output]
Sir Henry
Sir Alex
Sir Anthony
Sir Stanley
[/output]
[/test]
[test open]
[input]
Derryl Isaac David
[/input]
[output]
Sir Derryl
Sir Isaac
Sir David
[/output]
[/test]
[test open]
[input]
Patrick Christopher
[/input]
[output]
Sir Patrick
Sir Christopher
[/output]
[/test]
[test]
[input]
Print Me Please Now
[/input]
[output]
Sir Print
Sir Me
Sir Please
Sir Now
[/output]
[/test]
[test]
[input]
Hello World
[/input]
[output]
Sir Hello
Sir World
[/output]
[/test]
[test]
[input]
Its A Really Big Big World
[/input]
[output]
Sir Its
Sir A
Sir Really
Sir Big
Sir Big
Sir World
[/output]
[/test]
[test]
[input]
All Your Base Belong To Us
[/input]
[output]
Sir All
Sir Your
Sir Base
Sir Belong
Sir To
Sir Us
[/output]
[/test]
[test]
[input]
Dolche Far Niente
[/input]
[output]
Sir Dolche
Sir Far
Sir Niente
[/output]
[/test]
[/tests]
[/code-task]
[/slide]