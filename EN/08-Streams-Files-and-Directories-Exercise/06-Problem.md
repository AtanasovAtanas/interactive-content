[slide hideTitle]
# Problem: Word Count
[code-task title="Problem: Word Count" taskId="39f0764c-dec5-49f3-870e-5ec7c9a52c27" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that reads a list of words from the file **words.txt** (from the Resources - Folder) and finds how many times each of the words is **contained** in another file **text.txt** (from the Resources – Folder).

Matching should be **case-insensitive**.

Write the results in file **results.txt**. 

Sort the words by frequency in **descending order**.

## Guidelines
There is one zipped folder with resources for all exercises, that you need to use. 

Download the resources folder [here](https://mega.nz/file/nIwjSaKQ#KQpc5igeWhk70YWHwrA7QRqqyAySVW5xap-dxwFULgU).

For each exercise submit only the **output** of your program, **not the code**.

## Examples
| **Input** | **Output** |
| --- | --- |
| of which The | of - 6 |
|  | which - 2 |
|  | The - 1 |

[/task-description]
[code-io /]
[tests]
[test]
[input]
of - 6
which - 2
The - 1
[/input]
[output]
of - 6
which - 2
The - 1
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
