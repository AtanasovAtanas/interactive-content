[slide]
# Problem 1. Counter Strike
[code-task title="Problem 1. Counter Strike" taskId="0b90ee7d-e7d0-4fe3-acf1-c5ee916860ae" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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

Write a program that **keeps track of every won** battle against an **enemy**.

You will receive **initial energy**.

Afterward, you will start receiving the **distance** you need to **go to reach an enemy** until the `End of battle` command is given, or until you **run out of energy**.

The **energy** you need for reaching an enemy is **equal to the distance you receive**.

Each time you reach an enemy, your **energy is reduced**.

This is considered a successful battle **win**.

If you don't have **enough energy** to reach the enemy, print:

`Not enough energy! Game ends with {count} won battles and {energy} energy`

and **end the program**.

Every **third won battle** increases **your energy with the value of your current count of won battles**.

Upon receiving the `End of battle` command, print the **count of won battles** in the following format:

`Won battles: {count}. Energy left: {energy}`

## Input \/ Constraints

- On the **first line**, you will receive **initial energy** – an **integer 1-10000**

- On the **next lines**, you will be receiving distance of the enemy – **an integer 1-10000**

## Output

- The description contains the proper output messages for each case and the format in which they
should be print.

## Examples
| **Input** | **Output** |
| --- | --- |
| 200 | Won battles: 4. Energy left: 94 |
| 54 |  |
| 14 |  |
| 28 |  |
| 13 |  |
| End of battle |  |

### Comments

The initial energy is `100`.

The first distance is `10`, so we **subtract** `10` from `100` and we consider this a **won battle**.

We are left with `90` energy.

Next distance `–10`, and `80` energy left.

Next distance `–10`, `3` won battles and `70` energy, but since **we have 3 won battles**, we increase the energy with the current count of won battle, in this case `–3` and it becomes `73`.

The last distance we receive `–10` is unreachable since we have `0` energy, so we print the appropriate message and the program ends.

| **Input** | **Output** |
| --- | --- |
| 100 | Not enough energy! Game ends with 7 won battles and 0 energy |
| 10 |  |
| 10 |  |
| 10 |  |
| 1 |  |
| 2 |  |
| 3 |  |
| 73 |  |
| 10 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
100
10
10
10
1
2
3
73
10
[/input]
[output]
Not enough energy! Game ends with 7 won battles and 0 energy
[/output]
[/test]
[test open]
[input]
200
54
14
28
13
End of battle
[/input]
[output]
Won battles: 4. Energy left: 94
[/output]
[/test]
[test]
[input]
10
1
1
1
1
1
1
1
1
1
End of battle
[/input]
[output]
Won battles: 9. Energy left: 19
[/output]
[/test]
[test]
[input]
20
10
10
10
10
End of battle
[/input]
[output]
Not enough energy! Game ends with 2 won battles and 0 energy
[/output]
[/test]
[test]
[input]
20
3
3
3
12
12
[/input]
[output]
Not enough energy! Game ends with 4 won battles and 2 energy
[/output]
[/test]
[test]
[input]
100
150
End of battle
[/input]
[output]
Not enough energy! Game ends with 0 won battles and 100 energy
[/output]
[/test]
[test]
[input]
500
500
End of battle
[/input]
[output]
Won battles: 1. Energy left: 0
[/output]
[/test]
[test]
[input]
200
100
End of battle
[/input]
[output]
Won battles: 1. Energy left: 100
[/output]
[/test]
[test]
[input]
200
20
20
20
20
20
20
89
End of battle
[/input]
[output]
Won battles: 7. Energy left: 0
[/output]
[/test]
[/tests]
[/code-task]
[/slide]