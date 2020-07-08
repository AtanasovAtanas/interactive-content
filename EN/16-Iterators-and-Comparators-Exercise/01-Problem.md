[slide hideTitle]
# Problem: Listy Iterator
[code-task title="Listy Iterator" taskId="9a6d5aae-9c95-4829-a067-f76b9213d27a" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create a `class ListyIterator`.

It should receive the collection of **Strings** which it will iterate, through its constructor.

You should store the elements in a **List**.

The class should have three main functions:

- `Move` - should move an internal **index** position to the next index in the list, the method should return **true** if it successfully moved and **false** if there is no next index.

- `HasNext` - should return **true** if there is a next index and **false** if the index is already at the **last** element of the list.
- `Print` - should **print** the element at the current internal index, calling Print on a collection without elements should **throw** an appropriate **exception** with the message "**Invalid Operation!**".

By default, the internal index should be pointing to **the zero index** of the List. Your program should support the following commands:

| **Command** | **Return Type** | **Description** |
| --- | --- | --- |
| Create {e1 e2 …} | void | Creates a ListyIterator from the specified collection. In case of a Create command without any elements, you should create a ListyIterator with an empty collection. |
| Move | boolean | This command should move the internal index to the next index. |
| Print | void | This command should print the element at the current internal index. |
| HasNext | boolean | Returns whether the collection has the next element. |
| END | void | Stops the input. |

## Input

Input will come from the console as **lines** of commands. The first line will **always** be **Create** command in the input. The last command received will **always** be **END** command.

## Output

For every command from the input (with the exception of the **END** and **Create** commands) print the result of that command on the console, each on a **new line**. In case of **Move** or **HasNext** commands print the **returned value** of the method, in case of a **Print** command you don't have to do anything additional as the method itself should already print on the console. Your program should catch **any exceptions thrown** because of validations (calling Print on an empty collection) and print their messages instead.

## Constraints

- There will always be only **one Create** command and it will always be the first command passed.
- The number of commands received will be **between** [1 ... 100].
- The last command will always be the `END` command.


## Examples
| **Input** | **Output** |
| --- | --- |
| Create | Invalid Operation! |
| Print | false |
| Move | false |
| HasNext |  |
| END |  |

| **Input** | **Output** |
| --- | --- |
| Create Stan Johnson | true |
| HasNext | Stan |
| Print | true |
| Move | Johnson |
| Print |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Create
Print
Move
HasNext
END
[/input]
[output]
Invalid Operation!
false
false
[/output]
[/test]
[test open]
[input]
Create Stan Johnson
HasNext
Print
Move
Print
END
[/input]
[output]
true
Stan
true
Johnson
[/output]
[/test]
[test]
[input]
Create
Print
END
[/input]
[output]
Invalid Operation!
[/output]
[/test]
[test]
[input]
Create Steven Grand
HasNext
Print
Move
Print
END
[/input]
[output]
true
Steven
true
Grand
[/output]
[/test]
[test]
[input]
Create 1 2 3
HasNext
Move
HasNext
HasNext
Move
HasNext
END
[/input]
[output]
true
true
true
true
true
false
[/output]
[/test]
[test]
[input]
Create Steven Grand
HasNext
Print
Move
Print
Move
Print
Move
Print
END
[/input]
[output]
true
Steven
true
Grand
false
Grand
false
Grand
[/output]
[/test]
[test]
[input]
Create Steven Grand
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
HasNext
Print
END
[/input]
[output]
true
true
true
true
true
true
true
true
true
true
true
true
true
true
true
true
true
true
Steven
[/output]
[/test]
[test]
[input]
Create Steven Grand
END
[/input]
[output]

[/output]
[/test]
[/tests]
[/code-task]
[/slide]