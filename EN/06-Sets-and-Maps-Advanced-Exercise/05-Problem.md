[slide]
# Problem: Phonebook
[code-task title="Problem: Phonebook" taskId="9530e974-a298-483a-a529-354207c85293" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that receives some info from the console about **people** and their **phone numbers**.

You are free to choose how the data is entered; each **entry** should have just **one name** and **one number** (both of them strings). 

If you receive a name that **already exists** in the phonebook, simply update its number.

After filling this simple phonebook, upon receiving the **command "search"**, your program should be able to perform a search of contact by name and print the details in the format `{name} -> {number}`. 

In case the contact isn't found, print `Contact {name} does not exist.`


## Examples
| **Input** | **Output** |
| --- | --- |
| John-00359888080808 | Contact Maria does not exist. |
| search | John -> 00359888080808 |
| Maria |  |
| John |  |
| stop |  |

| **Input** | **Output** |
| --- | --- |
| John-00359888001122 | Samuel -> 0047123123123 |
| Peter-0040333111000 | Contact samuel does not exist. |
| George-0049112233 | Contact PeTeR does not exist. |
| Samuel-0047123123123 | Peter -> 0040333111000 |
| search |  |
| Samuel |  |
| samuel |  |
| PeTeR |  |
| Peter |  |
| stop |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
John-00359888080808
search
Maria
John
stop
[/input]
[output]
Contact Maria does not exist.
John -\> 00359888080808
[/output]
[/test]
[test open]
[input]
John-00359888001122
Peter-0040333111000
George-0049112233
Samuel-0047123123123
search
Samuel
samuel
PeTeR
Peter
stop
[/input]
[output]
Samuel -\> 0047123123123
Contact samuel does not exist.
Contact PeTeR does not exist.
Peter -\> 0040333111000
[/output]
[/test]
[test]
[input]
Peter-00359888001122
Daniel-004312345678
James-0032987654321
Oscar-003011335577
search
Oscar
Daniele
James
Pete
stop
[/input]
[output]
Oscar -\> 003011335577
Contact Daniele does not exist.
James -\> 0032987654321
Contact Pete does not exist.
[/output]
[/test]
[test]
[input]
Abby-0049112233
Barbara-0033999888777
Daisy-0037166668888
Faith-0034333555777
Gabriela-0040333111000
Ella-0047123123123
search
Daisy
Gabrielle
Faith
Aby
stop
[/input]
[output]
Daisy -\> 0037166668888
Contact Gabrielle does not exist.
Faith -\> 0034333555777
Contact Aby does not exist.
[/output]
[/test]
[test]
[input]
search
stop
[/input]
[output]

[/output]
[/test]
[test]
[input]
France-0033
Germany-0049
Srain-0034
Portugal-00351
Italy-0039
Netherlands-0031
Greece-0030
Austria-0043
search
Ireland
Bulgaria
Estonia
Finland
Norway
stop
[/input]
[output]
Contact Ireland does not exist.
Contact Bulgaria does not exist.
Contact Estonia does not exist.
Contact Finland does not exist.
Contact Norway does not exist.
[/output]
[/test]
[test]
[input]
Oliver-004455667788
Sophia-003344556677
search
Sophia
Oliver
stop
[/input]
[output]
Sophia -\> 003344556677
Oliver -\> 004455667788
[/output]
[/test]
[/tests]
[/code-task]
[/slide]