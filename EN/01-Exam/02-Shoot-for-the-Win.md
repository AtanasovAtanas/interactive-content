[slide]
# Problem 2. Shoot for the Win
[code-task title="Problem 2. Shoot for the Win" taskId="java-fundamentals-regex-2" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that helps you keep track of your **shot targets**.

You will receive **a sequence with integers**, separated by single space, representing targets and their value.

Afterward, you will be receiving indices until the `End` command is given and you need to print the **targets** and the **count of shot targets**.

Every time you receive an **index**, you need to shoot the target on that index, **if it is possible**.

Every time you **shoot a target**, its value becomes **-1 and it is considered shot**.

Along with that you also need to **Reduce** all the other **targets**, which have **greater values** than your **current** target, **with its value**.

All the **targets**, which **have less than or equal** value to the **shot target**, you need to **increase with its value**.

**Keep in mind that you can't shoot a target, which is already shot**.

**You also can't increase or reduce a target, which is considered shot**.

When you receive the `End` command, print the targets in their current state and the count of shot targets in the following format:

`Shot targets: {count} -> {target1} {target2}… {targetn}`

## Input \/ Constraints

- On the **first line** of input, you will receive a **sequence** of **integers**, **separated** by a **single space** – **the target sequence**.

- On the **next lines**, until the `End` command you be receiving **integers** each on a single line – **the index of the target to be shot**.

## Output

- The format of the output is described above in the problem description.


## Examples
| **Input** | **Output** |
| --- | --- |
| 30 30 12 60 54 66 | Shot targets: 4 -\> -1 120 -1 66 -1 -1 |
| 5 |  |
| 2 |  |
| 4 |  |
| 0 |  |
| End |  |

### Comments

First we shoot target on **index 0**.

It becomes **equal to -1** and we start going through the rest of the targets.

Since `50` is more than `24`, we reduce it to `26` and `36` to `12` and `70` to `46`.

The sequence looks like that:
`-1 26 12 46`

The next index is **invalid**, so we don't do anything.

Index 3 is **valid** and after the operations our sequence should look like that:
`-1 72 58 -1`

Then we take the **first index** with value `72` and our sequence looks like that:
`-1 -1 130 -1`

Then we print the result after the `End` command.

| **Input** | **Output** |
| --- | --- |
| 24 50 36 70 | Shot targets: 4 -\> -1 120 -1 66 -1 -1 |
| 0 |  |  
| 4 |  |
| 3 |  |
| 1 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
24 50 36 70
0
4
3
1
End
[/input]
[output]
Shot targets: 3 -\> -1 -1 130 -1
[/output]
[/test]
[test open]
[input]
30 30 12 60 54 66
5
2
4
0
End
[/input]
[output]
Shot targets: 4 -\> -1 120 -1 66 -1 -1
[/output]
[/test]
[test]
[input]
1 2 3
End
[/input]
[output]
Shot targets: 0 -\> 1 2 3
[/output]
[/test]
[test]
[input]
1 2
1
End
[/input]
[output]
Shot targets: 1 -\> 3 -1
[/output]
[/test]
[test]
[input]
1 1 1 2
3
End
[/input]
[output]
Shot targets: 1 -\> 3 3 3 -1
[/output]
[/test]
[test]
[input]
0 0 0
1
7
End
[/input]
[output]
Shot targets: 1 -\> 0 -1 0
[/output]
[/test]
[test]
[input]
3 3
1
7
End
[/input]
[output]
Shot targets: 1 -\> 6 -1
[/output]
[/test]
[test]
[input]
3 3 3 3 3 3 3
0
7
End
[/input]
[output]
Shot targets: 1 -\> -1 6 6 6 6 6 6
[/output]
[/test]
[test]
[input]
1 5 6 7
0
7
End
[/input]
[output]
Shot targets: 1 -\> -1 4 5 6
[/output]
[/test]
[test]
[input]
1 2 3 4 5
0
4
7
End
[/input]
[output]
Shot targets: 2 -\> -1 5 6 7 -1
[/output]
[/test]
[test]
[input]
1 2 2 3 4
0
4
1
7
End
[/input]
[output]
Shot targets: 3 -\> -1 -1 8 1 -1
[/output]
[/test]
[test]
[input]
1 1 2 2 3 3 4 4 5 5
0
9
10
End
[/input]
[output]
Shot targets: 2 -\> -1 6 5 5 6 6 7 7 8 -1
[/output]
[/test]
[/tests]
[/code-task]
[/slide]