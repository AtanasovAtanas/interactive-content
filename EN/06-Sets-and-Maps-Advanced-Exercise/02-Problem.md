[slide]
# Problem: Sets of Elements
[code-task title="Problem: Sets of Elements" taskId="2ebfb89c-b1ab-44a3-a8f6-3767d98bc225" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
On the first line, you are given **the length of two sets n and m**.

On the **next n + m** lines, there are **n numbers that are in the first set** and **m numbers that are in the second**.

Find all **non-repeating elements** that appears in **both** of them, and print them in **the same order** at the console:

Set with length n = 4: {1, **3** , **5** , 7}

Set with length m = 3: { **3** , 4, **5** }

Set that contains all repeating elements -> { **3** , **5** }

## Examples
| **Input** | **Output** |
| --- | --- |
| 4 3 | 3 5 |
| 1 |  |
| 3 |  |
| 5 |  |
| 7 |  |
| 3 |  |
| 4 |  |
| 5 |  |

| **Input** | **Output** |
| --- | --- |
| 2 2 | 1 |
| 1 |  |
| 3 |  |
| 1 |  |
| 5 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
4 3
1
3
5
7
3
4
5
[/input]
[output]
3 5
[/output]
[/test]
[test open]
[input]
2 2
1
3
1
5
[/input]
[output]
1
[/output]
[/test]
[test]
[input]
5 5
5
6
16
8
12
5
6
16
8
12
[/input]
[output]
5 6 16 8 12
[/output]
[/test]
[test]
[input]
5 5
5
5
16
8
12
5
5
16
8
12
[/input]
[output]
5 16 8 12
[/output]
[/test]
[test]
[input]
2 2
2
2
2
2
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
0 0
[/input]
[output]

[/output]
[/test]
[test]
[input]
40 40
12
91
84
19
35
46
81
73
17
93
47
109
18
38
31
8
37
118
51
118
48
19
38
9
86
98
30
69
120
62
98
96
80
35
117
18
10
118
19
93
104
114
116
23
110
82
121
75
50
20
114
44
113
87
79
37
108
94
31
95
45
114
119
39
4
107
16
103
73
19
71
49
118
71
99
79
47
29
10
39
[/input]
[output]
19 73 47 31 37 118 10
[/output]
[/test]
[/tests]
[/code-task]
[/slide]