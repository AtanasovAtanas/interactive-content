[slide hideTitle]
# Problem: Car Salesman
[code-task title="Problem: Car Salesman" taskId="bd8337bb-a2b2-4af9-b2db-ab23ef09eb24" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Define two classes **Car** and **Engine**.

A **Car** has a **model, engine, weight** and **color**.

An Engine has **model, power, displacement** and **efficiency**.

A Car's **weight** and **color** and its Engine's **displacements** and **efficiency** are **optional**.

On the first line, you will read a number **N** which will specify how many lines of engines you will receive. 

On each of the next **N** lines you will receive information about an **Engine** in the following format:

`<model> <power> <displacement> <efficiency>`

After the lines with engines, on the next line you will receive a number **M** – specifying the number of Cars that will follow. 

On each of the next **M** lines the information about a **Car** will follow in the following format:

`<model> <engine> <weight> <color>`

Where the engine in the format will be the **model of an existing Engine**. 

When creating the object for a **Car**, you should keep a **reference to the real engine** in it, instead of just the engines model, **note** that the optional properties **might be missing** from the formats.

Your task is to print each car (in the **order** you **received** them) and its information in the format defined below. 

If any of the optional fields have not been given print **"n/a"** in its place instead of:

**<carModel>:**
**<engineModel>:**
**Power: <enginePower>**
**Displacement: <engineDisplacement>**
**Efficiency: <engineEfficiency>**
**Weight: <carWeight>**
**Color: <carColor>**

## Optional

Override the classes **toString()** methods to have a reusable way of displaying the objects.

## Examples
| **Input** | **Output** |
| --- | --- |
| 2 | FordFocus: |
| V8-101 220 50 | V4-33: |
| V4-33 140 28 B | Power: 140 |
| 3 | Displacement: 28 |
| FordFocus V4-33 1300 Silver | Efficiency: B |
| FordMustang V8-101 | Weight: 1300 |
| VolkswagenGolf V4-33 Orange | Color: Silver |
|  | FordMustang: |
|  | V8-101: |
|  | Power: 220 |
|  | Displacement: 50 |
|  | Efficiency: n/a |
|  | Weight: n/a |
|  | Color: n/a |
|  | VolkswagenGolf: |
|  | V4-33: |
|  | Power: 140 |
|  | Displacement: 28 |
|  | Efficiency: B |
|  | Weight: n/a |
|  | Color: Orange |

| **Input** | **Output** |
| --- | --- |
| 4 | FordMondeo: |
| DSL-10 280 B | DSL-13: |
| V7-55 200 35 | Power: 305 |
| DSL-13 305 55 A+ | Displacement: 55 |
| V7-54 190 30 D | Efficiency: A+ |
| 4 | Weight: n/a |
| FordMondeo DSL-13 Purple | Color: Purple |
| VolkswagenPolo V7-54 1200 Yellow | VolkswagenPolo: |
| VolkswagenPassat DSL-10 1375 Blue | V7-54: |
| FordFusion DSL-13 | Power: 190 |
|  | Displacement: 30 |
|  | Efficiency: D |
|  | Weight: 1200 |
|  | Color: Yellow |
|  | VolkswagenPassat: |
|  | DSL-10: |
|  | Power: 280 |
|  | Displacement: n/a |
|  | Efficiency: B |
|  | Weight: 1375 |
|  | Color: Blue |
|  | FordFusion: |
|  | DSL-13: |
|  | Power: 305 |
|  | Displacement: 55 |
|  | Efficiency: A+ |
|  | Weight: n/a |
|  | Color: n/a |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
2
V8-101 220 50
V4-33 140 28 B
3
FordFocus V4-33 1300 Silver
FordMustang V8-101
VolkswagenGolf V4-33 Orange
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 28
Efficiency: B
Weight: 1300
Color: Silver
FordMustang:
V8-101:
Power: 220
Displacement: 50
Efficiency: n/a
Weight: n/a
Color: n/a
VolkswagenGolf:
V4-33:
Power: 140
Displacement: 28
Efficiency: B
Weight: n/a
Color: Orange
[/output]
[/test]
[test open]
[input]
4
DSL-10 280 B
V7-55 200 35
DSL-13 305 55 A+
V7-54 190 30 D
4
FordMondeo DSL-13 Purple
VolkswagenPolo V7-54 1200 Yellow
VolkswagenPassat DSL-10 1375 Blue
FordFusion DSL-13
[/input]
[output]
FordMondeo:
DSL-13:
Power: 305
Displacement: 55
Efficiency: A+
Weight: n/a
Color: Purple
VolkswagenPolo:
V7-54:
Power: 190
Displacement: 30
Efficiency: D
Weight: 1200
Color: Yellow
VolkswagenPassat:
DSL-10:
Power: 280
Displacement: n/a
Efficiency: B
Weight: 1375
Color: Blue
FordFusion:
DSL-13:
Power: 305
Displacement: 55
Efficiency: A+
Weight: n/a
Color: n/a
[/output]
[/test]
[test]
[input]
4
V8-101 220 50 A
V4-33 140 28 B
V6-33 230 28 D
V7-44 330 35 E
5
FordFocus V4-33 1300 Silver
Opelche V7-44 1550 Gold
Orel V8-101 1000 Pink
Nissan V8-101 1050 Yellow
Jugan V6-33 2001 Red
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 28
Efficiency: B
Weight: 1300
Color: Silver
Opelche:
V7-44:
Power: 330
Displacement: 35
Efficiency: E
Weight: 1550
Color: Gold
Orel:
V8-101:
Power: 220
Displacement: 50
Efficiency: A
Weight: 1000
Color: Pink
Nissan:
V8-101:
Power: 220
Displacement: 50
Efficiency: A
Weight: 1050
Color: Yellow
Jugan:
V6-33:
Power: 230
Displacement: 28
Efficiency: D
Weight: 2001
Color: Red
[/output]
[/test]
[test]
[input]
5
V8-101 220 50
V4-33 140 28
V6-33 230 28
V7-44 330 35
V12-45 450 60 
7
FordFocus V4-33 1300 Silver
Opelche V7-44 1550 Gold
Orel V8-101 1000 Pink
Nissan V8-101 1050 Yellow
Jugan V6-33 2001 Red
Trabant V12-45 1000 White
Trabant V7-44 600 Green
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 28
Efficiency: n/a
Weight: 1300
Color: Silver
Opelche:
V7-44:
Power: 330
Displacement: 35
Efficiency: n/a
Weight: 1550
Color: Gold
Orel:
V8-101:
Power: 220
Displacement: 50
Efficiency: n/a
Weight: 1000
Color: Pink
Nissan:
V8-101:
Power: 220
Displacement: 50
Efficiency: n/a
Weight: 1050
Color: Yellow
Jugan:
V6-33:
Power: 230
Displacement: 28
Efficiency: n/a
Weight: 2001
Color: Red
Trabant:
V12-45:
Power: 450
Displacement: 60
Efficiency: n/a
Weight: 1000
Color: White
Trabant:
V7-44:
Power: 330
Displacement: 35
Efficiency: n/a
Weight: 600
Color: Green
[/output]
[/test]
[test]
[input]
5
V8-101 220 C
V4-33 140 B
V33-33 220 D
V12-101 340 A
V10-10 210 E+
6
FordFocus V4-33 1300 Silver
Trabant V10-10 600 Gold
Jaguar V8-101 1235 Green
Toyota V33-33 1200 Green
MercedesSmart V8-101 1100 None
MiniCooper V12-101 100 YellowBlack
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: n/a
Efficiency: B
Weight: 1300
Color: Silver
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: E+
Weight: 600
Color: Gold
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: C
Weight: 1235
Color: Green
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: D
Weight: 1200
Color: Green
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: C
Weight: 1100
Color: None
MiniCooper:
V12-101:
Power: 340
Displacement: n/a
Efficiency: A
Weight: 100
Color: YellowBlack
[/output]
[/test]
[test]
[input]
7
V8-101 220
V4-33 140
V33-33 220
V12-101 340
V10-10 210
V11-1110 110
V01-1011 230
10
FordFocus V4-33 1300 Silver
Trabant V10-10 600 Gold
Ford V4-33 650 Red
Jaguar V8-101 1235 Green
Toyota V33-33 1200 Green
Trabant V11-1110 1200 BlackYellow
MercedesSmart V8-101 1100 None
Tesla V01-1011 1230 PinkGreen
MiniCooper V12-101 100 YellowBlack
Motor123 V12-101 1000 JellyBeanColor
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: n/a
Efficiency: n/a
Weight: 1300
Color: Silver
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: n/a
Weight: 600
Color: Gold
Ford:
V4-33:
Power: 140
Displacement: n/a
Efficiency: n/a
Weight: 650
Color: Red
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 1235
Color: Green
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 1200
Color: Green
Trabant:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: n/a
Weight: 1200
Color: BlackYellow
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 1100
Color: None
Tesla:
V01-1011:
Power: 230
Displacement: n/a
Efficiency: n/a
Weight: 1230
Color: PinkGreen
MiniCooper:
V12-101:
Power: 340
Displacement: n/a
Efficiency: n/a
Weight: 100
Color: YellowBlack
Motor123:
V12-101:
Power: 340
Displacement: n/a
Efficiency: n/a
Weight: 1000
Color: JellyBeanColor
[/output]
[/test]
[test]
[input]
7
V8-101 220 220 A
V4-33 140 110 D
V33-33 220 323 C
V12-101 340 325 D
V10-10 210 121 A+
V11-1110 110 450 D++
V01-1011 230 440 B+
11
FordFocus V4-33 1300
Trabant V10-10 600
Ford V4-33 650
Jaguar V8-101 1235
Toyota V33-33 1200
Trabant V11-1110 1200
MercedesSmart V8-101 1100
Tesla V01-1011 1230
MiniCooper V12-101 100
Motor123 V12-101 1001
Kolichka V11-1110 1234
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: 1300
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: 121
Efficiency: A+
Weight: 600
Color: n/a
Ford:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: 650
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: 1235
Color: n/a
Toyota:
V33-33:
Power: 220
Displacement: 323
Efficiency: C
Weight: 1200
Color: n/a
Trabant:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: 1200
Color: n/a
MercedesSmart:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: 1100
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: 440
Efficiency: B+
Weight: 1230
Color: n/a
MiniCooper:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: 100
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: 1001
Color: n/a
Kolichka:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: 1234
Color: n/a
[/output]
[/test]
[test]
[input]
7
V8-101 220 220 A
V4-33 140 110 D
V33-33 220 323 C
V12-101 340 325 D
V10-10 210 121 A+
V11-1110 110 450 D++
V01-1011 230 440 B+
11
FordFocus V4-33 Yellow
Trabant V10-10 Green
Ford V4-33 Black
Jaguar V8-101 White
Toyota V33-33 Red
Trabant V11-1110 None
MercedesSmart V8-101 GrayMetalic
Tesla V01-1011 Gray
MiniCooper V12-101 Purple
Motor123 V12-101 Pink
Kolichka V11-1110 Colorless
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: n/a
Color: Yellow
Trabant:
V10-10:
Power: 210
Displacement: 121
Efficiency: A+
Weight: n/a
Color: Green
Ford:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: n/a
Color: Black
Jaguar:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: n/a
Color: White
Toyota:
V33-33:
Power: 220
Displacement: 323
Efficiency: C
Weight: n/a
Color: Red
Trabant:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: n/a
Color: None
MercedesSmart:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: n/a
Color: GrayMetalic
Tesla:
V01-1011:
Power: 230
Displacement: 440
Efficiency: B+
Weight: n/a
Color: Gray
MiniCooper:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: n/a
Color: Purple
Motor123:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: n/a
Color: Pink
Kolichka:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: n/a
Color: Colorless
[/output]
[/test]
[test]
[input]
7
V8-101 220 220 A
V4-33 140 110 D
V33-33 220 323 C
V12-101 340 325 D
V10-10 210 121 A+
V11-1110 110 450 D++
V01-1011 230 440 B+
11
FordFocus V4-33
Trabant V10-10
Ford V4-33
Jaguar V8-101
Toyota V33-33
Trabant V11-1110
MercedesSmart V8-101
Tesla V01-1011
MiniCooper V12-101
Motor123 V12-101
Kolichka V11-1110
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: n/a
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: 121
Efficiency: A+
Weight: n/a
Color: n/a
Ford:
V4-33:
Power: 140
Displacement: 110
Efficiency: D
Weight: n/a
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: n/a
Color: n/a
Toyota:
V33-33:
Power: 220
Displacement: 323
Efficiency: C
Weight: n/a
Color: n/a
Trabant:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: n/a
Color: n/a
MercedesSmart:
V8-101:
Power: 220
Displacement: 220
Efficiency: A
Weight: n/a
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: 440
Efficiency: B+
Weight: n/a
Color: n/a
MiniCooper:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: n/a
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: 325
Efficiency: D
Weight: n/a
Color: n/a
Kolichka:
V11-1110:
Power: 110
Displacement: 450
Efficiency: D++
Weight: n/a
Color: n/a
[/output]
[/test]
[test]
[input]
7
V8-101 220
V4-33 140
V33-33 220
V12-101 340
V10-10 210
V11-1110 110
V01-1011 230
12
FordFocus V4-33
Trabant V10-10
Ford V4-33
Jaguar V8-101
Toyota V33-33
Trabant V11-1110
MercedesSmart V8-101
Tesla V01-1011
MiniCooper V12-101
Motor123 V12-101
Kolichka V11-1110
Tracktorche V8-101
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Ford:
V4-33:
Power: 140
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Trabant:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
MiniCooper:
V12-101:
Power: 340
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Kolichka:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Tracktorche:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
[/output]
[/test]
[test]
[input]
7
V8-101 220
V4-33 140 430
V33-33 220 E+
V12-101 340 230 A++
V10-10 210
V11-1110 110 C
V01-1011 230 330
12
FordFocus V4-33
Trabant V10-10
Ford V4-33
Jaguar V8-101
Toyota V33-33
Trabant V11-1110
MercedesSmart V8-101
Tesla V01-1011
MiniCooper V12-101
Motor123 V12-101
Kolichka V11-1110
Tracktorche V8-101
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 430
Efficiency: n/a
Weight: n/a
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Ford:
V4-33:
Power: 140
Displacement: 430
Efficiency: n/a
Weight: n/a
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: E+
Weight: n/a
Color: n/a
Trabant:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: C
Weight: n/a
Color: n/a
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: 330
Efficiency: n/a
Weight: n/a
Color: n/a
MiniCooper:
V12-101:
Power: 340
Displacement: 230
Efficiency: A++
Weight: n/a
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: 230
Efficiency: A++
Weight: n/a
Color: n/a
Kolichka:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: C
Weight: n/a
Color: n/a
Tracktorche:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
[/output]
[/test]
[test]
[input]
8
V8-101 220
V4-33 140 430
V33-33 220 E+
V12-101 340 230 A++
V10-10 210
V11-1110 110 C
V01-1011 230 330
V22-22 323 100 A-
13
FordFocus V4-33
Trabant V10-10 Yellow
Ford V4-33 1230
Jaguar V8-101 1200 Green
Toyota V33-33 900 Purple
Trabant V11-1110 1000
Lambo V22-22 999 Gold
MercedesSmart V8-101
Tesla V01-1011 GreenishPurple
MiniCooper V12-101 9000
Motor123 V12-101 790 Colorful
Kolichka V11-1110 Colorless
Tracktorche V8-101 899 Gray
[/input]
[output]
FordFocus:
V4-33:
Power: 140
Displacement: 430
Efficiency: n/a
Weight: n/a
Color: n/a
Trabant:
V10-10:
Power: 210
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: Yellow
Ford:
V4-33:
Power: 140
Displacement: 430
Efficiency: n/a
Weight: 1230
Color: n/a
Jaguar:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 1200
Color: Green
Toyota:
V33-33:
Power: 220
Displacement: n/a
Efficiency: E+
Weight: 900
Color: Purple
Trabant:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: C
Weight: 1000
Color: n/a
Lambo:
V22-22:
Power: 323
Displacement: 100
Efficiency: A-
Weight: 999
Color: Gold
MercedesSmart:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: n/a
Color: n/a
Tesla:
V01-1011:
Power: 230
Displacement: 330
Efficiency: n/a
Weight: n/a
Color: GreenishPurple
MiniCooper:
V12-101:
Power: 340
Displacement: 230
Efficiency: A++
Weight: 9000
Color: n/a
Motor123:
V12-101:
Power: 340
Displacement: 230
Efficiency: A++
Weight: 790
Color: Colorful
Kolichka:
V11-1110:
Power: 110
Displacement: n/a
Efficiency: C
Weight: n/a
Color: Colorless
Tracktorche:
V8-101:
Power: 220
Displacement: n/a
Efficiency: n/a
Weight: 899
Color: Gray
[/output]
[/test]
[/tests]
[/code-task]
[/slide]