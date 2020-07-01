[slide hideTitle]
# Problem: Google
[code-task title="Problem: Google" taskId="5d118095-25ac-454f-b83d-562694f855fa" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
*Google knows everything about you (even your pokemon collection). Since you are good at writing classes, Google asked you to design a Class that can hold all the information they need for people.*

From the console you will receive lines until the command `End`.

Each of those lines contains information about a person in one of the following formats:

- `{personName} company {companyName} {department} {salary}`

- `{personName} pokemon {pokemonName} {pokemonType}`

- `{personName} parents {parentName} {parentBirthday}`

- `{personName} children {childName} {childBirthday}`

- `{personName} car {carModel} {carSpeed}`

You should structure all information about a person in a class with nested subclasses. 

Person names are **unique** - there won't be 2 person with the same name.

A person can have **only one company** and **one car**, but can have **multiple parents, children** and **pokemon**. 

After the command `End` you will receive a **single** name on the next line.

You should **print** all information about that person. 

**Note** that the information can change **during** the **input**.

For example, if you receive multiple lines which specify a person company, only the **last one** should be the one remembered. 

The salary must be formatted to **the second decimal place**.

Print the information in the following format:

```java
{personName}
Company:
{companyName} {companyDepartment} {salary}
Car:
{carModel} {carSpeed}
Pokemon:
{pokemonName} {pokemonType}
Parents:
{parentName} {parentBirthday}
Children:
{childName} {childBirthday}
```

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter company PeshInc Management 1000.00 | Tom |
| Tom car Volvo 30 | Company: |
| Peter pokemon Pikachu Electricity | Car: |
| Peter parents JohnDoe 22/02/1920 | Volvo 30 |
| Tom pokemon Electrode Electricity | Pokemon: |
| End | Electrode Electricity |
| Tom | Parents: |
|  | Children: |


| **Input** | **Output** |
| --- | --- |
| JohnDoe pokemon Onyx Rock | JohnDoe |
| JohnDoe parents JJ 13/03/1933 | Company: |
| GeorgeAdams pokemon Moltres Fire | JLtd Jelior 777.77 |
| JohnDoe company JLtd Jelior 777.77 | Car: |
| JohnDoe children PJ 01/01/2001 | AudiA4 180 |
| StanSmith pokemon Blastoise Water | Pokemon: |
| JohnDoe car AudiA4 180 | Onyx Rock |
| JohnDoe pokemon Charizard Fire | Charizard Fire |
| End | Parents: |
| JohnDoe | JJ 13/03/1933 |
|  | Children: |
|  | PJ 01/01/2001 |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter company PeshInc Management 1000.00
Tom car Volvo 30
Peter pokemon Pikachu Electricity
Peter parents JohnDoe 22/02/1920
Tom pokemon Electrode Electricity
End
Tom
[/input]
[output]
Tom
Company:
Car:
Volvo 30
Pokemon:
Electrode Electricity
Parents:
Children:
[/output]
[/test]
[test open]
[input]
JohnDoe pokemon Onyx Rock
JohnDoe parents JJ 13/03/1933
GeorgeAdams pokemon Moltres Fire
JohnDoe company JLtd Jelior 777.77
JohnDoe children PJ 01/01/2001
StanSmith pokemon Blastoise Water
JohnDoe car AudiA4 180
JohnDoe pokemon Charizard Fire
End
JohnDoe
[/input]
[output]
JohnDoe
Company:
JLtd Jelior 777.77
Car:
AudiA4 180
Pokemon:
Onyx Rock
Charizard Fire
Parents:
JJ 13/03/1933
Children:
PJ 01/01/2001
[/output]
[/test]
[test]
[input]
K company JC CEO 2000.00
K pokemon P P
K car Audi 50
S parents MJ 19/01/1950
S children KK 20/09/1992
S pokemon B B
End
S
[/input]
[output]
S
Company:
Car:
Pokemon:
B B
Parents:
MJ 19/01/1950
Children:
KK 20/09/1992
[/output]
[/test]
[test]
[input]
K pokemon C C
K pokemon S S
K pokemon S W
K car L 100
M car L 99
M car S 98
E parents P 19/09/1999
E children H 19/08/1998
End
K
[/input]
[output]
K
Company:
Car:
L 100
Pokemon:
C C
S S
S W
Parents:
Children:
[/output]
[/test]
[test]
[input]
V children AR 01/05/1995
A pokemon RA Water
A children IJ 02/06/1993
A car BMW 120
A company SoftUni Janitor 5.00
A parents SN 06/06/1966
End
A
[/input]
[output]
A
Company:
SoftUni Janitor 5.00
Car:
BMW 120
Pokemon:
RA Water
Parents:
SN 06/06/1966
Children:
IJ 02/06/1993
[/output]
[/test]
[test]
[input]
D pokemon Z Z
D parents TB 01/01/1983
D company DC P 500
K company NL JD 2000
K pokemon K K
K parents P 07/23/1960
KT company B CG 100
KT pokemon T T
End
K
[/input]
[output]
K
Company:
NL JD 2000.00
Car:
Pokemon:
K K
Parents:
P 07/23/1960
Children:
[/output]
[/test]
[test]
[input]
T company H EM 999999.99
T children H 01/01/1000
T children A 01/01/1000
T children LR 01/01/1000
T parents N 00/00/0000
T pokemon MR S
End
T
[/input]
[output]
T
Company:
H EM 999999.99
Car:
Pokemon:
MR S
Parents:
N 00/00/0000
Children:
H 01/01/1000
A 01/01/1000
LR 01/01/1000
[/output]
[/test]
[/tests]
[/code-task]
[/slide]