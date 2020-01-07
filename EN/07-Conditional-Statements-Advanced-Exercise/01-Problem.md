[slide]
# Problem: Personal Titles
[code-task title="Personal Titles" taskId="CAE-p-01" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
# Description

Write a **console** program **that reads** age (floating-point number) and **gender**("**m**" or "**f**") and prints **address** among these:
- "**Mr.**" - a man (gender "**m**") of age 16 or more
- "**Master**" - a boy (gender "**m**") under 16 years old
- "**Ms.**" - a woman (gender "**f**") of age 16 or more
- "**Miss**" - a girl (gender "**f**") under 16 years old

# Input
Enter from the console:
- age - floating-point number
- gender - "**m**" or "**f**"

# Output
Print the expected address on a single line.

# Example

| **Input** | | **Output** | 
| --- | --- | --- |
| 25 | | Ms. |
| f | | |

| **Input** | | **Output** | 
| --- | --- | --- |
| 13.5 | | Master |
| m | | |
[/task-description]
[tests]
[test]
[input]
12
f
[/input]
[output]
Miss
[/output]
[/test]
[test]
[input]
17
m
[/input]
[output]
Mr.
[/output]
[/test]
[test]
[input]
25
f
[/input]
[output]
Ms.
[/output]
[/test]
[test]
[input]
13.5
m
[/input]
[output]
Master
[/output]
[/test]
[test]
[input]
11
f
[/input]
[output]
Miss
[/output]
[/test]
[test]
[input]
19
m
[/input]
[output]
Mr.
[/output]
[/test]
[test]
[input]
30
f
[/input]
[output]
Ms.
[/output]
[/test]
[test]
[input]
14
m
[/input]
[output]
Master
[/output]
[/test]
[test]
[input]
4.5
m
[/input]
[output]
Master
[/output]
[/test]
[test]
[input]
16
m
[/input]
[output]
Mr.
[/output]
[/test]
[test]
[input]
16
f
[/input]
[output]
Ms.
[/output]
[/test]
[test]
[input]
15.9
m
[/input]
[output]
Master
[/output]
[/test]
[test]
[input]
15.9
f
[/input]
[output]
Miss
[/output]
[/test]
[test]
[input]
95.125
m
[/input]
[output]
Mr.
[/output]
[/test]
[/tests]
[code-io /]
[/code-task]
[/slide]