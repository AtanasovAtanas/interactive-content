[slide hideTitle]
# Problem: CAPITAL LETTERS
[code-task title="Problem: CAPITAL LETTERS" taskId="4c58e831-a4f5-4845-9b41-e083d08eac22" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that reads a text file ( **input.txt** from the Resources - Folder) and changes the casing of **all** letters to **upper**.

Write the output to another file ( **output.txt** ).

Use **BufferedReader** and **PrintWriter**.

## Guidelines
There is one zipped folder with resources for all exercises, that you need to use. 

Download the resources folder [here](https://mega.nz/file/nIwjSaKQ#KQpc5igeWhk70YWHwrA7QRqqyAySVW5xap-dxwFULgU).

For each exercise submit only the **output** of your program, **not the code**.

## Examples
| **Input** | **Output** |
| --- | --- |
| On January 1 , 1533 ,  | ON JANUARY 1 , 1533 ,  |
| Michael Angelo,  | MICHAEL ANGELO,  |
| then fifty-seven years old,  | THEN FIFTY-SEVEN YEARS OLD,  |
| writes | WRITES |
| from Florence to  | FROM FLORENCE TO  |
| Tommaso de' Cavalieri,  | TOMMASO DE' CAVALIERI,  |
| a youth of noble Roman family, | A YOUTH OF NOBLE ROMAN FAMILY, |

[/task-description]
[code-io /]
[tests]
[test]
[input]
ON JANUARY 1 , 1533 , 
MICHAEL ANGELO, 
THEN FIFTY-SEVEN YEARS OLD, 
WRITES
FROM FLORENCE TO 
TOMMASO DE' CAVALIERI, 
A YOUTH OF NOBLE ROMAN FAMILY,
[/input]
[output]
ON JANUARY 1 , 1533 , 
MICHAEL ANGELO, 
THEN FIFTY-SEVEN YEARS OLD, 
WRITES
FROM FLORENCE TO 
TOMMASO DE' CAVALIERI, 
A YOUTH OF NOBLE ROMAN FAMILY,
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
