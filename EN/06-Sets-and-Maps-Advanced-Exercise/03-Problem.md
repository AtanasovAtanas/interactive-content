[slide]
# Problem: Periodic Table
[code-task title="Problem: Periodic Table" taskId="3cdc56cd-58c0-49aa-aa7f-49105f144cca" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are given an **n** number of **chemical compounds**.

You need to **keep track of all chemical elements** used in the compounds and at the end print all **unique ones in ascending order**:

## Examples
| **Input** | **Output** |
| --- | --- |
| 4 | Ce Ee Mo O |
| Ce O |  |
| Mo O Ce |  |
| Ee |  |
| Mo |  |

| **Input** | **Output** |
| --- | --- |
| 3 | Ch Ge Mo Nb Ne O Tc |
| Ge Ch O Ne |  |
| Nb Mo Tc |  |
| O Ne |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
4
Ce O
Mo O Ce
Ee
Mo
[/input]
[output]
Ce Ee Mo O
[/output]
[/test]
[test open]
[input]
3
Ge Ch O Ne
Nb Mo Tc
O Ne
[/input]
[output]
Ch Ge Mo Nb Ne O Tc
[/output]
[/test]
[test]
[input]
6
He Cl Na
Na
Fe
Si
He Cl
Ca
[/input]
[output]
Ca Cl Fe He Na Si
[/output]
[/test]
[test]
[input]
2
Al Ca Li
B Br U
[/input]
[output]
Al B Br Ca Li U
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
8
F Ne
Ar I
Ge Mg
Pt Te
Pt Te
Ge Mg
Ar I
F Ne
[/input]
[output]
Ar F Ge I Mg Ne Pt Te
[/output]
[/test]
[test]
[input]
5
Zn Ni Sn Ba As
Kr Co Cs Y W
As Ba Sn Ni Zn
W Y Cs Co Kr
Zn Ni Sn Ba As
[/input]
[output]
As Ba Co Cs Kr Ni Sn W Y Zn
[/output]
[/test]
[/tests]
[/code-task]
[/slide]