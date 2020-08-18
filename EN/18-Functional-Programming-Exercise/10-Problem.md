[slide hideTitle]
# Problem: Predicate Party!
[code-task title="Predicate Party!" taskId="dddde019-7c68-4e50-a225-d788254e9e69" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You want to make a party at home this weekend.

You have to create a program to track your reservations.

On the first line, you get a **list** with all the **people** that are coming. On the next lines, until you get the `Party!` command, you may be asked to `Double` or `Remove` all the people that apply to **given criteria**. 

There are three different options:

- `StartsWith` - everyone that has a name **starting** with a given string;
- `EndsWith` - everyone that has a name **ending** with a given string;
- `Length` - everyone that has a name with a given **length**.

When you print the guests that are coming to the party, you have to print them in **ascending** order. 

If nobody is going, print `Nobody is going to the party!"`. 

For more information see the examples below:

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter Michael Steven | Michael, Michael, Steven are going to the party! |
| Remove StartsWith P |  |
| Double Length 7 |  |
| Party! |  |

| **Input** | **Output** |
| --- | --- |
| Pete | Pete, Pete, Pete, Pete are going to the party! |
| Double StartsWith Pe |  |
| Double EndsWith te |  |
| Party! |  |

| **Input** | **Output** |
| --- | --- |
| John | Nobody is going to the party! |
| Remove StartsWith J |  |
| Party! |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter Michael Steven
Remove StartsWith P
Double Length 7
Party!
[/input]
[output]
Michael, Michael, Steven are going to the party!
[/output]
[/test]
[test open]
[input]
Pete
Double StartsWith Pe
Double EndsWith te
Party!
[/input]
[output]
Pete, Pete, Pete, Pete are going to the party!
[/output]
[/test]
[test open]
[input]
John
Remove StartsWith J
Party!
[/input]
[output]
Nobody is going to the party!
[/output]
[/test]
[test]
[input]
P M S G H M p s l
Remove StartsWith P
Double StartsWith p
Remove Length 4
Party!
[/input]
[output]
G, H, M, M, S, l, p, p, s are going to the party!
[/output]
[/test]
[test]
[input]
G
Party!
[/input]
[output]
G are going to the party!
[/output]
[/test]
[test]
[input]
P
Double StartsWith P
Double Length 1
Double EndsWith P
Party!
[/input]
[output]
P, P, P, P, P, P, P, P are going to the party!
[/output]
[/test]
[test]
[input]
S
Double StartsWith P
Double Length 5
Double EndsWith o
Remove Length 5
Double StartsWith Pe
Double StartsWith S
Party!
[/input]
[output]
S, S are going to the party!
[/output]
[/test]
[test]
[input]
P
Double StartsWith P
Double Length 1
Double EndsWith P
Remove Length 1
Double StartsWith P
Party!
[/input]
[output]
Nobody is going to the party!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]