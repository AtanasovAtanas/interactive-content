[slide]
# Problem: The Matrix
[code-task title="Problem: The Matrix" taskId="250961da-1f32-4b0b-a551-bb5137d0e282" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are given a matrix (2D array) of lowercase alphanumeric characters ( **a-z** , **0-9** ), a starting position – defined by a start row `startRow` and a start column `startCol` – and a filling symbol `fillChar`.

Let's call the symbol originally at `startRow` and `startCol` the `startChar`.

Write a program, which, starting from the symbol at `startRow` and `startCol`, changes to `fillChar` every symbol in the matrix which:


- is equal to **startChar** AND
- can be reached from **startChar** by going up ( **row – 1** ), down ( **row + 1** ), left ( **col – 1** ) and right ( **col + 1** ) and "stepping" ONLY on symbols equal **startChar**

So, you basically start from `startRow` and `startCol` and can move either by changing the row OR column (not both at once, i.e. you can not go diagonally) by **1**, and can only go to positions which have the `startChar` written on them. Once you find all those positions, you change them to `fillChar`.

In other words, you need to implement something like the Fill tool in MS Paint, but for a 2D char array instead of a bitmap.

## Input

On the first line, two integers will be entered – the number **R** of rows and number **C** of columns.

On each of the next **R** lines, **C** characters separated by single spaces will be entered – the symbols of the **R** th row of the matrix, starting from the **0** th column and ending at the **C-1** column.

On the next line, a single character – the `fillChar` – will be entered.

On the last line, two integers – `startRow` and `startCol` – separated by a single space, will be entered.

## Output

The output should consist of R lines, each consisting of exactly C characters, **NOT SEPARATED** by spaces, representing the matrix after the fill operation has been finished.

## Constraints

**0 < R, C < 20**
**0 <= startRow < R**
**0 <= startCol < C**

All symbols in the input matrix will be lowercase alphanumerics ( **a-z** , **0-9** ). The `fillChar` will also be alphanumeric and lowercase.

The total running time of your program should be no more than **0.1s**

The total memory allowed for use by your program is **5MB**

## Hints

For some of the tests you can solve the problem with naive approach, however complete solution can be obtained by using **Stack**, **Queue**, **DFS** or **BFS** – go search on the internet.

## Examples
| **Input** | **Output** |
| --- | --- |
| 5 3 | xxx |
| a a a | xxx |
| a a a | xbx |
| a b a | xbx |
| a b a | xbx |
| a b a |  |
| x |  |
| 0 0 |  |

| **Input** | **Output** |
| --- | --- |
| 5 3 | aaa |
| a a a | aaa |
| a a a | axa |
| a b a | axa |
| a b a | axa |
| a b a |  |
| x |  |
| 2 1 |  |

| **Input** | **Output** |
| --- | --- |
| 5 6 | oo11oo |
| o o 1 1 o o | o1331o |
| o 1 o o 1 o | 133331 |
| 1 o o o o 1 | o1331o |
| o 1 o o 1 o | oo11oo |
| o o 1 1 o o |  |
| 3 |  |
| 2 1 |  |

| **Input** | **Output** |
| --- | --- |
| 5 6 | oooooo |
| o o o o o o | ooo1oo |
| o o o 1 o o | oo1o11 |
| o o 1 o 1 1 | o11w1z |
| o 1 1 w 1 o | 1zzzzz |
| 1 o o o o o |  |
| z |  |
| 4 1 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5 3
a a a
a a a
a b a
a b a
a b a
x
0 0
[/input]
[output]
xxx
xxx
xbx
xbx
xbx
[/output]
[/test]
[test open]
[input]
5 3
a a a
a a a
a b a
a b a
a b a
x
2 1
[/input]
[output]
aaa
aaa
axa
axa
axa
[/output]
[/test]
[test open]
[input]
5 6
o o 1 1 o o
o 1 o o 1 o
1 o o o o 1
o 1 o o 1 o
o o 1 1 o o
3
2 1
[/input]
[output]
oo11oo
o1331o
133331
o1331o
oo11oo
[/output]
[/test]
[test open]
[input]
5 6
o o o o o o
o o o 1 o o
o o 1 o 1 1
o 1 1 w 1 o
1 o o o o o
z
4 1
[/input]
[output]
oooooo
ooo1oo
oo1o11
o11w1z
1zzzzz
[/output]
[/test]
[test open]
[input]
5 6
o 1 o o 1 o
o 1 o o 1 o
o 1 1 1 1 o
o 1 o w 1 o
o o o o o o
z
4 0
[/input]
[output]
z1oo1z
z1oo1z
z1111z
z1zw1z
zzzzzz
[/output]
[/test]
[test]
[input]
19 19
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 1 1 1 1 1 1 0 0 0 0 0 0 0 0
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 1 1 1 1 1 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
h
8 6
[/input]
[output]
0000000000000000000
0000000000000000000
0000011111100000000
000001hhhh100000000
000001hhhh100000000
000001hhhh100000000
000001hhhh100000000
000001hhhh100000000
000001hhhh100000000
0000011111000000000
0000000000000000000
0000000000000000000
0000000000000000000
0000000000000000000
0000000000000000000
0000000000000000000
0000000000000000000
0000000000000000000
0000000000000000000
[/output]
[/test]
[test]
[input]
19 19
0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 1 0 0 1 1 0 0
0 0 0 0 0 1 1 1 1 1 1 0 1 1 0 0 1 1 0
0 0 0 0 0 1 0 0 0 0 1 0 0 1 1 0 0 1 1
0 0 0 0 0 1 0 0 0 0 1 0 0 0 1 1 0 0 1
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 1 0 1
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 1
0 0 0 0 0 1 0 0 0 0 1 1 1 1 1 1 0 0 1
0 0 0 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 1
0 0 0 0 0 1 1 1 1 1 1 0 0 0 0 0 0 0 1
0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 1 1 1
0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 1 0 0
0 0 0 0 0 0 1 1 1 1 1 0 0 0 0 1 1 0 0
0 0 0 0 0 0 1 0 0 0 0 0 0 0 1 1 0 0 0
0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
y
3 5
[/input]
[output]
000000000000yyyy000
000000000000y00yy00
00000yyyyyy0yy00yy0
00000y0000y00yy00yy
00000y0000y000yy00y
00000y0000y0000yy0y
00000y0000y0000y00y
00000y0000yyyyyy00y
00000y000000000000y
00000yyyyyy0000000y
0000000000y00000000
0000000000y00000000
0000000000y00000yyy
0000000000y00000y00
000000yyyyy0000yy00
000000y0000000yy000
000000yyyyyyyyy0000
0000000000000000000
0000000000000000000
[/output]
[/test]
[test]
[input]
19 19
0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 1 0 0 1 0 0 0
0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 1 0 0
0 0 0 0 0 1 0 0 0 0 1 0 0 0 1 0 0 1 0
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 1
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 0 1 0 1
0 0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 1
0 0 0 0 0 1 0 0 0 0 1 1 1 1 1 0 0 0 1
0 0 0 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 1
0 0 0 0 0 1 1 1 1 1 1 0 0 0 0 0 0 0 1
0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 0 1 1
0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 1 0 0
0 0 0 0 0 0 1 1 1 1 1 0 0 0 0 1 0 0 0
0 0 0 0 0 0 1 0 0 0 0 0 0 0 1 0 0 0 0
0 0 0 0 0 0 1 1 1 1 1 1 1 1 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
z
2 14
[/input]
[output]
0000000000000110000
0000000000001zz1000
00000111111001zz100
000001zzzz10001zz10
000001zzzz100001zz1
000001zzzz1000001z1
000001zzzz100001zz1
000001zzzz11111zzz1
000001zzzzzzzzzzzz1
00000111111zzzzzzz1
00000000001zzzzzzzz
00000000001zzzzzzzz
00000000001zzzzzz11
00000000001zzzzz100
00000011111zzzz1000
0000001zzzzzzz10000
0000001111111100000
0000000000000000000
0000000000000000000
[/output]
[/test]
[test]
[input]
4 10
s x x s s s s s s s
a s s x s s s s s s
s a s s x s s s s s
s a s s s x s s s s
f
1 2
[/input]
[output]
sxxsssssss
affxssssss
saffxsssss
safffxssss
[/output]
[/test]
[test]
[input]
1 1
a
b
0 0
[/input]
[output]
b
[/output]
[/test]
[test]
[input]
7 1
u
u
u
u
u
d
u
d
5 0
[/input]
[output]
u
u
u
u
u
d
u
[/output]
[/test]
[test]
[input]
7 1
u
u
u
u
u
d
u
d
6 0
[/input]
[output]
u
u
u
u
u
d
d
[/output]
[/test]
[test]
[input]
1 3
a b 0
0
0 1
[/input]
[output]
a00
[/output]
[/test]
[test]
[input]
4 2
a b
c a
a b
b a
i
0 0
[/input]
[output]
ib
ca
ab
ba
[/output]
[/test]
[/tests]
[/code-task]
[/slide]