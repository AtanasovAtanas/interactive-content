[slide hideTitle]
# Problem: Radioactive Mutant Vampire Bunnies
[code-task title="Problem: Radioactive Mutant Vampire Bunnies" taskId="dde93238-e1ea-4fda-ba5a-a39c4c921bb0" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Browsing through GitHub, you come across an old JS Basics teamwork game.

It is about very nasty bunnies that multiply extremely fast.

There is also a player that has to escape from their lair.

You really like the game so you decide to port it to Java because that is your language of choice.

The last thing that is left is the algorithm that decides if the player will escape the lair or not.

First, you will receive a line holding integers **N** and **M** , which represent the rows and columns in the lair. 

Then you receive **N** strings that can **only** consist of **"."**, **"B"** , **"P"**. 

The **bunnies** are marked with **"B"**, the **player** is marked with **"P"**, and **everything** else is free space, marked with a dot **"."**. 

They represent the initial state of the lair. 

There will be **only** one player. 

Then you will receive a string with **commands** such as **LLRRUUDD** – where each letter represents the next **move** of the player (Left, Right, Up, Down).

**After** each step of the player, each of the bunnies spread to the up, down, left, and right (neighboring cells marked as "." **changes** their value to B). 

If the player **moves** to a bunny cell or a bunny **reaches** the player, the player has died. 

If the player goes **out** of the lair **without** encountering a bunny, the player has won.

When the player **dies** or **wins** , the game ends. 

All the activities for **this** turn continue (e.g. all the bunnies spread normally), but there are no more turns. 

There will be **no** stalemates where the moves of the player end before he dies or escapes.

Finally, print the final state of the lair with every row on a separate line. 

On the last line, print either `dead: {row} {col}` or `won: {row} {col}`. 

Row and col are the coordinates of the cell where the player has died or the last cell he has been in before escaping the lair.

## Input

- On the first line of input, the numbers **N** and **M** are received – the number of **rows** and **columns** in the lair
- On the next N lines, each row is received in the form of a string. The string will contain only ".", "B", "P". All strings will be the same length. There will be only one "P" for all the input
- On the last line, the directions are received in the form of a string, containing "R", "L", "U", "D"

## Output

- On the first N lines, print the final state of the bunny lair
- On the last line, print the outcome – "won:" or "dead:" + `{row} {col}`

## Constraints

- The dimensions of the lair are in the range [3 ... 20]
- The directions string length is in the range [1 ... 20]

## Examples
| **Input** | **Output** |
| --- | --- |
| 5 8 | BBBBBBBB |
| .......B | BBBBBBBB |
| ...B.... | BBBBBBBB |
| ....B..B | .BBBBBBB |
| ........ | ..BBBBBB |
| ..P..... | won: 3 0 |
| ULLL |  |

| **Input** | **Output** |
| --- | --- |
| 4 5 | .B... |
| ..... | BBB.. |
| ..... | BBBB. |
| .B... | BBB.. |
| ...P. | dead: 3 1 |
| LLLLLLLL |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5 8
.......B
...B....
....B..B
........
..P.....
ULLL
[/input]
[output]
BBBBBBBB
BBBBBBBB
BBBBBBBB
.BBBBBBB
..BBBBBB
won: 3 0
[/output]
[/test]
[test open]
[input]
4 5
.....
.....
.B...
...P.
LLLLLLLL
[/input]
[output]
.B...
BBB..
BBBB.
BBB..
dead: 3 1
[/output]
[/test]
[test]
[input]
8 11
...........
...........
.....B.....
...........
...........
....B.....P
...........
..B........
LDRR
[/input]
[output]
...BBBBB...
..BBBBBBB..
.BBBBBBBBB.
..BBBBBBB..
.BBBBBBB...
BBBBBBBBB..
BBBBBBBB...
BBBBBBB....
won: 6 10
[/output]
[/test]
[test]
[input]
3 3
..B
...
P..
UUU
[/input]
[output]
BBB
.BB
..B
dead: 0 0
[/output]
[/test]
[test]
[input]
4 8
........
........
....B...
.......P
R
[/input]
[output]
........
....B...
...BBB..
....B...
won: 3 7
[/output]
[/test]
[test]
[input]
5 5
.....
BP...
.....
B....
.....
RRRR
[/input]
[output]
BBBB.
BBBBB
BBBB.
BBBBB
BBBB.
won: 1 4
[/output]
[/test]
[test]
[input]
20 20
...B................
....................
..........B.........
....................
....................
....................
....................
....................
....................
....................
....................
....................
....................
P...................
....................
....................
....................
....................
....................
....................
RRRRDDDLLLLL
[/input]
[output]
BBBBBBBBBBBBBBBBBBBB
BBBBBBBBBBBBBBBBBBBB
BBBBBBBBBBBBBBBBBBBB
BBBBBBBBBBBBBBBBBBBB
BBBBBBBBBBBBBBBBBBBB
BBBBBBBBBBBBBBBBBBBB
BBBBBBBBBBBBBBBBBBB.
BBBBBBBBBBBBBBBBBB..
BBBBBBBBBBBBBBBBB...
BBBBBBBBBBBBBBBB....
.BBBBBBBBBBBBBB.....
..BBB..BBBBBBB......
...B....BBBBB.......
.........BBB........
..........B.........
....................
....................
....................
....................
....................
won: 16 0
[/output]
[/test]
[test]
[input]
5 5
P....
.....
...B.
.....
.....
RDRD
[/input]
[output]
..BBB
.BBBB
BBBBB
.BBBB
..BBB
dead: 1 2
[/output]
[/test]
[test]
[input]
3 3
...
PB.
...
R
[/input]
[output]
.B.
BBB
.B.
dead: 1 1
[/output]
[/test]
[test]
[input]
7 3
...
.B.
.P.
...
...
...
...
DDDDDDD
[/input]
[output]
BBB
BBB
BBB
BBB
BBB
BBB
.B.
won: 6 1
[/output]
[/test]
[test]
[input]
10 10
B........B
..........
..........
..........
..........
.....P....
..........
..........
..........
B........B
LLLLLLLLL
[/input]
[output]
BBBBBBBBBB
BBBBBBBBBB
BBBB..BBBB
BBB....BBB
BB......BB
BB......BB
BBB....BBB
BBBB..BBBB
BBBBBBBBBB
BBBBBBBBBB
dead: 5 0
[/output]
[/test]
[test]
[input]
4 15
...............
...............
B.............P
...............
LLLLLLLLLLLLL
[/input]
[output]
BBBBBB.........
BBBBBBB........
BBBBBBBB.......
BBBBBBB........
dead: 2 7
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
