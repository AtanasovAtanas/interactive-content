[slide hideTitle]
# Problem: Collection
[code-task title="Collection" taskId="d1be3bcc-1298-496e-8add-f13ce702bfe8" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Using the `ListyIterator` from the last problem, extend it by implementing the `Iterable` interface.

Implement **all** methods desired by the interface manually.

Add a new method to the class `PrintAll()`, the method should use `foreach` on the collection and print all elements on a **single line** separated by a space.

## Input
Input will come from the console as **lines** of commands. The first line will always be the `Create` command. 

The **last** command received will always be the `END` command.

## Output
For every command from the input (with the exception of the `END` and `Create` commands) print the result of that command on the console, each on a **new line**. 

In the case of `Move` or `HasNext` commands print the returned value of the method, in case of a `Print` command you don't have to do anything additional as the method itself should already print on the console. 

In the case of a `PrintAll` command, you should print all elements on a single line **separated by spaces**. Your program should catch **any exceptions** thrown because of validations and print their messages instead.

## Constraints
- **Do not use the built-in iterators!**
- There will always be only **one** `Create` **command** and it will **always** be the first command passed.
- The number of commands received will be **between** [1 ... 100].
- The **last** command will always be the `END` command.

## Examples
| **Input** | **Output** |
| --- | --- |
| Create 1 2 3 4 5 | true |
| Move | 1 2 3 4 5 |
| PrintAll |  |
| END |  |

| **Input** | **Output** |
| --- | --- |
| Create Steven John Kevin | Steven John Kevin  |
| PrintAll | true |
| Move | true |
| Move | Kevin |
| Print | false |
| HasNext |  |
| END |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Create 1 2 3 4 5
Move
PrintAll
END
[/input]
[output]
true
1 2 3 4 5
[/output]
[/test]
[test open]
[input]
Create Steven John Kevin
PrintAll
Move
Move
Print
HasNext
END
[/input]
[output]
Steven John Kevin 
true
true
Kevin
false
[/output]
[/test]
[test]
[input]
Create Steven John Kevin
PrintAll
Move
Move
Print
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
HasNext
END
[/input]
[output]
Steven John Kevin 
true
true
Kevin
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
false
[/output]
[/test]
[test]
[input]
Create Steven John Kevin
PrintAll
Move
Move
Print
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
PrintAll
HasNext
HasNext
asd
asd
asd
asd
asd
PrintAll
END
[/input]
[output]
Steven John Kevin 
true
true
Kevin
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
Steven John Kevin 
false
false
Steven John Kevin
[/output]
[/test]
[test]
[input]
Create Steven John Kevin
PrintAll
Move
END
[/input]
[output]
Steven John Kevin 
true
[/output]
[/test]
[test]
[input]
Create Steven John Kevin
PrintAll
Move
Move
Move
Move
Move
Move
Move
Move
Move
Move
Move
PrintAll
END
[/input]
[output]
Steven John Kevin 
true
true
false
false
false
false
false
false
false
false
false
Steven John Kevin
[/output]
[/test]
[/tests]
[/code-task]
[/slide]