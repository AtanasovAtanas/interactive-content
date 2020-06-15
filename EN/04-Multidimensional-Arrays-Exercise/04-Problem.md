[slide]
# Problem: Maximal Sum
[code-task title="Problem: Maximal Sum" taskId="39222da7-dc7c-44ed-ba09-9458d9454bca" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that reads a rectangular integer matrix of size  **N x M**  and finds in it the square  **3 x 3**  that **has maximal sum of its elements**.

## Input

- On the first line, you will receive the rows **N** and columns **M**.
- On the next **N lines** you will receive **each row with its elements**.

Print the **elements** of the 3 x 3 square as a matrix, along with their **sum**. See the format of the output below:

## Examples
| **Input** | **Output** |
| --- | --- |
| 4 5 | Sum = 75 |
| 1 5 5 2 4 | 1 4 14 |
| 2 1 4 14 3 | 7 11 2 |
| 3 7 11 2 8 | 8 12 16 |
| 4 8 12 16 4 |  |

## Comments

[image assetsSrc=""/]

[/task-description]
[code-io /]
[tests]
[test open]
[input]
4 5
1 5 5 2 4
2 1 4 14 3
3 7 11 2 8
4 8 12 16 4
[/input]
[output]
Sum = 75
1 4 14
7 11 2
8 12 16
[/output]
[/test]
[test open]
[input]
5 6
1 0 4 3 1 1 
1 3 1 3 0 4 
6 4 1 2 5 6 
2 2 1 5 4 1 
3 3 3 6 0 5
[/input]
[output]
Sum = 34
2 5 6 
5 4 1 
6 0 5
[/output]
[/test]
[test]
[input]
20 10
4 1 4 1 4 1 3 0 2 1 
2 1 1 3 0 4 4 0 4 3 
3 1 3 1 1 0 4 3 0 2 
4 0 4 0 2 1 1 2 2 1 
2 3 0 3 4 1 3 1 2 4 
0 4 4 2 3 0 3 2 1 4 
4 4 0 4 0 3 4 0 1 2 
0 3 1 3 1 2 4 3 0 2 
3 0 1 1 2 2 4 1 0 2 
1 2 1 1 1 4 2 4 4 3 
4 0 4 0 1 1 4 2 0 4 
1 2 0 2 2 3 0 3 0 2 
0 1 1 1 1 4 0 2 2 1 
3 2 3 0 3 3 2 2 4 3 
2 1 0 1 2 0 4 2 4 3 
3 4 3 1 4 2 1 4 3 4 
3 4 0 4 1 3 2 0 0 4 
4 3 0 0 0 0 2 0 3 2 
0 3 0 2 4 0 2 0 3 2 
4 2 1 2 2 3 2 4 1 2
[/input]
[output]
Sum = 29
2 4 3 
2 4 3 
4 3 4
[/output]
[/test]
[test]
[input]
20 10
1 1 1 2 2 0 1 0 0 0 
1 0 1 0 2 1 2 2 0 2 
0 0 0 1 0 0 2 0 2 1 
1 2 0 0 2 0 2 1 0 1 
0 2 1 2 0 1 1 0 2 2 
1 1 1 0 0 1 2 2 1 1 
0 2 2 1 2 0 1 1 2 2 
0 2 0 2 0 0 1 0 1 0 
0 0 2 2 1 2 2 1 0 1 
2 1 2 1 1 0 0 2 1 2 
2 0 1 0 2 2 0 1 2 1 
1 2 0 2 0 2 1 1 1 1 
2 2 0 2 1 1 2 0 0 0 
2 0 0 0 2 1 1 1 2 2 
2 2 0 1 0 0 2 0 0 0 
0 0 0 1 2 1 2 1 0 1 
2 1 1 0 1 0 1 2 0 1 
0 0 0 2 0 1 0 1 2 1 
0 0 0 2 1 2 0 0 1 2 
1 0 1 2 0 1 1 2 1 1
[/input]
[output]
Sum = 13
0 2 2 
2 1 1 
1 2 2
[/output]
[/test]
[test]
[input]
20 10
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0
[/input]
[output]
Sum = 0
0 0 0 
0 0 0 
0 0 0
[/output]
[/test]
[test]
[input]
5 6
1 1 1 0 1 1 
0 1 1 1 0 0 
1 0 1 0 0 1 
0 0 0 1 1 1 
1 1 1 0 1 0
[/input]
[output]
Sum = 7
1 1 1 
0 1 1 
1 0 1
[/output]
[/test]
[test]
[input]
20 20
18 17 8 10 17 10 1 13 11 5 5 19 11 9 5 16 10 1 18 5 
16 10 12 2 17 16 16 12 13 12 14 0 9 4 18 13 15 6 0 10 
2 5 9 8 17 15 19 14 18 12 8 19 15 19 10 15 2 1 15 18 
0 6 4 18 5 4 7 17 6 16 12 8 19 6 18 8 16 19 19 18 
1 4 8 13 1 10 14 0 0 3 1 2 14 4 15 2 8 7 4 5 
12 19 14 4 8 19 10 17 17 0 0 19 1 9 17 17 10 16 0 7 
19 0 4 16 18 16 17 6 0 3 9 4 7 6 2 6 17 16 19 4 
8 16 17 10 13 17 1 12 0 13 6 3 5 16 6 7 13 11 18 8 
7 8 16 5 2 12 13 11 12 18 11 9 8 7 19 8 16 17 5 19 
10 17 16 4 18 11 8 12 6 19 14 9 2 6 3 0 19 4 1 18 
4 13 5 17 6 2 6 0 13 8 14 1 4 8 16 6 2 11 2 12 
4 12 16 16 5 15 10 1 2 18 18 2 0 17 1 12 4 19 0 3 
13 18 3 14 19 7 7 15 3 11 11 5 9 5 8 7 18 5 1 6 
6 7 13 5 2 17 11 16 5 10 1 3 10 16 15 2 6 18 18 16 
15 3 9 1 16 16 4 7 0 7 19 6 8 6 8 9 0 8 12 12 
10 16 5 12 4 18 19 17 3 9 0 12 1 0 13 19 12 10 13 0 
0 2 11 1 7 2 9 12 14 7 6 12 11 17 1 3 15 17 13 11 
7 1 3 11 15 8 12 16 19 11 19 19 0 11 7 15 4 10 8 1 
16 17 10 11 14 2 16 16 13 14 18 3 10 15 15 1 12 1 2 5 
10 19 15 18 10 5 11 9 8 12 10 3 15 18 1 18 17 12 6 3
[/input]
[output]
Sum = 132
17 16 19 
13 11 18 
16 17 5
[/output]
[/test]
[/tests]
[/code-task]
[/slide]