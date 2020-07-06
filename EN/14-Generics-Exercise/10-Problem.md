[slide hideTitle]
# Problem: Tuple
[code-task title="Tuple" taskId="970fddee-cf23-4c2c-a160-e2ca9de024bb" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
There is a sequence of elements, called **"Tuple"**.

It is a class, which contains two objects: the first one is **"item1"**; the second one is **"item2"**.

It is similar to **Map.Entry** but it **only has items**, which are **neither key nor value**.

It is unknown what these objects are holding.

The class name does not give enough information, the methods which it has – too.

Your task is to try to implement it in Java, just for practicing generics.

Create a class **"Tuple"**, which is holding two objects. 

The first one will be **"item1"** and the second one - **"item2"**. 

The class has to hold **Generics**. 

When you create a new object of class -  **"Tuple"**, you should specify the item types separately.

### Input

The input consists of three lines:

- The first one is holding a **person's name** and **city of residence**. Both are **separated by space(s)**. You have to collect them in the Tuple and print them on the console. This input comes in the following format:

`{first name} {last name} {address}`

- The second line holds a **name** of a person and the **amount of hobbies** he has and comes in the following format:

`{name} {hobbies}`

- The last line will hold an **Integer** and a **Double** in the following format:

`{Integer} {Double}`

### Output

- Print the tuple items in format: 

`{item1} -> {item2}`

### Constraints

Use the good practices we have learned. 

Create the class and make it have getters and setters for its class variables. 

The input will be valid, there is no need to check it explicitly!

## Examples
| **Input** | **Output** |
| --- | --- |
| Sofia Tucker London | Sofia Tucker -> London |
| john 2 | john -> 2 |
| 23 21.23212321 | 23 -> 21.23212321 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Sofia Tucker London
John 2
23 21.23212321
[/input]
[output]
Sofia Tucker -\> London
John -\> 2
23 -\> 21.23212321
[/output]
[/test]
[test]
[input]
Sean Paul NY
Adam 6
29 21.121212
[/input]
[output]
Sean Paul -\> NY
Adam -\> 6
29 -\> 21.121212
[/output]
[/test]
[test]
[input]
Steven Adams Madrid
Peter 9
21 21
[/input]
[output]
Steven Adams -\> Madrid
Peter -\> 9
21 -\> 21.0
[/output]
[/test]
[test]
[input]
Garet = Geneva
 2999999
21 21
[/input]
[output]
Garet = -\> Geneva
 -\> 2999999
21 -\> 21.0
[/output]
[/test]
[test]
[input]
Charls King Westcastle
Shamsky 2999999
21 21.212
[/input]
[output]
Charls King -\> Westcastle
Shamsky -\> 2999999
21 -\> 21.212
[/output]
[/test]
[/tests]
[/code-task]
[/slide]