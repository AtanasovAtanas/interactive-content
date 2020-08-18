[slide hideTitle]
# Problem: Line Numbers
[code-task title="Line Numbers" taskId="6059845f-06d5-4e57-93db-f665072f1734" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that reads a text file (**inputLineNumbers.txt** from the Resources - Folder) and **inserts** line numbers in front of each of its lines.

The result should be written to **another** text file – **output.txt**.

## Guidelines
There is one zipped folder with resources for all exercises, that you need to use. 

Download the resources folder [here](https://mega.nz/file/nIwjSaKQ#KQpc5igeWhk70YWHwrA7QRqqyAySVW5xap-dxwFULgU).

For each exercise submit only the **output** of your program, **not the code**.

## Examples
| **Input** | **Output** |
| --- | --- |
| Two households, both alike in dignity, | 1. Two households, both alike in dignity, |
| In fair Verona, where we lay our scene, | 2. In fair Verona, where we lay our scene, |
| From ancient grudge break to new, | 3. From ancient grudge break to new, |
| Where civil blood makes civil hands. | 4. Where civil blood makes civil hands. |
| From forth the fatal loins of these two | 5. From forth the fatal loins of these two  |
| A pair of star-cross'd lovers take their life; | 6. A pair of star-cross'd lovers take their life; |
| Whose misadventured piteous overthrows | 7. Whose misadventured piteous overthrows |
| Do with their death bury their parents' strife. | 8. Do with their death bury their parents' strife. |

[/task-description]
[code-io /]
[tests]
[test]
[input]
1. Two households, both alike in dignity,
2. In fair Verona, where we lay our scene,
3. From ancient grudge break to new,
4. Where civil blood makes civil hands.
5. From forth the fatal loins of these two 
6. A pair of star-cross'd lovers take their life;
7. Whose misadventured piteous overthrows
8. Do with their death bury their parents' strife.
[/input]
[output]
1. Two households, both alike in dignity,
2. In fair Verona, where we lay our scene,
3. From ancient grudge break to new,
4. Where civil blood makes civil hands.
5. From forth the fatal loins of these two 
6. A pair of star-cross'd lovers take their life;
7. Whose misadventured piteous overthrows
8. Do with their death bury their parents' strife.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
