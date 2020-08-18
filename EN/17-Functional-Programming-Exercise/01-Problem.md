[slide hideTitle]
# Problem: Consumer Print
[code-task title="Consumer Print" taskId="0080f16e-7468-4ba7-8b44-4fa30787a3df" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that **reads** a collection of **strings**, separated by one or **more** whitespaces, from the console, and then prints them onto the console.

Each string should be printed on a new line.

Use a `Consumer<T>`.

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter George Adam | Peter |
|  | George |
|  | Adam |


| **Input** | **Output** |
| --- | --- |
| Nelson Grand Hubert | Nelson |
|  | Grand |
|  | Hubert |


| **Input** | **Output** |
| --- | --- |
| Alan Nick Connor | Alan |
|  | Nick |
|  | Connor |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter George Adam
[/input]
[output]
Peter
George
Adam
[/output]
[/test]
[test open]
[input]
Nelson Grand Hubert
[/input]
[output]
Nelson
Grand
Hubert
[/output]
[/test]
[test open]
[input]
Alan Nick Connor
[/input]
[output]
Alan
Nick
Connor
[/output]
[/test]
[test]
[input]
Print Me Please Now
[/input]
[output]
Print
Me
Please
Now
[/output]
[/test]
[test]
[input]
Hello World
[/input]
[output]
Hello
World
[/output]
[/test]
[test]
[input]
Its A Really Big Big World
[/input]
[output]
Its
A
Really
Big
Big
World
[/output]
[/test]
[test]
[input]
All Your Base Are Belong To Us
[/input]
[output]
All
Your
Base
Are
Belong 
To
Us
[/output]
[/test]
[test]
[input]
Dolche Far Niente
[/input]
[output]
Dolche
Far
Niente
[/output]
[/test]
[/tests]
[/code-task]
[/slide]