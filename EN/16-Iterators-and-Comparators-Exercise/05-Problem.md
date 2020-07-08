[slide hideTitle]
# Problem: Comparing Objects
[code-task title="Comparing Objects" taskId="ca960ad8-04a2-484b-a743-8d395d7c8ebb" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
There is a Comparable interface but probably you already know.

Your task is simple.

Create a **Class Person**.

Each person should have **name**, **age ** and **town**.

You should implement the interface - `Comparable` and try to override the `compareTo` method.

When you compare two people, first you should compare their **names**, after that - their **age** and last but not at least - compare their **town**.


## Input
On single lines, you will be given people in format:

`{name} {age} {town}`

Collect them till you receive `END`

After that, you will receive an integer **N** - the **Nth** person in your collection.

## Output
On the single output line, you should bring statistics, how many people are **equal** to him, how many people are **not** equal to him, and the **total** people in your collection.

Format:

`{number of equal people} {number of not equal people} {total number of people}`

## Constraints
- Names, ages and addresses will be **valid.**
- Input number will be always а **valid** integer in **range** [2 ... 100]
- If there are no equal people print: `No matches`

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter 22 Venice | No matches |
| George 14 San Francisco |  |
| END |  |
| 2 |  |

| **Input** | **Output** |
| --- | --- |
| John 22 Miami | 2 1 3 |
| Adam 22 Miami |  |
| Adam 22 Miami |  |
| END |  |
| 2 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter 22 Venice
George 14 San Francisco
END
2
[/input]
[output]
No matches
[/output]
[/test]
[test open]
[input]
John 22 Miami
Adam 22 Miami
Adam 22 Miami
END
2
[/input]
[output]
2 1 3
[/output]
[/test]
[test]
[input]
John 22 Venice
George 14 San Francisco
END
2
[/input]
[output]
No matches
[/output]
[/test]
[test]
[input]
Peter 22 Miami
Adam 22 Miami
Adam 22 Miami
END
2
[/input]
[output]
2 1 3
[/output]
[/test]
[test]
[input]
P 22 V
G 22 V
G 22 V
P 22 V
P 22 V
G 22 V
G 22 V
P 22 V
P 22 V
G 22 V
G 22 V
P 22 V
P 22 V
G 22 V
G 22 V
P 22 V
END
2
[/input]
[output]
8 8 16
[/output]
[/test]
[test]
[input]
P 22 V
END
1
[/input]
[output]
No matches
[/output]
[/test]
[/tests]
[/code-task]
[/slide]