[slide]
# Problem: Count Character Types
[code-task title="Problem: Count Character Types" taskId="9f79317b-6fb7-42f2-8ff9-8cde6dcb5181" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that reads a list of words from the file ( **input.txt** from the Resources - Folder) and finds the count of **vowels**, **consonants**, and **punctuation** marks.

Assume that:

- **a, e, i, o, u** are vowels, only lower case
- **All others** are consonants
- Punctuation marks are **(!,.?)**
- **Do not** count whitespace.

Write the results to another file – **output.txt**.

Use **BufferedReader** and **PrintWriter**.

## Guidelines
There is one zipped folder with resources for all exercises, that you need to use. 

Download the resources folder [here](https://mega.nz/file/nIwjSaKQ#KQpc5igeWhk70YWHwrA7QRqqyAySVW5xap-dxwFULgU).

For each exercise submit only the **output** of your program, **not the code**.

## Examples
| **Input** | **Output** |
| --- | --- |
| On January 1 , 1533 , Michael Angelo, then fifty-seven years old, writes | Vowels: 41 |
| from Florence to Tommaso de' Cavalieri, a youth of noble Roman family, | Consonants: 72 |
|  | Punctuation: 6 |


[/task-description]
[code-io /]
[tests]
[test]
[input]
Vowels: 41
Consonants: 72
Punctuation: 6
[/input]
[output]
Vowels: 41
Consonants: 72
Punctuation: 6
[/output]
[/test]
[/tests]
[/code-task]
[/slide]