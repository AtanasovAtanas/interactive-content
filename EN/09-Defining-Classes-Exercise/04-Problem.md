[slide hideTitle]
# Problem: Raw Data
[code-task title="Raw Data" taskId="45d1be24-82dd-4ff1-9586-d02e73ff698d" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are the owner of a courier company and you want to make a system for tracking your cars and their cargo.

Define a class **Car** that holds information about **model, engine, cargo**, and a **collection of exactly 4 tires**.

The engine, cargo, and tire **should be separate classes**, create a constructor that receives all information about the Car, and creates and initializes its inner components (engine, cargo, and tires).

On the first line of the input you will receive a number **N** - the number of cars you have. 

On each of the next **N** lines you will receive information about a car in the format: 

`<model> <engineSpeed> <enginePower> <cargoWeight> <cargoType> <tire1Pressure> <tire1Age> <tire2Pressure> <tire2Age> <tire3Pressure> <tire3Age> <tire4Pressure> <tire4Age>`

Where the speed, power, weight and tire age are **integers**, tire pressure is a **double**.

After the **N** lines you will receive a single line with one of 2 commands `fragile` or `flamable`.

If the command is `fragile` print all cars whose **cargoType is** `fragile` with a **tire** whose **pressure is < 1**.

If the command is `flamable` print all cars whose **cargoType is** `flamable` and have **enginePower > 250**. 

The cars should be printed in order of appearing in the input on a separate lines.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | Citroen2CV |
| ChevroletAstro 200 180 1000 fragile 1.3 1 1.5 2 1.4 2 1.7 4 |  |
| Citroen2CV 190 165 1200 fragile 0.9 3 0.85 2 0.95 2 1.1 1 |  |
| fragile |  |

| **Input** | **Output** |
| --- | --- |
| 4 | ChevroletExpress |
| ChevroletExpress 215 255 1200 flamable 2.5 1 2.4 2 2.7 1 2.8 1 | DaciaDokker |
| ChevroletAstro 210 230 1000 flamable 2 1 1.9 2 1.7 3 2.1 1 |  |
| DaciaDokker 230 275 1400 flamable 2.2 1 2.3 1 2.4 1 2 1 |  |
| Citroen2CV 190 165 1200 fragile 0.8 3 0.85 2 0.7 5 0.95 2 |  |
| flamable |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
ChevroletAstro 200 180 1000 fragile 1.3 1 1.5 2 1.4 2 1.7 4
Citroen2CV 190 165 1200 fragile 0.9 3 0.85 2 0.95 2 1.1 1
fragile
[/input]
[output]
Citroen2CV
[/output]
[/test]
[test open]
[input]
4
ChevroletExpress 215 255 1200 flamable 2.5 1 2.4 2 2.7 1 2.8 1
ChevroletAstro 210 230 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
DaciaDokker 230 275 1400 flamable 2.2 1 2.3 1 2.4 1 2 1
Citroen2CV 190 165 1200 fragile 0.8 3 0.85 2 0.7 5 0.95 2
flamable
[/input]
[output]
ChevroletExpress
DaciaDokker
[/output]
[/test]
[test]
[input]
5
ChevroletExpress 215 255 1200 flamable 2.5 1 2.4 2 2.7 1 2.8 1
ChevroletAstro 210 230 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
DaciaDokker 230 275 1400 flamable 2.2 1 2.3 1 2.4 1 2 1
Citroen2CV 190 165 1200 fragile 0.8 3 0.85 2 0.7 5 0.95 2
LaTroca 150 350 1500 flamable 2 1 1.9 2 1.7 3 2.1 1
flamable
[/input]
[output]
ChevroletExpress
DaciaDokker
LaTroca
[/output]
[/test]
[test]
[input]
4
C 200 180 1000 fragile 1.3 1 1.5 2 1.4 2 1.7 4
C2 190 165 1200 fragile 0.9 3 0.85 2 0.95 2 1.1 1
M4 300 250 1500 fragile 0.9 4 0.55 2 0.85 2 1.1 2
M 404 404 4004 fragile 0.9 1 0.9 5 0.9 4 3 5
fragile
[/input]
[output]
C2
M4
M
[/output]
[/test]
[test]
[input]
6
ChevroletExpress 215 255 1200 flamable 2.5 1 2.4 2 2.7 1 2.8 1
ChevroletAstro 210 230 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
DaciaDokker 230 275 1400 flamable 2.2 1 2.3 1 2.4 1 2 1
Citroen2CV 190 165 1200 fragile 0.8 3 0.85 2 0.7 5 0.95 2
Chevrolantiq 210 270 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
KappaMobile 210 330 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
flamable
[/input]
[output]
ChevroletExpress
DaciaDokker
Chevrolantiq
KappaMobile
[/output]
[/test]
[test]
[input]
2
ChevroletExpress 215 200 1200 fragile 2.5 1 2.4 2 2.7 1 2.8 1
ChevroletAstro 210 200 1000 flamable 2 1 1.9 2 1.7 3 2.1 1
flamable
[/input]
[output]

[/output]
[/test]
[test]
[input]
1
T 2000 1800 10000 flamable 1.3 1 1.5 2 1.4 2 1.7 4
flamable
[/input]
[output]
T
[/output]
[/test]
[/tests]
[/code-task]
[/slide]