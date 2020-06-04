[slide]
# Problem 3. Moving Target
[code-task title="Problem 3. Moving Target" taskId="88cec4f2-513b-4141-b949-1908afff8ce4" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Description

You are at the shooting gallery again and you need a program that helps you keep track of moving targets.

On the first line, you will receive a **sequence of targets with their integer values**, split by a **single space**.

Then, you will start **receiving commands for manipulating the targets**, until the `End` command.

The commands are the following:

- `Shoot {index} {power}`:

Shoot the target at the index, **if it exists by reducing** its **value** by the **given power (integer value)**.

A target is considered a **shot** when **its value reaches 0**.

Remove the target, **if it is shot**.

- `Add {index} {value}`:

Insert a target with the received value at the received **index**, **if it exists**. If not, print: `Invalid placement!`

- `Strike {index} {radius}`:

Remove the **target at the given index** and the **ones before and after it depending on the radius**, **if such exist**.

**If any of the indices in the range is invalid print:**

`Strike missed!`

**and skip this command.**

### Example:

`Strike 2 2`

`{radius} {radius}` **\{strikeIndex\}** `{radius} {radius}`


## Examples
| **Input** | **Output** |
| --- | --- |
| 52 74 23 44 96 110 | Invalid placement! |
| Shoot 5 10 | 52\|100 |
| Shoot 1 80 |  |
| Strike 2 1 |  |
| Add 22 3 |  |
| End |  |

## Comments

The first command is `Shoot`, so we reduce the target on **index 5**, which is valid, with the given power `–10`.

Then we receive the **same command** but we need to reduce the target on the **1st index**, with power `80`.

The value of this target is `74`, so it is considered shot and we **remove it**.

Then we receive the `Strike` command on the **2nd index** and we need to check if the range with **radius 1 is valid**:

`52 23` **44** `96 100`

And it is, so we **remove** the targets.

At last we receive the `Add` command, but the index is **invalid** so we print the appropriate message and in the end we have the following result:

`52|100`


| **Input** | **Output** |
| --- | --- |
| 47 55 85 78 99 20 | Strike missed! |
| Shoot 1 55 | 22\|47\|50\|40\|85\|78\|99\|20 |
| Shoot 8 15 |  |
| Strike 2 3 |  |
| Add 0 22 |  |
| Add 2 40 |  |
| Add 2 50 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
52 74 23 44 96 110
Shoot 5 10
Shoot 1 80
Strike 2 1
Add 22 3
End
[/input]
[output]
Invalid placement!
52\|100
[/output]
[/test]
[test open]
[input]
47 55 85 78 99 20
Shoot 1 55
Shoot 8 15
Strike 2 3
Add 0 22
Add 2 40
Add 2 50
End
[/input]
[output]
Strike missed!
22\|47\|50\|40\|85\|78\|99\|20
[/output]
[/test]
[test]
[input]
1 2 3
Add 0 1
End
[/input]
[output]
1\|1\|2\|3
[/output]
[/test]
[test]
[input]
1 2 3 4 5
Add 0 1
Add 9 0
End
[/input]
[output]
Invalid placement!
1\|1\|2\|3\|4\|5
[/output]
[/test]
[test]
[input]
1 2 3 4 5
Shoot 3 2
End
[/input]
[output]
1\|2\|3\|2\|5
[/output]
[/test]
[test]
[input]
1 2 3 4 5 6
Shoot 0 1
End
[/input]
[output]
2\|3\|4\|5\|6
[/output]
[/test]
[test]
[input]
1 2 3 4 5
Shoot 9 0
Add 9 0
Add 0 1
End
[/input]
[output]
Invalid placement!
1\|1\|2\|3\|4\|5
[/output]
[/test]
[test]
[input]
1 2 3 4 5 6
Strike 3 1
End
[/input]
[output]
1\|2\|6
[/output]
[/test]
[test]
[input]
1 2 3 4 5
Strike 0 1
End
[/input]
[output]
Strike missed!
1\|2\|3\|4\|5
[/output]
[/test]
[test]
[input]
1 2 3 4 5 6 7 8 9 10
Add 0 1
Add 0 2
Add 12 0
Shoot 5 2
Shoot 6 5
Shoot 7 7
Shoot 13 13
End
[/input]
[output]
Invalid placement!
2\|1\|1\|2\|3\|2\|6\|8\|9\|10
[/output]
[/test]
[test]
[input]
1 2 3 4 5
Add -1 1
Add 0 1
Shoot -1 1
Shoot 0 1
Strike 2 1
Strike 0 3
End
[/input]
[output]
Invalid placement!
Strike missed!
1\|5
[/output]
[/test]
[test]
[input]
1 2 3 3
Strike 1 1
Add 0 1
Add 0 2
Add 0 3
Add 0 4
Add 0 5
Strike 0 5
Shoot -1 1
Add -1 1
Shoot 4 2
End
[/input]
[output]
Strike missed!
Invalid placement!
5\|4\|3\|2\|3
[/output]
[/test]
[/tests]
[/code-task]
[/slide]