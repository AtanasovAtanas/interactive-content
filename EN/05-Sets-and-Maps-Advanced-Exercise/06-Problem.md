[slide hideTitle]
# Problem: A Miner Task
[code-task title="Problem: A Miner Task" taskId="bad4cdeb-97fa-4c60-8bd2-41da26365e05" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are given a sequence of strings, each on a **new line**.

Every **odd** line on the console is representing a **resource** (e.g.

Gold, Silver, Copper, and so on), and every **even - quantity**.

Your task is to **collect** the resources and to print them each on a **new line**.

**Print the resources and their quantities in the format:**

`{resource} –> {quantity}`

The quantities inputs will be in the **range** [1 ... 2 000 000 000]

## Examples
| **Input** | **Output** |
| --- | --- |
| Gold | Gold -> 155 |
| 155 | Silver -> 10 |
| Silver | Copper -> 17 |
| 10 |  |
| Copper |  |
| 17 |  |
| stop |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
Gold
155
Silver
10
Copper
17
stop
[/input]
[output]
Gold -\> 155
Silver -\> 10
Copper -\> 17
[/output]
[/test]
[test open]
[input]
Gold
15555555
Silver
10000000
Copper
17000000
Copper
1700
stop
[/input]
[output]
Gold -\> 15555555
Silver -\> 10000000
Copper -\> 17001700
[/output]
[/test]
[test]
[input]
Gold
96941
Silver
40909
Cooper
70826
Gold
26953
Silver
11860
Cooper
68966
Gold
28604
Silver
67208
Cooper
62054
Gold
70777
Silver
5012
Cooper
49873
Gold
667
Silver
70628
Cooper
8741
Gold
42550
Silver
19878
Cooper
16479
Gold
43512
Silver
77785
Cooper
60305
Gold
13619
Silver
53187
Cooper
4777
Gold
45510
Silver
1355
Cooper
434
Gold
19443
Silver
554
Cooper
22528
stop
[/input]
[output]
Gold -\> 388576
Silver -\> 348376
Cooper -\> 364983
[/output]
[/test]
[test]
[input]
Gold
43426
Silver
9066
Cooper
48254
Gold
91578
Silver
65032
Cooper
79895
Gold
13100
Silver
10035
Cooper
38187
Gold
34882
Silver
27216
Cooper
4153
Gold
83120
Silver
91917
Cooper
50021
stop
[/input]
[output]
Gold -\> 266106
Silver -\> 203266
Cooper -\> 220510
[/output]
[/test]
[test]
[input]
Gold
26922
Silver
8566
Cooper
57765
Gold
70738
Silver
6941
Cooper
2538
Gold
70120
Silver
1696
Cooper
73384
Gold
91663
Silver
78550
Cooper
24019
Gold
16221
Silver
89664
Cooper
7669
stop
[/input]
[output]
Gold -\> 275664
Silver -\> 185417
Cooper -\> 165375
[/output]
[/test]
[test]
[input]
Gold
0
Silver
0
Cooper
0
stop
[/input]
[output]
Gold -\> 0
Silver -\> 0
Cooper -\> 0
[/output]
[/test]
[test]
[input]
Gold
2000000000
Silver
2000000000
Cooper
2000000000
stop
[/input]
[output]
Gold -\> 2000000000
Silver -\> 2000000000
Cooper -\> 2000000000
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
