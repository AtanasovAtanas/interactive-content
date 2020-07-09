[slide hideTitle]
# Problem: Equality Logic
[code-task title="Equality Logic" taskId="153a6dbe-9071-4032-838c-08fe0abc284c" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Create a **class** `Person` holding **name** and **age**.

A person with the **same** name and age should be considered the same, override any methods needed to enforce this logic.

Your class should work with **both** standard and hashed collections.

Create a `TreeSet` and a `HashSet` of type Person.

## Input

On the first line, you will receive a number **N**. 

On each of the next **N** lines, you will receive information about people in the format `{name} {age}`. 

Add the people from the input into **both** sets (both sets should hold all the people passed in from the input).

## Output

The output should consist of **exactly** 2 lines. 

On the first, you should print the **size** of the `TreeSet` and on the second - the **size** of the `HashSet`.

## Constraints

- A person's name will be a string that contains **only** alphanumerical characters with a length **between** [1 ... 50] symbols.
- A person's age will be a **positive** integer **between** [1 ... 100].
- The number of people **N** will be a positive integer **between** [0 ... 100].

## Hint

You should override **both** the equals and **hashCode** methods. 

You can check online for implementation of hashCode - it doesn't have to be perfect, but it should be good enough to produce the same hash code for objects with the **same** name and age, and different enough hash codes for objects with **different** name and/or age.


## Examples
| **Input** | **Output** |
| --- | --- |
| 3 | John 100 |
| Peter 20 | Peter 20 |
| John 100 | Penelope 1 |
| Penelope 1 | Penelope 1 |
|  | Peter 20 |
|  | John 100 |

| **Input** | **Output** |
| --- | --- |
| 5 | aria 33 |
| Ivan 17 | Ivan 17 |
| aria 33 | John 3 |
| Steven 25 | Nicko 99 |
| Nicko 99 | Steven 25 |
| John 3 | John 3 |
|  | Ivan 17 |
|  | Steven 25 |
|  | aria 33 |
|  | Nicko 99 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
4
Peter 20
Pete 20
John 15
Peter 21
[/input]
[output]
4
4
[/output]
[/test]
[test open]
[input]
7
Ivan 17
ivan 17
Stan 25
Ivan 18
Ivan 17
Stann 25
Stan 25
[/input]
[output]
5
5
[/output]
[/test]
[test]
[input]
4
Peter 30
Pete 30
John 25
Peter 31
[/input]
[output]
4
4
[/output]
[/test]
[test]
[input]
7
Ivan 27
ivan 27
Stan 35
Ivan 28
Ivan 27
Stann 35
Stan 35
[/input]
[output]
5
5
[/output]
[/test]
[test]
[input]
14
Ivan 17
ivan 17
Stan 25
Ivan 18
Ivan 17
Stann 25
Stan 25
Ivan 17
ivan 17
Stan 25
Ivan 18
Ivan 17
Stann 25
Stan 25
[/input]
[output]
5
5
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
0
0
[/output]
[/test]
[test]
[input]
2
P 100
Y 1
[/input]
[output]
2
2
[/output]
[/test]
[test]
[input]
2
I 3
I 3
[/input]
[output]
1
1
[/output]
[/test]
[/tests]
[/code-task]
[/slide]