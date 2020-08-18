[slide hideTitle]
# Program: Froggy
[code-task title="Froggy" taskId="1d93d93e-0062-46f0-8a20-acf10598a4b6" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Let's play a game.

You have a tiny little **Frog**, and a **Lake** with numbers.

The **Lake** and its numbers, you will get by an input from the console.

Imagine, your **Frog** belongs to the **Lake**.

The **Frog jumps** only when the `END` command is received.

When the **Frog** starts jumping, print on the console **each number** the **Frog** have stepped over.

To calculate the jumps, use the guidelines:

The jumps start from the **zero index**. 

And follows the pattern - first all even indexes in **ascending** order(0 -> 2 -> 4 -> 6 and so on) and then all odd indexes in **ascending** order (1 -> 3 -> 5 -> 7 and so on). 

Consider the **zero** index as **even**.

Long story short: Create a Class `Lake`, it should implement the interface - `Iterable`. 

Inside the `Lake`, create a Class - `Frog` and implement the interface `Iterator`. 

You will receive **only integers**.

## Input
The input will consist of two lines. First-line - the **initial** numbers of the lake, **separated** by comma and a single space. 

The second line command is `END`.

## Output
When you receive `END`, the input is over. 

**Foreach** the collection of numbers, the **Frog** has jumped over, and print **each** element.

The output should be print on a **single** line.

Format:

`{number}, {second number}, {third number} ...`

## Constraints
- **Lake's** numbers will be **valid** integers in the **range** [2 ^ -32 ... 2 ^ 32 - 1]
- The command will always be **valid** - `END`

## Examples
| **Input** | **Output** |
| --- | --- |
| 1, 2, 3, 4, 5, 6, 7, 8 | 1, 3, 5, 7, 2, 4, 6, 8 |
| END |  |

| **Input** | **Output** |
| --- | --- |
| 1, 2, 3 | 1, 3, 2 |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
1, 2, 3, 4, 5, 6, 7, 8
END
[/input]
[output]
1, 3, 5, 7, 2, 4, 6, 8
[/output]
[/test]
[test open]
[input]
1, 2, 3
END
[/input]
[output]
1, 3, 2
[/output]
[/test]
[test]
[input]
1, 2, 3, 4, 5, 6, 7, 8, 1, 2, 3, 4, 5, 6, 7, 8
END
[/input]
[output]
1, 3, 5, 7, 1, 3, 5, 7, 2, 4, 6, 8, 2, 4, 6, 8
[/output]
[/test]
[test]
[input]
1, 2, 3, 4
END
[/input]
[output]
1, 3, 2, 4
[/output]
[/test]
[test]
[input]
1, 2, 3, 4, -3, -0, 0
END
[/input]
[output]
1, 3, -3, 0, 2, 4, 0
[/output]
[/test]
[test]
[input]
0
END
[/input]
[output]
0
[/output]
[/test]
[test]
[input]
10000000, 100000000, 100000000
END
[/input]
[output]
10000000, 100000000, 100000000
[/output]
[/test]
[test]
[input]
3, 3, 3
END
[/input]
[output]
3, 3, 3
[/output]
[/test]
[/tests]
[/code-task]
[/slide]