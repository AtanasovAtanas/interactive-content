[slide hideTitle]
# Problem: Count Symbols
[code-task title="Problem: Count Symbols" taskId="7075fd90-4715-4d84-bb4e-7185a33822d3" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
Write a program that reads some **text** from the console and **counts the occurrences of each character** in it.

Print the results in **alphabetical** (lexicographical) order, using the syntax: `{symbol}: {count} time/s`.

## Examples
| **Input** | **Output** |
| --- | --- |
| SoftUni rocks |  : 1 time/s |
|  | S: 1 time/s |
|  | U: 1 time/s |
|  | c: 1 time/s |
|  | f: 1 time/s |
|  | i: 1 time/s |
|  | k: 1 time/s |
|  | n: 1 time/s |
|  | o: 2 time/s |
|  | r: 1 time/s |
|  | s: 1 time/s |
|  | t: 1 time/s |

| **Input** | **Output** |
| --- | --- |
| Did you know Math.Round rounds to the nearest even integer? |  : 9 time/s |
|  | .: 1 time/s |
|  | ?: 1 time/s |
|  | D: 1 time/s |
|  | M: 1 time/s |
|  | R: 1 time/s |
|  | a: 2 time/s |
|  | d: 3 time/s |
|  | e: 7 time/s |
|  | g: 1 time/s |
|  | h: 2 time/s |
|  | i: 2 time/s |
|  | k: 1 time/s |
|  | n: 6 time/s |
|  | o: 5 time/s |
|  | r: 3 time/s |
|  | s: 2 time/s |
|  | t: 5 time/s |
|  | u: 3 time/s |
|  | v: 1 time/s |
|  | w: 1 time/s |
|  | y: 1 time/s |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
SoftUni rocks
[/input]
[output]
 : 1 time/s
S: 1 time/s
U: 1 time/s
c: 1 time/s
f: 1 time/s
i: 1 time/s
k: 1 time/s
n: 1 time/s
o: 2 time/s
r: 1 time/s
s: 1 time/s
t: 1 time/s
[/output]
[/test]
[test open]
[input]
Did you know Math.Round rounds to the nearest even integer?
[/input]
[output]
 : 9 time/s
.: 1 time/s
?: 1 time/s
D: 1 time/s
M: 1 time/s
R: 1 time/s
a: 2 time/s
d: 3 time/s
e: 7 time/s
g: 1 time/s
h: 2 time/s
i: 2 time/s
k: 1 time/s
n: 6 time/s
o: 5 time/s
r: 3 time/s
s: 2 time/s
t: 5 time/s
u: 3 time/s
v: 1 time/s
w: 1 time/s
y: 1 time/s
[/output]
[/test]
[test]
[input]
Write a program that reads some text from the console and counts the occurrences of each character in it
[/input]
[output]
 : 18 time/s
W: 1 time/s
a: 8 time/s
c: 8 time/s
d: 2 time/s
e: 11 time/s
f: 2 time/s
g: 1 time/s
h: 5 time/s
i: 3 time/s
l: 1 time/s
m: 3 time/s
n: 5 time/s
o: 8 time/s
p: 1 time/s
r: 9 time/s
s: 5 time/s
t: 10 time/s
u: 2 time/s
x: 1 time/s
[/output]
[/test]
[test]
[input]
Problem 4.	Count Symbols
[/input]
[output]
    : 1 time/s
 : 2 time/s
.: 1 time/s
4: 1 time/s
C: 1 time/s
P: 1 time/s
S: 1 time/s
b: 2 time/s
e: 1 time/s
l: 2 time/s
m: 2 time/s
n: 1 time/s
o: 3 time/s
r: 1 time/s
s: 1 time/s
t: 1 time/s
u: 1 time/s
y: 1 time/s
[/output]
[/test]
[test]
[input]
0
[/input]
[output]
0: 1 time/s
[/output]
[/test]
[test]
[input]

[/input]
[output]

[/output]
[/test]
[test]
[input]
K - the type of keys maintained by this map
V - the type of mapped values
[/input]
[output]
 : 9 time/s
-: 1 time/s
K: 1 time/s
a: 3 time/s
b: 1 time/s
d: 1 time/s
e: 4 time/s
f: 1 time/s
h: 2 time/s
i: 3 time/s
k: 1 time/s
m: 2 time/s
n: 2 time/s
o: 1 time/s
p: 2 time/s
s: 2 time/s
t: 4 time/s
y: 3 time/s
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
