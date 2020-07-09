[slide hideTitle]
# Problem: Strategy Pattern
[code-task title="Strategy Pattern" taskId="34db6cd1-ca97-4cdd-b4d1-72e88985f539" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
An interesting pattern you may have heard of is the Strategy Pattern.

If we have multiple ways to do a task (let's say sort a collection) it allows the client to choose the way that most fits his needs.

A famous implementation of the pattern in Java is the `Collections.sort()` method that takes a **Comparator**.

Create a class `Person` that holds **name** and **age**. 

Create 2 Comparators for Person (classes which implement the `Comparator<Person>` **interface**). 

The first comparator should compare people based on the **length of their name** as a first parameter if two persons have a name with the **same** length, perform a **case-insensitive** compare based on the **first letter of their name** instead. 

The second comparator should compare them based on their **age**. Create 2 **TreeSets** of type Person, the first should implement the name comparator, the second should implement the age comparator.

## Input
On the first line, you will receive a number **N**. 

On each of the next **N** lines, you will receive information about people in the format `{name} {age}`. 

Add the people from the input into **both** sets.

## Output
**Foreach** the sets and print each person from the set on a **new line** in the same format that you received them. 

Start with the set that implements the name comparator.

## Constraints
- A person's name will be a string that contains **only** alphanumerical characters with a length **between** [1 ... 50] symbols.
- A person's age will be a **positive** integer **between** [1 ... 100].
- The number of people **N** will be a **positive** integer **between** [0 ... 100].

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
3
Peter 20
John 100
Penelope 1
[/input]
[output]
John 100
Peter 20
Penelope 1
Penelope 1
Peter 20
John 100
[/output]
[/test]
[test open]
[input]
5
Ivan 17
aria 33
Steven 25
Nicko 99
John 3
[/input]
[output]
aria 33
Ivan 17
John 3
Nicko 99
Steven 25
John 3
Ivan 17
Steven 25
aria 33
Nicko 99
[/output]
[/test]
[test]
[input]
3
Peter 33
John 11
Penelope 2
[/input]
[output]
John 11
Peter 33
Penelope 2
Penelope 2
John 11
Peter 33
[/output]
[/test]
[test]
[input]
5
Ivan 27
aria 43
Steven 35
Nicko 99
John 13
[/input]
[output]
aria 43
Ivan 27
John 13
Nicko 99
Steven 35
John 13
Ivan 27
Steven 35
aria 43
Nicko 99
[/output]
[/test]
[test]
[input]
0
[/input]
[output]

[/output]
[/test]
[test]
[input]
2
Ivan 17
aria 33
[/input]
[output]
aria 33
Ivan 17
Ivan 17
aria 33
[/output]
[/test]
[test]
[input]
5
Ivan 17
aria 33
aaRia 20
aaRias 20
Vans1 13
[/input]
[output]
aria 33
Ivan 17
aaRia 20
Vans1 13
aaRias 20
Vans1 13
Ivan 17
aaRia 20
aria 33
[/output]
[/test]
[/tests]
[/code-task]
[/slide]