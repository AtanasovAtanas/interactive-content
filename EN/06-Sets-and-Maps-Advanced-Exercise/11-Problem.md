[slide]
# Problem: Logs Aggregator
[code-task title="Problem: Logs Aggregator" taskId="8e468d5a-5145-4713-85f5-4d7f41f70f72" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
You are given a sequence of access logs in format `< IP > < user > < duration >`.

For example:

- 168.0.11 peter 33
- 10.17.33 alex 12
- 10.17.35 peter 30
- 10.17.34 peter 120
- 10.17.34 peter 120
- 50.118.81 alex 46
- 50.118.81 alex 4

Write a program to aggregate the logs data and print **for each user** the **total duration** of his sessions and a **list of unique IP addresses** in format `< user > < duration > [ < IP1 >, < IP2 >, ...]`. 

Order the **users alphabetically**. 

Order the **IPs alphabetically**. 

The output should be printed like this:

- alex: 62 [10.10.17.33, 212.50.118.81]
- peter: 303 [10.10.17.34, 10.10.17.35, 192.168.0.11]

## Input

The input comes from the console. 

At the first line is a number **n** - the count of the following lines. 

Each of the next n lines holds a log information in format `< IP > < user > < duration >`. 

The input data will always be **valid** and in the described format. 

There is no need to check it explicitly.

## Output

Print **single line for each user** (order users alphabetically). 

For each user print the sum of durations and all of his session IPs, ordered alphabetically in format `< user >: < duration > [< IP1 >, < IP2 >, ...]`. 

Remove any duplicated values in the IP addresses.

## Constraints

- The **count** of the lines **n** is in the range [1 ... 1000].
- The **< IP >** is a standard IP address in format **a.b.c.d** where **a**, **b**, **c** and **d** are integers in the range [0 ... 255].
- The **< user >** consists only of **Latin characters**, with length of [1 .... 20].
- The **< duration >** is an integer number in the range [1 ... 1000].
- Time limit: 0.3 sec. Memory limit: 16 MB.

## Examples
| **Input** | **Output** |
| --- | --- |
| Sofia|Bulgaria|1000000 | Bulgaria (total population: 1000000) |
| report | =>Sofia: 1000000 |
|  |  |

| **Input** | **Output** |
| --- | --- |
| 7 | alex: 62 [10.10.17.33, 212.50.118.81] |
| 192.168.0.11 peter 33 | peter: 303 [10.10.17.34, 10.10.17.35, 192.168.0.11] |
| 10.10.17.33 alex 12 |  |
| 10.10.17.35 peter 30 |  |
| 10.10.17.34 peter 120 |  |
| 10.10.17.34 peter 120 |  |
| 212.50.118.81 alex 46 |  |
| 212.50.118.81 alex 4 |  |

| **Input** | **Output** |
| --- | --- |
| 2 | john: 60 [84.238.140.178] |
| 84.238.140.178 john 25 |  |
| 84.238.140.178 john 35 |  |

[/task-description]
[code-io /]
[tests]
[test open]
[input]
7
192.168.0.11 peter 33
10.10.17.33 alex 12
10.10.17.35 peter 30
10.10.17.34 peter 120
10.10.17.34 peter 120
212.50.118.81 alex 46
212.50.118.81 alex 4
[/input]
[output]
alex: 62 \[10.10.17.33, 212.50.118.81\]
peter: 303 \[10.10.17.34, 10.10.17.35, 192.168.0.11\]
[/output]
[/test]
[test open]
[input]
2
84.238.140.178 john 25
84.238.140.178 john 35
[/input]
[output]
john: 60 \[84.238.140.178\]
[/output]
[/test]
[test]
[input]
1
8.8.8.8 google 100
[/input]
[output]
google: 100 \[8.8.8.8\]
[/output]
[/test]
[test]
[input]
2
8.8.8.8 google 50
10.10.10.10 test 500
[/input]
[output]
google: 50 \[8.8.8.8\]
test: 500 \[10.10.10.10\]
[/output]
[/test]
[test]
[input]
4
10.10.10.10 test 500
8.8.8.8 google 150
10.10.10.10 test 100
8.8.8.8 google 50
[/input]
[output]
google: 200 \[8.8.8.8\]
test: 600 \[10.10.10.10\]
[/output]
[/test]
[test]
[input]
4
10.10.10.10 root 46
8.8.8.8 root 167
1.2.3.4 root 120
5.6.7.8 root 970
192.168.0.11 root 55
[/input]
[output]
root: 1303 \[1.2.3.4, 10.10.10.10, 5.6.7.8, 8.8.8.8\]
[/output]
[/test]
[test]
[input]
14
8.8.8.8 google 100
8.8.8.8 google 50
10.10.10.10 test 98
10.10.10.10 google 730
8.8.8.8 google 150
10.10.10.10 test 100
8.8.8.8 google 50
10.10.10.10 root 46
10.10.10.10 root 58
8.8.8.8 root 167
1.2.3.4 root 120
5.6.7.8 root 970
192.168.0.11 root 55
10.10.10.10 test 302
[/input]
[output]
google: 1080 \[10.10.10.10, 8.8.8.8\]
root: 1416 \[1.2.3.4, 10.10.10.10, 192.168.0.11, 5.6.7.8, 8.8.8.8\]
test: 500 \[10.10.10.10\]
[/output]
[/test]
[test]
[input]
30
8.8.8.8 pepi 100
8.8.8.8 google 999
8.8.8.8 google 100
8.8.8.8 didi 999
10.10.10.10 steve 98
10.10.10.10 google 730
8.8.8.8 google 150
10.10.10.10 test 100
8.8.8.8 google 50
10.10.10.10 root 46
10.10.10.10 root 58
8.8.8.8 nakov 167
1.2.3.4 peter 120
5.6.7.8 root 970
192.168.0.33 root 55
10.10.10.10 kurtev 302
8.8.28.8 google 100
8.8.8.8 google 50
10.10.10.10 test 98
10.10.10.10 google 730
8.8.8.8 google 150
10.10.10.103 test 100
8.8.8.18 google 50
10.10.10.10 root 46
10.10.10.10 george 58
8.8.8.8 root 167
1.2.3.4 maria 120
5.6.7.8 root 970
192.168.0.11 root 55
10.10.10.1 test 302
[/input]
[output]
didi: 999 \[8.8.8.8\]
george: 58 \[10.10.10.10\]
google: 3109 \[10.10.10.10, 8.8.28.8, 8.8.8.18, 8.8.8.8\]
kurtev: 302 \[10.10.10.10\]
maria: 120 \[1.2.3.4\]
nakov: 167 \[8.8.8.8\]
pepi: 100 \[8.8.8.8\]
peter: 120 \[1.2.3.4\]
root: 2367 \[10.10.10.10, 192.168.0.11, 192.168.0.33, 5.6.7.8, 8.8.8.8\]
steve: 98 \[10.10.10.10\]
test: 600 \[10.10.10.1, 10.10.10.10, 10.10.10.103\]
[/output]
[/test]
[test]
[input]
60
8.18.8.8 pepi 100
8.8.28.8 kiki 999
8.8.48.8 google 100
8.83.8.8 didi 999
10.140.10.10 steve 98
10.10.10.10 google 630
8.38.8.8 google 150
10.140.10.10 kiki 100
8.8.68.8 google 50
110.10.10.10 root 46
10.160.10.10 root 58
8.8.8.86 nakov 166
1.26.3.4 peter 120
5.26.6.8 hristo 960
192.168.0.33 didi 55
10.160.10.10 kurtev 302
8.8.28.8 google 100
8.8.38.8 google 50
10.140.10.10 test 98
10.10.10.10 google 630
8.8.8.8 google 150
10.10.10.103 test 100
8.8.8.18 google 50
10.106.10.10 root 46
160.10.10.10 george 58
8.8.86.8 root 166
1.2.3.4 maria 120
5.6.66.8 root 960
192.168.0.11 penka 55
10.10.10.1 test 302
8.8.86.8 pepi 100
8.86.8.8 google 999
8.86.8.8 google 100
8.8.8.8 didi 999
10.10.10.10 steve 98
10.10.10.10 google 630
8.8.86.8 google 150
10.10.10.10 test 100
8.8.8.8 google 50
10.160.10.10 root 46
10.10.10.10 root 58
8.8.8.8 nakov 166
1.2.63.4 peter 120
5.66.6.8 hristo 960
192.168.0.33 martin 55
10.10.10.10 kurtev 302
8.8.228.8 google 100
8.8.8.8 google 50
10.10.10.10 test 98
10.130.10.10 google 630
8.8.8.8 google 150
10.130.10.103 steve 100
8.8.8.18 joke 50
10.10.10.10 root 46
10.10.10.10 george 58
8.8.38.8 penka 166
1.2.3.4 maria 120
5.26.6.8 root 960
192.168.0.12 root 55
10.10.10.11 test 302
[/input]
[output]
didi: 2053 \[192.168.0.33, 8.8.8.8, 8.83.8.8\]
george: 116 \[10.10.10.10, 160.10.10.10\]
google: 4769 \[10.10.10.10, 10.130.10.10, 8.38.8.8, 8.8.228.8, 8.8.28.8, 8.8.38.8, 8.8.48.8, 8.8.68.8, 8.8.8.18, 8.8.8.8, 8.8.86.8, 8.86.8.8\]
hristo: 1920 \[5.26.6.8, 5.66.6.8\]
joke: 50 \[8.8.8.18\]
kiki: 1099 \[10.140.10.10, 8.8.28.8\]
kurtev: 604 \[10.10.10.10, 10.160.10.10\]
maria: 240 \[1.2.3.4\]
martin: 55 \[192.168.0.33\]
nakov: 332 \[8.8.8.8, 8.8.8.86\]
penka: 221 \[192.168.0.11, 8.8.38.8\]
pepi: 200 \[8.18.8.8, 8.8.86.8\]
peter: 240 \[1.2.63.4, 1.26.3.4\]
root: 2441 \[10.10.10.10, 10.106.10.10, 10.160.10.10, 110.10.10.10, 192.168.0.12, 5.26.6.8, 5.6.66.8, 8.8.86.8\]
steve: 296 \[10.10.10.10, 10.130.10.103, 10.140.10.10\]
test: 1000 \[10.10.10.1, 10.10.10.10, 10.10.10.103, 10.10.10.11, 10.140.10.10\]
[/output]
[/test]
[test]
[input]
15
8.18.8.8 pepi 100
8.8.28.8 kiki 999
8.8.48.8 google 100
8.83.8.8 didi 999
10.140.10.10 steve 98
10.10.10.10 google 630
8.38.8.8 google 150
10.140.10.10 kiki 100
8.8.68.8 google 50
110.10.10.10 root 46
10.160.10.10 root 58
8.8.8.86 nakov 166
1.26.3.4 peter 120
5.26.6.8 hristo 960
12.168.0.33 didi 55
[/input]
[output]
didi: 1054 \[12.168.0.33, 8.83.8.8\]
google: 930 \[10.10.10.10, 8.38.8.8, 8.8.48.8, 8.8.68.8\]
hristo: 960 \[5.26.6.8\]
kiki: 1099 \[10.140.10.10, 8.8.28.8\]
nakov: 166 \[8.8.8.86\]
pepi: 100 \[8.18.8.8\]
peter: 120 \[1.26.3.4\]
root: 104 \[10.160.10.10, 110.10.10.10\]
steve: 98 \[10.140.10.10\]
[/output]
[/test]
[test]
[input]
30
8.18.8.8 pepi 100
8.8.28.8 kiki 999
8.8.48.8 google 100
8.83.8.8 didi 999
10.140.10.10 steve 98
10.10.10.10 google 630
8.38.8.8 google 150
10.140.10.10 kiki 100
8.8.68.8 google 50
110.10.10.10 root 46
10.160.10.10 root 58
8.8.8.86 nakov 166
1.26.3.4 peter 120
5.26.6.8 hristo 960
12.168.0.33 didi 55
10.160.10.10 kurtev 302
8.8.28.8 google 100
8.8.38.8 google 50
10.140.10.10 test 98
10.10.10.10 google 630
8.8.8.8 google 150
10.10.10.103 test 100
8.8.8.18 google 50
10.106.10.10 root 46
160.10.10.10 george 58
8.8.86.8 root 166
1.2.3.4 maria 120
5.6.66.8 root 960
192.168.0.11 penka 55
10.10.10.1 test 302
[/input]
[output]
didi: 1054 \[12.168.0.33, 8.83.8.8\]
george: 58 \[160.10.10.10\]
google: 1910 \[10.10.10.10, 8.38.8.8, 8.8.28.8, 8.8.38.8, 8.8.48.8, 8.8.68.8, 8.8.8.18, 8.8.8.8\]
hristo: 960 \[5.26.6.8\]
kiki: 1099 \[10.140.10.10, 8.8.28.8\]
kurtev: 302 \[10.160.10.10\]
maria: 120 \[1.2.3.4\]
nakov: 166 \[8.8.8.86\]
penka: 55 \[192.168.0.11\]
pepi: 100 \[8.18.8.8\]
peter: 120 \[1.26.3.4\]
root: 1276 \[10.106.10.10, 10.160.10.10, 110.10.10.10, 5.6.66.8, 8.8.86.8\]
steve: 98 \[10.140.10.10\]
test: 500 \[10.10.10.1, 10.10.10.103, 10.140.10.10\]
[/output]
[/test]
[test]
[input]
50
8.4.8.8 pepi 100
8.8.28.8 kiki 999
8.8.48.8 google 100
8.83.8.8 didi 999
10.140.10.10 steve 98
10.10.10.10 google 630
8.38.8.8 google 150
10.140.10.10 kiki 100
8.8.68.8 google 50
110.5.10.10 root 46
10.160.10.10 root 58
8.8.8.86 nakov 166
1.26.3.4 peter 120
5.26.6.8 hristo 960
12.168.0.33 didi 55
10.160.10.10 kurtev 302
8.8.28.8 google 100
8.8.38.8 google 50
10.140.10.10 test 98
10.10.10.10 google 630
8.8.8.8 google 150
10.10.10.103 test 100
8.8.8.18 google 50
10.106.10.10 root 46
160.10.10.10 george 58
8.8.86.8 root 166
1.2.3.4 maria 120
5.6.66.8 root 960
192.168.0.11 penka 55
10.10.10.1 test 302
8.8.55.8 pepi 100
8.86.8.8 google 999
8.55.8.8 google 100
8.8.8.8 didi 999
10.10.150.10 steve 98
10.10.10.10 google 630
8.8.86.8 google 150
105.10.10.10 test 100
8.8.8.8 google 50
10.160.10.10 root 46
10.10.10.10 root 58
8.8.8.8 nakov 166
1.2.63.4 peter 120
5.66.6.8 hristo 960
192.168.0.33 martin 55
10.10.10.10 kurtev 302
8.84.228.8 google 100
8.8.8.8 google 50
10.10.10.10 test 98
10.130.10.10 google 630
[/input]
[output]
didi: 2053 \[12.168.0.33, 8.8.8.8, 8.83.8.8\]
george: 58 \[160.10.10.10\]
google: 4619 \[10.10.10.10, 10.130.10.10, 8.38.8.8, 8.55.8.8, 8.8.28.8, 8.8.38.8, 8.8.48.8, 8.8.68.8, 8.8.8.18, 8.8.8.8, 8.8.86.8, 8.84.228.8, 8.86.8.8\]
hristo: 1920 \[5.26.6.8, 5.66.6.8\]
kiki: 1099 \[10.140.10.10, 8.8.28.8\]
kurtev: 604 \[10.10.10.10, 10.160.10.10\]
maria: 120 \[1.2.3.4\]
martin: 55 \[192.168.0.33\]
nakov: 332 \[8.8.8.8, 8.8.8.86\]
penka: 55 \[192.168.0.11\]
pepi: 200 \[8.4.8.8, 8.8.55.8\]
peter: 240 \[1.2.63.4, 1.26.3.4\]
root: 1380 \[10.10.10.10, 10.106.10.10, 10.160.10.10, 110.5.10.10, 5.6.66.8, 8.8.86.8\]
steve: 196 \[10.10.150.10, 10.140.10.10\]
test: 698 \[10.10.10.1, 10.10.10.10, 10.10.10.103, 10.140.10.10, 105.10.10.10\]
[/output]
[/test]
[/tests]
[/code-task]
[/slide]