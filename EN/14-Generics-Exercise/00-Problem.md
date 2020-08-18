[slide hideTitle]
# Problem: Generic Box
[code-task title="Generic Box" taskId="03c888d5-32bb-49b1-8ea0-e43077b1138a" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create a **Generic Class Box** that can store any type.

**Override** the `toString()` method to print the type and the value of the stored data in the format:

`{class full name}: {value}`

Use the class that you have created and test it with the class `java.lang.String`. 

On the first line, you will get the number **n** - the number of Strings to read from the console. 

On the next **n** lines, you will get the actual Strings. 

For each of them create a box and call its `toString()` method to print its data on the console.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | java.lang.String: life in a box |
| life in a box | java.lang.String: box in a life |
| box in a life |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
life in a box
box in a life
[/input]
[output]
java.lang.String: life in a box
java.lang.String: box in a life
[/output]
[/test]
[test]
[input]
3
Pesho
Simo
Gosho
[/input]
[output]
java.lang.String: Pesho
java.lang.String: Simo
java.lang.String: Gosho
[/output]
[/test]
[test]
[input]
5
jega
mi
e
tezi
dni
[/input]
[output]
java.lang.String: jega
java.lang.String: mi
java.lang.String: e
java.lang.String: tezi
java.lang.String: dni
[/output]
[/test]
[test]
[input]
6
kolko
mnogo
muka
ima
po
tozi
[/input]
[output]
java.lang.String: kolko
java.lang.String: mnogo
java.lang.String: muka
java.lang.String: ima
java.lang.String: po
java.lang.String: tozi
[/output]
[/test]
[test]
[input]
1
I am an Integer
[/input]
[output]
java.lang.String: I am an Integer
[/output]
[/test]
[test]
[input]
10
I am an Integer
I am an Integer
I am an Integer
I am an Integer
I am an Integer
I am an Integer
I am an Integer
I am an Integer
I am an Integer
I am an Integer
[/input]
[output]
java.lang.String: I am an Integer
java.lang.String: I am an Integer
java.lang.String: I am an Integer
java.lang.String: I am an Integer
java.lang.String: I am an Integer
java.lang.String: I am an Integer
java.lang.String: I am an Integer
java.lang.String: I am an Integer
java.lang.String: I am an Integer
java.lang.String: I am an Integer
[/output]
[/test]
[/tests]
[/code-task]
[/slide]