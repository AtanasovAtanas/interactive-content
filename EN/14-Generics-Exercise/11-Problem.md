[slide hideTitle]
# Problem: Threeuple
[code-task title="Threeuple" taskId="b1e957b9-7d47-45a6-914a-5c81cb5f5915" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
The next task is to create another Tuple.

Create a Class **Threeuple**. Its name shows, that the **Threeuple** should **hold three objects**.  It should also have getters and setters. You can extend the previous class - Tuple.

## Input
The input consists of three lines:

- The first one is holding a person's name and city and country of residence in the following format:

`{{first name} {last name}} {city} {country}`

- The second line is holding a name, amount of hobbies, and a **Boolean variable** - happy or not, in the following format:

`{name} {hobbies} {happy or not}`

- The last line will hold a name, a bank balance (double) and a bank name. Format:

`{name} {account balance} {bank name}`

## Output

- Print the Threeuples objects in the following format: 

`{firstElement} -> {secondElement} -> {thirdElement}`


## Examples
| **Input** | **Output** |
| --- | --- |
| Sofia Tucker London UK | Sofia Tucker -> London -> UK |
| John 2 happy | John -> 2 -> false |
| Peter 0.10 Expressbank | Peter -> 0.1 -> Expressbank |

| **Input** | **Output** |
| --- | --- |
| Kevin Johnson Sofia Bulgaria | Kevin Johnson -> Sofia -> Bulgaria |
| Mat 18 not | Mat -> 18 -> false |
| Adam 0.10 NGB | Adam -> 0.1 -> NGB |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Sofia Tucker London UK
John 2 happy
Peter 0.10 Expressbank
[/input]
[output]
Sofka Tripova -\> Izgrev -\> Burgas
MitkoShtaigata -\> 18 -\> true
SashoKompota -\> 0.1 -\> NkqfaBanka
[/output]
[/test]
[test open]
[input]
Kevin Johnson Sofia Bulgaria
Mat 18 not
Adam 0.10 NGB
[/input]
[output]
Kevin Johnson -\> Sofia -\> Bulgaria
Mat -\> 18 -\> false
Adam -\> 0.1 -\> NGB
[/output]
[/test]
[test]
[input]
John Johnson Muiami USA
John 3 happy
John 11.11 AmericanExpress
[/input]
[output]
John Johnson -\> Muiami -\> USA
John -\> 3 -\> true
John -\> 11.11 -\> AmericanExpress
[/output]
[/test]
[test]
[input]
K K Varna Bulgaria
K 18 not
K 0.00 DSK
[/input]
[output]
K K -\> Varna -\> Bulgaria
K -\> 18 -\> false
K -\> 0.0 -\> DSK
[/output]
[/test]
[test]
[input]
Aaa Aaa B B
AA 3333 veryHappy
AA 10.01 aaa
[/input]
[output]
Aaa Aaa -\> B -\> B
AA -\> 3333 -\> false
AA -\> 10.01 -\> aaa
[/output]
[/test]
[test]
[input]
A B C D
E 18 HAPPY
F 0.10 G
[/input]
[output]
A B -\> C -\> D
E -\> 18 -\> false
F -\> 0.1 -\> G
[/output]
[/test]
[/tests]
[/code-task]
[/slide]