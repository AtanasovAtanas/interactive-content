[slide]
# Problem: Diagonal Difference
[code-task title="# Problem: Diagonal Difference" taskId="bb9083d2-94d1-4e24-997e-dfa9b838847e" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that finds the **difference between the sums of the square matrix diagonals** (absolute value).

[image assetsSrc="diagonal-difference.png"/]

## Input

- The **first line** holds a number **n** – the size of the matrix.
- The next **n**  **lines** hold the **values for every row** – **n** numbers separated by a space.

## Hints

- Use a **single** loop **i = [ 1 ... n ]** to sum the diagonals.

- The **primary diagonal** holds all cells { **row** , **col** } where **row** == **col** == **i**.
- The **secondary diagonal** holds all cells { **row** , **col** } where **row** == **i** and **col** == **n - 1 - i**.


## Examples
| **Input** | **Output** | **Comments** |
| --- | --- | --- |
| 3 | 15 | **Primary diagonal:** sum = 11 + 5 + (-12) = 4  |
| 11 2 4 |  | **Secondary diagonal:** sum = 4 + 5 + 10 = 19  |
| 4 5 6 |  | **Difference:** 4 - 19 = 15  |
| 10 8 -12 |  |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
11 2 4
4 5 6
10 8 -12
[/input]
[output]
15
[/output]
[/test]
[test open]
[input]
4
-7 14 9 -20
3 4 9 21
-14 6 8 44
30 9 7 -14
[/input]
[output]
34
[/output]
[/test]
[test]
[input]
7
-8 -46 -34 -10 -17 28 -1 
30 -7 -48 50 22 50 47 
47 -40 -48 33 43 -19 9 
36 20 -33 -33 34 -28 -7 
46 42 1 41 -41 41 45 
21 0 -38 -10 -3 30 28 
-19 -13 30 -48 45 27 -50
[/input]
[output]
198
[/output]
[/test]
[test]
[input]
2
13 -34 
41 48
[/input]
[output]
54
[/output]
[/test]
[test]
[input]
10
47 -21 12 6 27 -11 39 -26 -44 -22 
-24 26 45 -18 -30 12 17 -12 -29 -27 
21 -42 33 33 26 27 32 7 -41 -3 
-21 -13 -26 -25 4 13 36 19 2 -40 
25 24 27 -2 -27 -7 -15 -37 23 20 
40 -12 -44 -26 -43 -4 21 -46 -25 48 
-18 15 49 3 -17 -43 46 31 28 -28 
25 16 49 -9 49 4 50 13 11 -32 
26 -36 32 -11 8 -48 12 24 -44 27 
11 -44 17 2 26 -10 -20 -31 -39 -41
[/input]
[output]
55
[/output]
[/test]
[test]
[input]
5
-36 -20 -5 39 -21 
28 32 21 27 -19 
35 33 -34 29 -13 
47 40 -3 25 28 
-15 26 42 18 48
[/input]
[output]
38
[/output]
[/test]
[test]
[input]
20
-16 4 45 -41 -1 10 45 -7 13 28 41 46 10 18 13 -13 48 49 -21 17 
13 -4 -18 14 18 6 14 7 -8 23 -45 6 -50 -38 -25 39 9 7 49 -2 
-13 -27 45 -42 37 -24 -18 -19 -27 -22 0 -32 -23 31 -31 -46 -9 -41 -1 -45 
26 -21 -32 36 5 37 -20 -48 49 -50 -39 21 -9 -43 33 -13 39 0 29 5 
40 -36 -29 23 1 -1 17 9 25 -19 36 43 31 18 -43 -10 -29 0 -31 4 
-49 16 1 -28 46 0 5 16 37 -8 44 1 17 14 -43 -16 31 -6 45 48 
36 20 -27 4 -25 29 -39 30 -38 -46 11 2 -7 14 42 -9 17 -3 44 25 
-25 -4 -36 -26 -6 38 50 43 -7 -9 -44 -3 -35 -20 18 48 10 29 9 -12 
-42 7 -27 -11 -20 -12 -14 18 -20 -20 20 -3 22 -2 11 -45 -9 -22 -39 11 
39 36 46 -6 -19 45 37 -49 -42 50 36 50 -39 -25 46 40 15 31 6 18 
31 -16 35 -23 -32 46 49 43 41 2 29 6 47 0 -23 -11 45 10 -2 -41 
-36 27 3 -5 24 27 38 -26 -34 49 41 21 0 46 9 1 47 -1 -23 -38 
8 13 -21 21 18 -43 8 -28 50 -14 36 -11 -37 24 15 -45 -11 -4 -29 39 
-1 40 8 -46 -40 -1 -32 18 -37 23 -49 -19 32 -7 -42 1 3 23 -21 -38 
30 -39 19 -40 -27 14 -17 -22 40 39 -17 36 0 -14 30 15 38 -50 46 -11 
16 -7 34 1 -31 27 -9 15 40 -32 -24 41 32 -43 24 -15 39 -4 -38 41 
-24 -34 -24 -41 -43 -30 -16 17 -12 -6 36 25 11 45 21 12 -37 48 -45 35 
41 39 24 -47 43 4 22 -11 -16 44 46 -42 -49 44 6 -5 9 -48 -48 -1 
8 33 -8 24 42 -49 -9 -16 -26 11 -30 -43 31 23 -47 -39 46 -29 -9 -5 
-42 -17 18 36 -15 -13 -36 -42 5 -37 2 -46 -35 -36 37 -36 -7 23 32 44
[/input]
[output]
179
[/output]
[/test]
[/tests]
[/code-task]
[/slide]