[slide]
# Problem: The Heigan Dance
[code-task title="Problem: The Heigan Dance" taskId="20bc5407-c957-4f8b-94d1-9aa365be70a2" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
At last, level 80.

And what do level eighties do? Go raiding.

This is where you are now – trying not to be wiped by the famous dance boss, Heigan the Unclean.

The fight is pretty straightforward - dance around the Plague Clouds and Eruptions, and you will be just fine.

Heigan's chamber is a 15-by-15 two-dimensional array. 

The player always starts at the **exact center**. 

For each turn, Heigan uses a spell that hits a certain cell and the neighboring **rows/columns**. 

For example, if he hits (1,1), he also hits (0,0, 0,1, 0,2, 1,0 ... 2,2). 

If the player's current position is within the area of damage, the player tries to move. 

First, he tries to move **up**, if there is **damage/wall**, he tries to move **right** , then **down**, then **left**. 

If he **cannot move** in any direction, because **the cell is damaged** or there is **a wall**, the player **stays** in place and takes the damage.

**Plague cloud** does 3500 damage **when it hits**, and 3500 damage **the next turn**. Then it **expires**. 

**Eruption** does 6000 damage **when it hits.** 

If a spell hits a player that also has an active Plague Cloud from the previous turn, the **cloud** damage is applied **first**. 

**Both** Heigan and the player **may** die in the same turn. 

If Heigan is **dead** , the spell he **would** have casted is **ignored**.

The player always starts at **18500** hit points; Heigan starts at **3,000,000** hit points. **Each** turn, the player does damage to Heigan. 

The fight is over either when the player is **killed** , or Heigan is **defeated**.

## Input

- On the first line you receive a floating-point number **D –** the damage done to Heigan each turn
- On the next several lines – you receive input in format **\{spell\} \{row\} \{col\}** – **\{spell\}** is either **Cloud** or **Eruption**

## Output

- On the first line
  - If Heigan is defeated: **"Heigan: Defeated!"**
  - Else: **"Heigan: \{remaining\}"**, where remaining is rounded to two digits after the decimal separator
- On the second line:
  - If the player is killed: **"Player: Killed by \{spell\}"**
  - Else **"Player: \{remaining\}"**
- On the third line: **"Final position: \{row, col\}"** -> the last coordinates of the player

## Constraints

- **D** is a floating-point number in range [0 ... 500000]
- A damaging spell will always affect at least one cell
- Allowed memory: 16 MB
- Allowed working time: 0.25s

## Examples
| **Input** | **Output** |
| --- | --- |
| 10000 | Heigan: 2960000.00 |
| Cloud 7 7 | Player: Killed by Eruption |
| Eruption 6 7 | Final position: 8, 7 |
| Eruption 8 7 |  |
| Eruption 8 7 |  |

| **Input** | **Output** |
| --- | --- |
| 500000 | Heigan: Defeated! |
| Cloud 7 6 | Player: 12500 |
| Eruption 7 8 | Final position: 7, 11 |
| Eruption 7 7 |  |
| Cloud 7 8 |  |
| Eruption 7 9 |  |
| Eruption 6 14 |  |
| Eruption 7 11 |  |

| **Input** | **Output** |
| --- | --- |
| 12500.66 | Heigan: 2949997.36 |
| Cloud 7 7 | Player: Killed by Plague Cloud |
| Cloud 7 7 | Final position: 7, 7 |
| Cloud 7 7 |  |
| Cloud 7 7 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
10000
Cloud 7 7
Eruption 6 7
Eruption 8 7
Eruption 8 7
[/input]
[output]
Heigan: 2960000.00
Player: Killed by Eruption
Final position: 8, 7
[/output]
[/test]
[test open]
[input]
500000
Cloud 7 6
Eruption 7 8
Eruption 7 7
Cloud 7 8
Eruption 7 9
Eruption 6 14
Eruption 7 11
[/input]
[output]
Heigan: Defeated!
Player: 12500
Final position: 7, 11
[/output]
[/test]
[test open]
[input]
12500.66
Cloud 7 7
Cloud 7 7
Cloud 7 7
Cloud 7 7
[/input]
[output]
Heigan: 2949997.36
Player: Killed by Plague Cloud
Final position: 7, 7
[/output]
[/test]
[test]
[input]
123123.1
Eruption 7 6
Eruption 7 7
Eruption 7 8
Eruption 7 9
Eruption 7 10
Eruption 7 11
Eruption 7 12
Eruption 8 13
Eruption 7 14
Eruption 6 14
Eruption 5 14
Eruption 4 14
Eruption 3 14
Eruption 2 14
Eruption 1 15
Eruption 0 14
Eruption 0 13
Eruption 0 12
Eruption 0 11
Eruption 0 10
Eruption 0 9
Eruption 0 8
Eruption 0 7
Eruption 0 6
Eruption 0 5
[/input]
[output]
Heigan: Defeated!
Player: 18500
Final position: 0, 4
[/output]
[/test]
[test]
[input]
0.5
Cloud 7 8
Cloud 7 7
Cloud 7 6
Cloud 7 4
Cloud 7 4
Cloud 7 4
Eruption 7 4
[/input]
[output]
Heigan: 2999996.50
Player: Killed by Plague Cloud
Final position: 7, 4
[/output]
[/test]
[test]
[input]
0.5
Cloud 7 8
Cloud 7 7
Cloud 7 6
Cloud 7 4
Cloud 7 4
Eruption 7 4
[/input]
[output]
Heigan: 2999997.00
Player: Killed by Eruption
Final position: 7, 4
[/output]
[/test]
[test]
[input]
0.59
Cloud 7 8
Cloud 7 7
Cloud 7 6
Cloud 7 5
Eruption 7 4
Eruption 7 3
Eruption 7 2
Eruption 7 1
Cloud 7 1
Cloud 7 1
Eruption 7 1
[/input]
[output]
Heigan: 2999993.51
Player: Killed by Plague Cloud
Final position: 7, 0
[/output]
[/test]
[test]
[input]
250000.15
Eruption 14 14
Eruption 6 7
Eruption 7 7
Cloud 8 7
Cloud 10 6
Cloud 10 7
Eruption 10 10
Eruption 10 9
Eruption 10 8
Eruption 10 7
Cloud 10 5
Cloud 10 4
[/input]
[output]
Heigan: Defeated!
Player: 11500
Final position: 10, 5
[/output]
[/test]
[test]
[input]
123.12
Eruption 10 10
Cloud 8 6
Cloud 11 8
Cloud 7 7
Eruption 6 7
Eruption 5 7
Eruption 3 7
Eruption 3 7
Eruption 3 7
Eruption 3 7
Cloud 3 7
Cloud 3 7
[/input]
[output]
Heigan: 2998768.80
Player: Killed by Eruption
Final position: 3, 7
[/output]
[/test]
[test]
[input]
498781.84
Eruption 6 8
Eruption 7 7
Eruption 8 7
Eruption 9 7
Eruption 10 7
Cloud 12 7
Eruption 12 7
[/input]
[output]
Heigan: Defeated!
Player: 11500
Final position: 12, 7
[/output]
[/test]
[test]
[input]
10298.08
Cloud 8 8
Cloud 7 7
Cloud 6 7
Cloud 5 7
Cloud 4 7
Cloud 3 7
Cloud 1 7
Cloud 2 7
Cloud 1 7
Cloud 1 7
Eruption 1 7
[/input]
[output]
Heigan: 2886721.12
Player: Killed by Plague Cloud
Final position: 0, 7
[/output]
[/test]
[test]
[input]
111111.111
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 8
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
Cloud 1 1
Cloud 0 5
Cloud 7 6
Eruption 7 1
[/input]
[output]
Heigan: Defeated!
Player: 11500
Final position: 7, 8
[/output]
[/test]
[test]
[input]
54789.01
Cloud 7 8
Cloud 7 7
Cloud 7 6
Cloud 7 5
Cloud 7 4
Cloud 7 3
Cloud 7 2
Cloud 8 1
Cloud 7 0
Cloud 6 0
Cloud 5 0
Cloud 4 0
Cloud 3 0
Cloud 2 0
Cloud 0 -1
Cloud 0 0
Cloud 0 1
Cloud 0 2
Cloud 0 3
Cloud 0 4
Cloud 0 5
Cloud 0 6
Cloud 0 7
Cloud 0 7
Cloud 0 7
Cloud 0 7
Cloud 0 7
Eruption 0 7
Cloud 0 7
Cloud 0 7
Cloud 0 7
Eruption 0 7
Cloud 0 7
Cloud 0 7
Cloud 0 7
Eruption 0 7
Cloud 0 7
Cloud 0 7
Cloud 0 7
Eruption 0 7
Cloud 0 7
Cloud 0 7
Cloud 0 7
Eruption 0 7
Cloud 0 7
Cloud 0 7
Cloud 0 7
Eruption 0 7
Cloud 0 7
Cloud 0 7
Eruption 0 7
Eruption 0 9
Eruption 0 9
Cloud 0 9
Eruption 0 9
[/input]
[output]
Heigan: Defeated!
Player: Killed by Plague Cloud
Final position: 0, 9
[/output]
[/test]
[/tests]
[/code-task]
[/slide]