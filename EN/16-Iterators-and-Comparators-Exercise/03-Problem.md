[slide hideTitle]
# Problem: Stack Iterator
[code-task title="Stack Iterator" taskId="881b70cc-b1ca-4ae0-8cc1-1fc25c85cef5" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You have a task to create your custom Stack.

You already know the Stack structure.

The elements are stored in a collection.

It has two functions (not from the functional programming) - to `push` and `pop` an element.

The first **popped** element is on the **last position** in the collection.

The `push` method adds an element to the **top** of the collection and the `pop` method returns the **top** element and **removes** it.

Write your custom implementation of `Stack<Integer>` and implement your custom **iterator**. 

Your Stack class should implement the `Iterable<Integer>` interface and your **Iterator Class** should implement `Iterator<Integer>` interface. 

Your Custom Iterator should follow the rules of the **Abstract Data Type - Stack**. 

The first element is the element at the top, and so on. 

Iterators are used only for iterating through the collection, they **should not** remove or mutate the elements.

## Input
The input can be only two types `Push` and `Pop`, followed by integers for the `Push` command and **no other** input for the `Pop` command. 

Each command will come on a separate line.

Format:
- `Push {element, secondElement…}`
- `Pop`

## Output
The program should stop when you receive the command `END`. 

Foreach the stack **twice** and print all elements. Each element should be on a **new line**.

## Constraints
- The elements in the `Push` command will be **valid** integers **between** [2 ^ -32 ... 2 ^ 32 - 1].
- The commands will always be **valid** (always be either `Push`, `Pop`, or `END`).
- There will be no more than **16**** elements in the `Push` command.
- If `Pop` command **could not** be executed as expected (e.g. no elements in the stack), print on the console: `No elements`.

## Examples
| **Input** | **Output** |
| --- | --- |
| Push 1, 2, 3, 4 | 2 |
| Pop | 1 |
| Pop | 2 |
| END | 1 |

| **Input** | **Output** |
| --- | --- |
| Push 1, 2, 3, 4  | 1 |
| Pop | 3 |
| Push 1 | 2 |
| END | 1 |
|  | 1 |
|  | 3 |
|  | 2 |
|  | 1 |

| **Input** | **Output** |
| --- | --- |
| Push 1, 2, 3, 4  | No elements |
| Pop |  |
| Pop |  |
| Pop |  |
| Pop |  |
| Pop |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Push 1, 2, 3, 4
Pop
Pop
END
[/input]
[output]
2
1
2
1
[/output]
[/test]
[test open]
[input]
Push 1, 2, 3, 4 
Pop
Push 1
END
[/input]
[output]
1
3
2
1
1
3
2
1
[/output]
[/test]
[test open]
[input]
Push 1, 2, 3, 4 
Pop
Pop
Pop
Pop
Pop
END
[/input]
[output]
No elements
[/output]
[/test]
[test]
[input]
Push 1, 2, 3, 4, 5
Pop
Pop
Pop
END
[/input]
[output]
2
1
2
1
[/output]
[/test]
[test]
[input]
Push 1, 2, 3, 4, 5 
Pop
Pop
Push 1
END
[/input]
[output]
1
3
2
1
1
3
2
1
[/output]
[/test]
[test]
[input]
Push 1, 2, 3, 4, 5 
Pop
Pop
Pop
Pop
END
[/input]
[output]
1
1
[/output]
[/test]
[test]
[input]
Push 1, 2, 3, 4 
Pop
Pop
Pop
Pop
END
[/input]
[output]

[/output]
[/test]
[test]
[input]
Push 1, 2, 3, 4, 5 
Pop
Pop
Pop
Pop
Pop
Pop
END
[/input]
[output]
No elements
[/output]
[/test]
[/tests]
[/code-task]
[/slide]