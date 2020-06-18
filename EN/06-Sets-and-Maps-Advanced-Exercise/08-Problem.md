[slide]
# Problem: Hands Of Cards
[code-task title="Problem: Hands Of Cards" taskId="e2bf2871-f2e7-44de-950e-0363166d4557" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are given a sequence of people and for every person what **cards** he draws from the deck.

The input will be **separate** lines in the **format**:

`{personName}: {PT, PT, PT,… PT}`

Where P (2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A) is the power of the card and T (S, H, D, C) is the type. The input ends when a **"JOKER"** is drawn. 

The name can contain any ASCII symbol except **":"**. 

The input will always be valid and in the format described, there is no need to check it.

A single person **cannot have more than one** card with the same power and type, if he draws such a card he **discards** it. 

The people are playing with **multiple decks**. 

Each card has a value that is **calculated** by the power multiplied by the type. 

Powers **2 to 10** have the same value and **J to A** are **11 to 14**. 

Types are mapped to multipliers the following way (**S -> 4, H-> 3, D -> 2, C -> 1**).

Finally print out the **total value each player** has in his hand in the format:

`{personName}: {value}`

## Examples
| **Input** | **Output** |
| --- | --- |
| Peter: 2C, 4H, 9H, AS, QS | Peter: 167 |
| Jenny: 3H, 10S, JC, KD, 5S, 10S | Jenny: 175 |
| Alice: QH, QC, QS, QD | Alice: 197 |
| Jenny: 6H, 7S, KC, KD, 5S, 10C |  |
| Alice: QH, QC, JS, JD, JC |  |
| Peter: JD, JD, JD, JD, JD, JD |  |
| JOKER |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Peter: 2C, 4H, 9H, AS, QS
Jenny: 3H, 10S, JC, KD, 5S, 10S
Alice: QH, QC, QS, QD
Jenny: 6H, 7S, KC, KD, 5S, 10C
Alice: QH, QC, JS, JD, JC
Peter: JD, JD, JD, JD, JD, JD
JOKER
[/input]
[output]
Peter: 167
Jenny: 175
Alice: 197
[/output]
[/test]
[test]
[input]
Jonathan Davis: JD, JD, JD, JD
JOKER
[/input]
[output]
Jonathan Davis: 22
[/output]
[/test]
[test]
[input]
John: 2C, 4H, 9H, AS, QS
Peter: 3H, 10S, JC, KD, 5S, 10S
Steve: QH, QC, QS, QD
Alice: 6H, 7S, KC, KD, 5S, 10C
Jenny: QH, QC, JS, JD, JC
Sandra: JD, 7D, 3D, 4D, 5D, 6D
JOKER
[/input]
[output]
John: 145
Peter: 106
Steve: 120
Alice: 115
Jenny: 125
Sandra: 72
[/output]
[/test]
[test]
[input]
JOKER
[/input]
[output]

[/output]
[/test]
[/tests]
[/code-task]
[/slide]