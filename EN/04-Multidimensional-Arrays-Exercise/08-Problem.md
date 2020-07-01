[slide hideTitle]
# Problem: Parking System
[code-task title="Problem: Parking System" taskId="577fbe15-c817-4701-b2be-a889976e6158" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program for an automated parking system.

The parking lot is a **rectangular** matrix where the **first** column is **always** free and all other cells are parking spots. 

A car can enter from **any cell** of the **first column** and then decides to go to a specific spot. 

If that spot is **not** free, the car searches for the **closest** free spot on the **same** row. 

If **all** the cells on that specific row are used, the car cannot park and leaves. 

If **two** free cells are located at the **same** distance from the **initial** parking spot, the cell which is **closer** to the entrance is preferred. 

A car can **pass** through a used parking spot.

Your task is to calculate the distance traveled by each car to its parking spot.

Example: A car enters the parking at row 1. It wants to go to cell 2, 2 so it moves through **exactly four** cells to reach its parking spot.

[image assetsSrc="parking-system.png"/]

## Input

- On the first line of input, you are given the integers **R** and **C**, defining the dimensions of the parking lot
- On the next several lines, you are given the integers **Z, X, Y** where **Z** is the entry row and **X, Y** are the coordinates of the desired parking spot
- The input stops with the command **"stop"**. All integers are separated by a **single** space

## Output

- For each car, print the distance traveled to the desired spot or the first free spot
- If a car cannot park on its desired row, print the message `Row {row number} full`;

## Constraints

- 2 <= R,C <= 10000
- Z, X, Y are inside the dimensions of the matrix. Y is never on the first column
- There are no more than 1000 input lines

## Examples
| **Input** | **Output** |
| --- | --- |
| 4 4 | 4 |
| 1 2 2 | 2 |
| 2 2 2 | 4 |
| 2 2 2 | Row 2 full |
| 3 2 2 |  |
| stop |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
4 4
1 2 2
2 2 2
2 2 2
3 2 2
stop
[/input]
[output]
4
2
4
Row 2 full
[/output]
[/test]
[test]
[input]
2 2
0 0 1
0 1 1
0 0 1
0 1 1
0 0 1
0 1 1
0 0 1
0 1 1
stop
[/input]
[output]
2
3
Row 0 full
Row 1 full
Row 0 full
Row 1 full
Row 0 full
Row 1 full
[/output]
[/test]
[test]
[input]
2 10
0 0 1
0 0 1
0 0 1
0 0 1
0 0 1
0 0 1
0 0 1
0 0 1
0 0 1
0 0 1
stop
[/input]
[output]
2
3
4
5
6
7
8
9
10
Row 0 full
[/output]
[/test]
[test]
[input]
2 10
0 0 5
0 0 5
0 0 4
0 0 3
0 0 2
0 0 1
0 0 1
0 0 1
0 0 1
0 0 1
stop
[/input]
[output]
6
5
4
3
2
7
8
9
10
Row 0 full
[/output]
[/test]
[test]
[input]
10 10
5 7 6
4 2 2
0 9 9
1 8 8
5 4 2
9 0 9
8 0 1
7 9 9
6 6 6
3 3 7
2 8 8
2 8 7
2 8 6
stop
[/input]
[output]
9
5
19
16
4
19
10
11
7
8
14
13
12
[/output]
[/test]
[test]
[input]
10000 10000
6788 1283 9898
1983 1231 9898
1287 127 1273
768 188 8182
1298 1249 1290
2989 1290 1230
1093 3123 1233
1209 2309 13
9888 1238 1212
8888 11 11
0 9999 9999
6787 1283 9898
1983 1221 9898
1287 127 1278
768 188 8182
1298 1409 1299
2988 1293 1290
1092 3123 1233
1209 2309 213
9898 1238 1232
8888 11 11
0 9999 9999
6788 1283 9888
1983 1231 9898
1287 127 1278
768 188 8182
1298 1240 1290
2989 1930 1930
1023 3123 1233
1209 2309 23
9988 1238 1231
8888 11 11
0 9999 9999
6787 1287 9988
1983 1231 9898
1287 127 1278
768 188 8182
1298 1249 1290
2898 1290 1290
1023 3123 1233
1209 2309 124
9898 1238 1231
8888 11 11
0 9999 9999
stop
[/input]
[output]
15404
10651
2434
8763
1340
2930
3264
1114
9863
8889
19999
15402
10661
2439
8762
1411
2986
3264
1314
9893
8888
19998
15394
10650
2438
8764
1349
2990
3335
1124
9982
8890
19997
15489
10652
2440
8761
1339
2899
3332
1225
9891
8887
19996
[/output]
[/test]
[test]
[input]
11 11
0 0 1
1 1 1
2 2 2
3 3 3
4 4 4
5 5 5
6 6 6
7 7 7
8 8 8
9 9 9
10 10 10
stop
[/input]
[output]
2
2
3
4
5
6
7
8
9
10
11
[/output]
[/test]
[test]
[input]
10 2
0 0 1
0 0 1
0 1 1
0 1 1
0 2 1
0 2 1
0 3 1
0 3 1
0 4 1
0 4 1
0 5 1
0 5 1
0 6 1
0 6 1
0 7 1
0 7 1
0 8 1
0 8 1
0 9 1
0 9 1
stop
[/input]
[output]
2
Row 0 full
3
Row 1 full
4
Row 2 full
5
Row 3 full
6
Row 4 full
7
Row 5 full
8
Row 6 full
9
Row 7 full
10
Row 8 full
11
Row 9 full
[/output]
[/test]
[test]
[input]
5 5
4 0 4
4 0 3
4 0 2
4 0 1
3 1 4
3 1 3
3 1 2
3 1 1
2 2 4
2 2 3
2 2 2
2 2 1
1 3 4
1 3 3
1 3 2
1 3 1
0 4 4
0 4 3
0 4 2
0 4 1
stop
[/input]
[output]
9
8
7
6
7
6
5
4
5
4
3
2
7
6
5
4
9
8
7
6
[/output]
[/test]
[test]
[input]
10000 10000
0 9999 9999
9999 0 9999
stop
[/input]
[output]
19999
19999
[/output]
[/test]
[test]
[input]
50 50
16 12 12
42 42 24
42 42 42
42 42 42
42 42 43
42 42 42
42 42 42
42 24 24
42 42 24
42 42 42
42 42 42
42 42 43
42 42 42
42 42 42
42 42 24
42 42 42
42 42 42
42 42 43
42 42 42
42 42 42
42 42 24
42 42 42
42 42 42
42 42 43
42 42 42
42 42 42
stop
[/input]
[output]
17
25
43
42
44
41
45
43
24
40
46
47
39
38
26
48
37
49
36
50
23
35
34
33
32
31
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
