[slide hideTitle]
# Problem: Speed Racing
[code-task title="Problem: Speed Racing" taskId="51ee0d4e-daac-43b6-8bde-2477b2e01912" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Your task is to implement a program that keeps track of cars and their fuel and supports methods for moving cars.

Define a class **Car** that keeps track of a car information **Model, fuel amount, fuel cost for 1 kilometer**, and **distance traveled**.

A Car Model is **unique** - there will never be 2 cars with the same model.

On the first line of the input you will receive a number **N** - the number of cars you need to track. 

On **each** of the next **N** lines you will receive information for a car in the following format: 

`<Model> <FuelAmount> <FuelCostFor1km>`

All **cars start at 0 kilometers traveled**.

After the **N** lines until the command `End` is received, you will receive commands in the following format: 

`Drive <CarModel> <amountOfKm>`

Implement a method in the **Car** class to calculate whether a car **can** move that distance or **not**. 

If it can, the car **fuel amount** should be **reduced** by the amount of used fuel and its **distance traveled** should be increased by the number of kilometers traveled, otherwise the car should not move (its fuel amount and distance traveled should stay the same) and you should print on the console 

`Insufficient fuel for the drive` 

After the `End` command is received, print each car in order of appearing in input and its current fuel amount and distance traveled in the format:

`<Model> <fuelAmount> <distanceTraveled>`

Where the fuel amount should be rounded to the **second decimal place**.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | AudiA4 17.60 18 |
| AudiA4 23 0.3 | BMW-M2 21.48 56 |
| BMW-M2 45 0.42 |  |
| Drive BMW-M2 56 |  |
| Drive AudiA4 5 |  |
| Drive AudiA4 13 |  |
| End |  |

| **Input** | **Output** |
| --- | --- |
| 3 | Insufficient fuel for the drive |
| AudiA4 18 0.34 | Insufficient fuel for the drive |
| BMW-M2 33 0.41 | AudiA4 1.00 50 |
| Ferrari-488Spider 50 0.47 | BMW-M2 33.00 0 |
| Drive Ferrari-488Spider 97 | Ferrari-488Spider 4.41 97 |
| Drive Ferrari-488Spider 35 |  |
| Drive AudiA4 85 |  |
| Drive AudiA4 50 |  |
| End |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
AudiA4 23 0.3
BMW-M2 45 0.42
Drive BMW-M2 56
Drive AudiA4 5
Drive AudiA4 13
End
[/input]
[output]
AudiA4 17.60 18
BMW-M2 21.48 56
[/output]
[/test]
[test open]
[input]
3
AudiA4 18 0.34
BMW-M2 33 0.41
Ferrari-488Spider 50 0.47
Drive Ferrari-488Spider 97
Drive Ferrari-488Spider 35
Drive AudiA4 85
Drive AudiA4 50
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
AudiA4 1.00 50
BMW-M2 33.00 0
Ferrari-488Spider 4.41 97
[/output]
[/test]
[test]
[input]
3
MustangGTR 80 4.9
FerarriGTR 10 5.5
Moher 10 0.1
Drive MustangGTR 25
Drive MustangGTR 10
Drive FerarriGTR 100
Drive FerarriGTR 1
Drive Moher 101
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
Insufficient fuel for the drive
MustangGTR 31.00 10
FerarriGTR 4.50 1
Moher 10.00 0
[/output]
[/test]
[test]
[input]
5
M1 10 1.1
M2 20 1.2
M3 40 2
M4 40 4
M 100 5
Drive M1 5
Drive M2 20
Drive M 15
Drive M1 70
Drive M3 20
Drive M4 20
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
Insufficient fuel for the drive
M1 4.50 5
M2 20.00 0
M3 0.00 20
M4 40.00 0
M 25.00 15
[/output]
[/test]
[test]
[input]
3
M100 90 6
T 100 5
H 200 7
Drive M100 15
Drive M100 10
Drive T 1000
Drive T 25
Drive H 25
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
Insufficient fuel for the drive
M100 0.00 15
T 100.00 0
H 25.00 25
[/output]
[/test]
[test]
[input]
3
K 5 0.1
S 9 10
T 10 0.2
Drive K 5
Drive K 15
Drive S 100
Drive T 15
End
[/input]
[output]
Insufficient fuel for the drive
K 3.00 20
S 9.00 0
T 7.00 15
[/output]
[/test]
[test]
[input]
5
B 50 1
S 5 0.5
M 1 0.5
D 15 2
K 20 5
Drive B 49
Drive S 10
Drive D 7
Drive D 1
Drive K 3
Drive K 1
Drive M 100
End
[/input]
[output]
Insufficient fuel for the drive
Insufficient fuel for the drive
B 1.00 49
S 0.00 10
M 1.00 0
D 1.00 7
K 0.00 4
[/output]
[/test]
[/tests]
[/code-task]
[/slide]